<p align="center">
  <a href="https://github.com/mindatama/tanampadi">
    <img src="https://github.com/mindatama/tanampadi/blob/main/img/WM.png" alt="Master">
  </a>
</p>

# Tanampadi
ini adalah proyek Wijatmoko Mindatama (Koko) untuk memberikan ilmu kepada seluruh orang tentang teknologi khususnya yang di kuasai oleh penulis sendiri. teknologi yang di kuasai dalam lingkup sysadm, network, iot dan proyek yang telah dikerjakan. dalam menulis proyek ini, Koko tergerak dari <a href="https://github.com/trimstray/the-book-of-secret-knowledge">the book secret kowledge</a>. sambil menunggu dirilisnya <a href="https://mindatama.com">mindatama.com</a> (undercontruction) yang mengakomodir kebutuhan proyek ini, dibuatlah repo github tanampadi sebagai alternatif post.

## Kenapa tanampadi
menganut filosofi padi sebagai bahan makanan pokok sebagian besar penduduk indonesia bahkan di Asia, dengan menanam padi dapat memberikan manfaat bagi khalayak umum dan menghasilkan sesuatu yang memiliki nilai di dalamnya.


## :key: &nbsp;Daftar Isi

Bab Utama:

- **[Sysadm](#Sysadm-DaftarIsi)**
- **[Network](#network-DaftarIsi)**
- **[Proyek](#proyek-DaftarIsi)**
- **[sertifikat](#Sertifikat-DaftarIsi)**
<!-- - **[webdev](#webdev-DaftarIsi)**
- **[IOT](#iot-DaftarIsi)** -->


## &nbsp;Tanampadi (Isi tiap Bab)

#### Sysadm &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)

##### :black_small_square: System Operasi

<p>
&nbsp;&nbsp; <a href="https://www.server-world.info/en/"><b>refrensi instalasi server</b></a> dengan menggunakan berbagai sistem operasi. linux, windows, freebsd<br>
&nbsp;&nbsp; <a href="https://www.linux.org/"><b>Ubuntu Server/ Debian</b></a> distro dari linux OS yang dirancang untuk penggunaan pada server.<br>
&nbsp;&nbsp; <a href="https://www.microsoft.com/en-us/windows-server"><b>Windows Server</b></a> adalah sistem operasi yang dikembangkan oleh microsoft untuk digunakan pada server.<br><br>
</p>

##### :black_small_square: Virtual Machine

<p>
&nbsp;&nbsp; <a href="https://vm.ibm.com/education/roadmaps/all.html"><b>referensi VM</b></a> dengan pengenalan dasar virtual machine. sebelum jauh melangkah, alasan dibalik adanya virtual machine adalah kebutuhan akan running berbagai service (aplikasi) di dalam satu enviroment dalam server bare metal. dengan munculnya vm, tiap service dijalankan pada enviroment terpisah dalam server bare metal. cara kerja vm adalah membagi resource bare metal sehingga dapat mengakomodir kebutuhan berbagai service dengan enviroment terpisah antar service.<br>
pada virtual machine terdapat hypervisor untuk memisahkan sumber daya server bare metal dan menjalankan service dengan enviroment terpisah.. <br>
&nbsp;&nbsp; <a href=""><b>hypervisor type 1 (bare metal)</b></a> berjalan langsung di bare metal tanpa membutuhkan OS untuk menjalankan servicenya. <br>
&nbsp;&nbsp; <a href=""><b>hypervisor type 2 (Hosted)</b></a> berjalan sebagai aplikasi yang membutuhkan OS. contoh virtualbox<br>
</p>

##### :black_small_square: Infrastruktur Monitoring

<p>
&nbsp;&nbsp; setelah berjalan, aplikasi yang telah terinstall perlu maintenance infrastruktur yang ada dengan salah satu cara monitoring. berbagai tools monitoring yang dapat di implementasikan untuk memudahkan provide pelayanan.<br>
&nbsp;&nbsp; salah satu tools yang digunakan yaitu <a href="https://www.solarwinds.com/network-performance-monitor"><b>solarwind</b></a> <br>
&nbsp;&nbsp; berikutnya <a href="https://www.solarwinds.com/kiwi-syslog-server"><b>kiwi log server</b></a> adalah produk turunan dari solarwind yang memiliki service log trap atau pengumpul log dari berbagai perangkat. log yang di kumpulkan memiliki berbagai severity atau tingkat keparahan dan data log tsb di gunakan untuk melakukan troubleshot pada perangkat yang mengirim log<br>
</p>

##### :black_small_square: Versioning Control system

<p>
&nbsp;&nbsp; digunakan untuk merekam perubahan file dari waktu ke waktu sehingga dapat melihat kembali perubahan dari sebelumnya (ke versi tertentu). version control juga dapat digunakan untuk berkolaborasi antar pengguna di proyek yang sama. tools version control berikut:<br>
&nbsp;&nbsp; <a href="https://git-scm.com"><b>Git</b></a> <br>
&nbsp;&nbsp; <a href="https://github.com"><b>Github</b></a> <br>
&nbsp;&nbsp; <a href="https://about.gitlab.com"><b>Gitlab</b></a> <br>
</p>

##### :black_small_square: Apps Pendukung

<p>
&nbsp;&nbsp; <a href=""><b>Low level design & High level design</b></a> <br>
&nbsp;&nbsp; <a href="https://docs.ansible.com/"><b>Ansible</b></a> <br>
&nbsp;&nbsp; <a href="https://www.veeam.com/"><b>Veeam Backup</b></a> <br>
&nbsp;&nbsp; <a href="https://www.cyberark.com/products/remote-access/"><b>PAM remote access cyberark</b></a> <br>
&nbsp;&nbsp; <a href="https://phpipam.net/"><b>PHPipam</b></a> <br>
&nbsp;&nbsp; <a href="https://www.synology.com/en-uk"><b>NAS</b></a> atau network attach storage adalah <br>
&nbsp;&nbsp; <a href="https://documentation.solarwinds.com/"><b>Solarwind</b></a> <br>
&nbsp;&nbsp; <a href="https://thwack.solarwinds.com/products/kiwi-syslog/"><b>Kiwi Syslog</b></a> <br>
</p>

#### Network &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)

##### :black_small_square: Dasar Network

<p>
&nbsp;&nbsp; <a href="https://www.youtube.com/watch?v=dV8mjZd1OtU"><b>OSI layer</b></a> <br>
&nbsp;&nbsp; <a href=""><b>MAC Adress</b></a> <br>
&nbsp;&nbsp; <a href="https://www.youtube.com/watch?v=F5rni9fr1yE"><b>IP Address</b></a> <br>
&nbsp;&nbsp; <a href="https://www.linuxjournal.com/article/6287"><b>subnetting</b></a> <br>
&nbsp;&nbsp; <a href=""><b>IP protocol</b></a> <br>
&nbsp;&nbsp; <a href="https://www.idn.id/configure-and-verify-virtual-local-area-network-vlans/"><b>VLAN</b></a><br>
&nbsp;&nbsp; <a href="https://www.idn.id/overview-static-dynamic-routing/"><b>routing</b></a><br>
&nbsp;&nbsp; <a href=""><b>DNS</b></a><br>
&nbsp;&nbsp; <a href=""><b>wireless</b></a><br>
</p>


<!-- #### Webdev &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)

<p>
&nbsp;&nbsp; <a href=""><b>materi pertama</b></a><br><br>
&nbsp;&nbsp; <a href=""><b>materi kedua</b></a><br><br>
&nbsp;&nbsp; <a href=""><b>materi ketiga</b></a><br><br>
</p>

#### IOT &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)<br>

<p>
&nbsp;&nbsp; <a href=""><b>materi pertama</b></a><br><br>
&nbsp;&nbsp; <a href=""><b>materi kedua</b></a><br><br>
&nbsp;&nbsp; <a href=""><b>materi ketiga</b></a><br><br>
</p> -->

#### Proyek &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)

<p>
&nbsp;&nbsp; Proyek pertama adalah <a href="https://github.com/mindatama/tanampadi/blob/main/Proyek/01-ansible-config-log-trap-cisco.md"><b>membuat konfigurasi kode</b></a> dengan menggunakan ansible. perangkat yang di manage adalah swith cisco berjumlah kurang lebih 28 perangkat. diberikan perintah untuk mengirim log ke log trap server dengan level severity errors.<br>
<br>
&nbsp;&nbsp; Proyek kedua masih sama dengan tools yang sama menggunakan ansible namun dengan pemanfaatan berbeda. proyek sebelumnya <a href="https://github.com/mindatama/tanampadi/blob/main/Proyek/01-ansible-config-log-trap-cisco.md"><b>membuat konfigurasi kode</b></a> namun proyek kedua ini <a href="https://github.com/mindatama/tanampadi/blob/main/Proyek/02-ansible-config-backup-cisco.md"><b>membuat backup configurasi</b></a> perangkat switch cisco berjumlah kurang lebih 28 perangkat. diberikan perintah untuk membackup konfigurasi ke dalam file dan menyimpannya dalam folder yang telah ditentukan.<br>
</p>
<p>
&nbsp;&nbsp; Proyek ketiga masih sama lagi dengan tools ansible namun dengan pemanfaatan berbeda. membuat configutasi backup dengan perangkat lain, cambium wireless. dan harus tertunda dahulu karena dari sumber yang ada ansible hanya mengcover switch dan router, belum merambah ke access point os.
</p>
<br>

#### Sertifikat &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)
<br>
&nbsp;&nbsp; pada materi linux fondation, akan diberikan informasi mengenai komponen pembentuk linux. komponen inti yaitu kernel, sebagai jembatan penghubung hardware dan software untuk menjalankan fungsi dan memproses perintah. ada 3 (distribusi linux) turunan utama dari kernel, debian yang memiliki cabang ubuntu. rhel (red hat enterprise linux) cabang centos dan fedora. dan suse dengan turunan sles dan open suse. serta banyak turunan lainnya. <br>