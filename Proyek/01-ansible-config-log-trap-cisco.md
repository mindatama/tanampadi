# Proyek pertama 
adalah membuat konfigurasi kode dengan menggunakan ansible. perangkat yang di manage adalah swith cisco berjumlah kurang lebih 28 perangkat. diberikan perintah untuk mengirim log ke log trap server dengan level severity errors.<br>

## Kenapa pakai ansible
dengan banyaknya perangkat network yang di manage, akan sangat memakan waktu ketika perangkat makin bertambah. untuk mempersingkat sumber daya (tenaga dan waktu) maka dilipih alternatif menggunakan ansible. 
selain kemudahan dalam me-manage banyaknya perangkat, untuk terkomunikasi ke berbagai perangkat cukup mudah karena ansible berkomunikasi dengan perangkat tsb melalui ssh (port standart ssh: 22).

## Ikuti cara settingnya
first thing first, ansible telah terinstall dan siap digunakan. arti siap digunakan adalah ansible sudah dapat dikonfigurasi sesuai kebutuhan serta dependensi atau library pendukung telah terpasang. 
ada 3 tahap untuk mengkonfigurasi ansible. setting inventory, setting playbook dan eksekusi playbook dan inventory dengan perintah yang sesuai kebutuhan. 

NB: inventory, playbook adalah bahasa yang umum digunakan dalam ansible, apabila masih belum familiar, kita bisa kembali ke pengenalan ansbile pada <a href="https://docs.ansible.com/"> dokumentasi resmi ansible</a>

ansible yang digunakan adalah versi 2.10.8 dengan config file tersetting di /etc/ansible/ansible.cfg

### Tahap pertama : setting inventory
untuk setting inventory, kita butuh ip atau hostname managed node. managed node di proyek ini adalah swith cisco dengan range ip 10.10.0.1 hingga 10.10.0.40. disini ada ketidak cocokan data antar jumlah managed node switch cisco dengan range ip tsb, karena dalam range ip tsb belum sepenuhnya termanage oleh perangkat artinya beberapa ip masih belum digunakan ke dalam perangkat. untuk mempersingkat waktu dalam membuat inventory, maka digunakan range ip tsb saja. 
dengan menamai file inventory dengan invcisco.ini pada penampakan gambar berikut

```bash
[sw-cisco:children]
sw-cisco-1-40
ipr-swa-km38-38

[sw-cisco-1-40]
10.10.0.[1:40]

[ipr-swa-km38-38]
10.10.0.38

[sw-cisco:vars]
ansible_user=user-cisco-kalian
ansible_password=password-cisco-kalian
ansible_connection=network_cli
ansible_network_os=ios
```
  > ansible_user dan ansible_password disesuaikan dengan user atau password masing masing device kalian ya. 

kita bedah satu persatu ya arti kode diatas.. 

```bash
[sw-cisco:children]
sw-cisco-1-40
ipr-swa-km38-38
```
artinya kita membuat penamaan [sw-cisco] untuk children atau anak dengan nama sw-cisco-1-40 dan ipr-swa-km38-38.

dimana sw-cisco-1-40 adalah perangkat cisco yang memiliki ip dengan range dari 10.10.0.1 hingga 10.10.0.40 dan ipr-swa-km38-38 adalah perangkat cisco yang memiliki ip 10.10.0.38 spt gambar dibawah
```bash
[sw-cisco-1-40]
10.10.0.[1:40]

[ipr-swa-km38-38]
10.10.0.38
```

lalu pada penamaan sw-cisco kita berikan variable user, password dan koneksi serta network os sesuai perangkat yang dimiliki spt gambar dibawah.. 
```bash
[sw-cisco:vars]
ansible_user=user-cisco-kalian
ansible_password=password-cisco-kalian
ansible_connection=network_cli
ansible_network_os=ios
```

### Tahap kedua : setting playbook
buat file .yaml dengan isi berikut untuk mengeksekusi tugas mengirim log ke log trap server dengan level severity errors
```bash
- name: log-trap-to-all-sw
  hosts: sw-cisco-1-40
  tasks:
   - name: execute
     ios_logging:
       dest: trap
       level: errors
```

mari kita bedah satu per satu kode diatas..

``bash
- name: log-trap-to-all-sw
```
kita membuat perintah dengan nama log-trap-to-all-sw

```bash
  host: sw-cisco-1-40
```
perintah tsb akan di eksekusi pada inventory mana saja, tentu iventory yang kita telah buat sebelumnya pada tahap pertama dengan nama sw-cisco-1-40

```bash
  tasks:
   - name: execute
     ios_logging:
       dest: trap
       level: errors
```
peritah ini berisi nama task dengan task ios_logging menggunakan variabel destinasi atau kebutuhannya: trap dan level atau severity (tingka keparahan): error

### Tahap ketiga : eksekusi perintah playbook dan inventory
lanjut tahap terakhir yaitu perintah eksekusinya. kita menggunakan perintah berikut 
```bash
 ansible-playbook /etc/.../logging-trap-errors-cisco.yaml -i /etc/.../invcisco.ini
```

artinya kita menjalankan perintah ansible dengan playbook pada file di lokasi /etc/.../logging-trap-errors-cisco.yaml dan di eksekusi inventory node pada file di lokasi /etc/.../invcisco.ini . maka hasil yang muncul sebagai berikut : 

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/log%20trap%2001.png" alt="Logtrap-01">
  </a>
  <i>tampilan eksekusi perintah ansible log trap error dari atas ke bawah (1/5)</i>
</p>

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/log%20trap%2002.png" alt="Logtrap-01">
  </a>
  <i>tampilan eksekusi perintah ansible log trap error dari atas ke bawah (2/5)</i>
</p>

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/log%20trap%2003.png" alt="Logtrap-01">
  </a>
  <i>tampilan eksekusi perintah ansible log trap error dari atas ke bawah (3/5)</i>
</p>

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/log%20trap%2004.png" alt="Logtrap-01">
  </a><br>
  <i>tampilan eksekusi perintah ansible log trap error dari atas ke bawah (4/5)</i>
</p>

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/log%20trap%2005.png" alt="Logtrap-01">
  </a>
  <i>tampilan eksekusi perintah ansible log trap error dari atas ke bawah (5/5)</i>
</p>

## Konklusi
dengan menggunakan ansible, dokumentasi pekerjaan menjadi lebih ringan. adapun ansible tower lebih mempermudah operasional dengan fitur yang diberikan, tapi perlu di kaji ulang untuk menggunakan ini karena ansible tower membutuhkan biaya supaya dapat terimplementasi.

## Next proyek
sebagai alternatir, untuk mendapatkan salah satu fitur asible tower yaitu rolebase access control next proyek kita akan mengkolaborasikan ansible dengan gitlab dengan enviroment tertutup (lokal) atau beroperasi tanpa koneksi ke internet. 

<a href="https://github.com/mindatama/tanampadi">ke beranda tanampadi</a>