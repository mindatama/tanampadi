# Proyek kedua
adalah membuat konfigurasi kode dengan menggunakan ansible. perangkat yang di manage adalah swith cisco berjumlah kurang lebih 28 perangkat. diberikan perintah untuk membuat backup file running config pada cisco.<br>

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
buat file .yaml dengan isi berikut untuk mengeksekusi tugas membuat file backup running konfigurasi dan di simpan ke directory/ folder pada ftp server
```bash
- name: copy backup running-config
  hosts: sw-cisco-1-40
  tasks:
  - name: backup ios config
    cisco.ios.ios_config:
      backup: true
      backup_options:
        filename: ""
        dir_path: /srv/ftp/backup-cisco-config
```

mari kita bedah satu persatu kode diatas.. 

```bash
- name: copy backup running-config
  hosts: sw-cisco-1-40
```
kode ini diartikan kita memberi nama pada eksekusi yang akan di buat akan di eksekusi pada host apa saja. terlihat host yang kita masukkan adalah sw-cisco-1-40

```bash
  tasks:
  - name: backup ios config
    cisco.ios.ios_config:
      backup: true
      backup_options:
        filename: ""
        dir_path: /srv/ftp/backup-cisco-config
```
perintah ini berisi task yang di eksekusi. di atas ada 1 task dengan nama backup ios config mengeksekusi perintah backup dengan file name default bysystem, yaitu ip dan tanggal jam eksekusi, lalu diarahkan ke lokasi folder ftp server di /srv/ftp/backup-cisco-config

### Tahap ketiga : eksekusi perintah playbook dan inventory
lanjut tahap akhir yaitu perintah eksekusi playbook dan inventory

```bash
ansible-playbook /etc/.../playbackup-test.yaml -i /etc/.../invcisco.ini
```
artinya kita menjalankan perintah ansbile dengan playbook pada file di lokasi /etc/.../playbackup-test.yaml dengan inventory pada file di lokasi /etc/.../invcisco.ini maka akan muncul hasil di 5 gambar sambung dibawah

<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/backup%20config%2001.png" alt="Backupconfig-01">
  </a>
  <i>tampilan eksekusi perintah ansible backup config dari atas ke bawah (1/5)</i>
</p>
<br>
<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/backup%20config%2002.png" alt="Backupconfig-01">
  </a>
  <i>tampilan eksekusi perintah ansible backup config dari atas ke bawah (2/5)</i>
</p>
<br>
<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/backup%20config%2003.png" alt="Backupconfig-01">
  </a>
  <i>tampilan eksekusi perintah ansible backup config dari atas ke bawah (3/5)</i>
</p>
<br>
<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/backup%20config%2004.png" alt="Backupconfig-01">
  </a>
  <i>tampilan eksekusi perintah ansible backup config dari atas ke bawah (4/5)</i>
</p>
<br>
<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/backup%20config%2005.png" alt="Backupconfig-01">
  </a>
  <i>tampilan eksekusi perintah ansible backup config dari atas ke bawah (5/5)</i>
</p>
<br>

## Konklusi 
dengan menggunakan ansible, dokumentasi pekerjaan menjadi lebih ringan. ketika dipadukan dengan cronjob di ubuntu dapat membuat otomasi proses yang dimana pekerjaan lebih efisien

<a href="https://github.com/mindatama/tanampadi">ke beranda tanampadi</a>