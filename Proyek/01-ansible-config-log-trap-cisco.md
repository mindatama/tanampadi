# Proyek pertama 
adalah membuat konfigurasi kode dengan menggunakan ansible. perangkat yang di manage adalah swith cisco berjumlah kurang lebih 28 perangkat. diberikan perintah untuk mengirim log ke log trap server dengan level severity errors.<br>

## Kenapa ansible
dengan banyaknya perangkat network yang di manage, akan sangat memakan waktu ketika perangkat makin bertambah. untuk mempersingkat sumber daya (tenaga dan waktu) maka dilipih alternatif menggunakan ansible. 
selain kemudahan dalam me-manage banyaknya perangkat, untuk terkomunikasi ke berbagai perangkat cukup mudah karena ansible berkomunikasi dengan perangkat tsb melalui ssh (port standart ssh: 22).

## Ikuti cara settingnya
first thing first, ansible telah terinstall dan siap digunakan. arti siap digunakan adalah ansible sudah dapat dikonfigurasi sesuai kebutuhan serta dependensi atau library pendukung telah terpasang. 
ada 3 tahap untuk mengkonfigurasi ansible. setting inventory, setting playbook dan eksekusi playbook dan inventory dengan perintah yang sesuai kebutuhan. 

NB: inventory, playbook adalah bahasa yang umum digunakan dalam ansible, apabila masih belum familiar, kita bisa kembali ke pengenalan ansbile pada <a href="https://docs.ansible.com/"> dokumentasi resmi ansible</a>

ansible yang digunakan adalah versi 2.10.8 dengan config file tersetting di /etc/ansible/ansible.cfg

### Tahap pertama : setting inventory
untuk setting inventory, kita butuh ip atau hostname managed node. managed node di proyek ini adalah swith cisco dengan range ip 10.10.0.1 hingga 10.10.0.40. disini ada ketidak cocokan data antar jumlah managed node switch cisco dengan range ip tsb, karena dalam range ip tsb belum sepenuhnya termanage oleh perangkat artinya beberapa ip masih belum digunakan ke dalam perangkat. untuk mempersingkat waktu dalam membuat inventory, maka digunakan range ip tsb saja. 


### Tahap kedua : setting playbook


### Tahap ketiga : eksekusi perintah playbook dan inventory


<a href="https://github.com/mindatama/tanampadi">ke beranda tanampadi</a>