# Proyek ketiga
adalah membuat configurasi dengan ansible untuk mengatur log trap server tertentu dan mengirim severity sesuai kebutuhan pada beberapa perangkat cambium secara langsung. <br>

## Kenapa Cambium dengan ansible
karena dengan banyaknya perangkat cambium sebagai wireless backhaul ataupun point to point dan point to multi point, maka untuk mengantisipasi recovery lebih cepat ketika terjadi kendala hingga perangkat mengalami mati. backup sendiri juga berfungsi sebagai review setting ketika dianggap ada setting yang tidak sesuai standart akan di review kembali setting pada perangkat tsb dengan eviden file backup tersebut.

## Manfaat
tentu dengan satu perintah ansible playbook yang sebelumnya telah kita setting dapat meningkatkan produktifitas dalam menjalankan aktifikas backup konfigurasi perangkat switch cisco lebih efisien. pun semakin bertambahnya perangkat yang di manage maka semakin efisien hasil yang diperoleh.

## Ikuti langkah dan settingnya
langkah awal adalah memastikan ansible telah terinstall dan berjalan dengan lancar (siap digunakan). berikut langkah