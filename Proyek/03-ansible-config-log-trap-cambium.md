# Proyek ketiga
adalah membuat configurasi dengan ansible untuk mengatur log trap server tertentu dan mengirim severity sesuai kebutuhan pada beberapa perangkat cambium secara langsung. <br>

## Kenapa Cambium dengan ansible
karena dengan banyaknya perangkat cambium sebagai wireless backhaul ataupun point to point dan point to multi point, maka untuk mengantisipasi recovery lebih cepat ketika terjadi kendala hingga perangkat mengalami mati. backup sendiri juga berfungsi sebagai review setting ketika dianggap ada setting yang tidak sesuai standart akan di review kembali setting pada perangkat tsb dengan eviden file backup tersebut.

## Manfaat
tentu dengan satu perintah ansible playbook yang sebelumnya telah kita setting dapat meningkatkan produktifitas dalam menjalankan aktifikas backup konfigurasi perangkat switch cisco lebih efisien. pun semakin bertambahnya perangkat yang di manage maka semakin efisien hasil yang diperoleh.

## Ikuti langkah dan settingnya
langkah awal adalah memastikan ansible telah terinstall dan berjalan dengan lancar (siap digunakan). berikut langkah. ada 3 tahap untuk mengkonfigurasi ansible. setting inventory, setting playbook dan eksekusi playbook dan inventory dengan perintah yang sesuai kebutuhan. 

NB: inventory, playbook adalah bahasa yang umum digunakan dalam ansible, apabila masih belum familiar, kita bisa kembali ke pengenalan ansbile pada <a href="https://docs.ansible.com/"> dokumentasi resmi ansible</a>

ansible yang digunakan adalah versi 2.10.8 dengan config file tersetting di /etc/ansible/ansible.cfg

### Tahap pertama : setting inventory
untuk setting inventory, kita butuh ip atau hostname managed node. managed node di proyek ini adalah access point cambium.
langkah awal adalah memastikan ansible telah terinstall dan berjalan dengan lancar (siap digunakan). 

### Tahap kedua : setting playbook
tahap kedua ini

### Tahap ketiga : eksekusi 

### Kesimpulan 