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
&nbsp;&nbsp; Proyek ketiga masih sama lagi dengan tools ansible namun dengan pemanfaatan berbeda. membuat configutasi backup dengan perangkat lain, cambium wireless. dan harus tertunda dahulu karena dari sumber yang ada ansible hanya mengcover switch dan router, belum merambah ke access point os.<br>
kesimpulan dari proyek ketiga belum dapat diimplementasikan karena ansible belum merambah ke os AP di cambium. untuk produk cambium yang sdh tcover adalah switch cambium. 
</p>
<br>

#### Sertifikat &nbsp;[<sup>[DaftarIsi]</sup>](#key-daftar-isi)
<br>
&nbsp;&nbsp; pada materi linux fondation, akan diberikan informasi mengenai komponen pembentuk linux. komponen inti yaitu kernel, sebagai jembatan penghubung hardware dan software untuk menjalankan fungsi dan memproses perintah. ada 3 (distribusi linux) turunan utama dari kernel, debian yang memiliki cabang ubuntu. rhel (red hat enterprise linux) cabang centos dan fedora. dan suse dengan turunan sles dan open suse. serta banyak turunan lainnya. <br> 
&nbsp;&nbsp; hal pertama adalah menginstall linux di laptop atau komputer yang dipakai, karena akan banyak tugas yang membutuhkan os linux. instalasi os linux dapat install langsung ke perangkat atau menggunakan virtual machine. pilih distro yang akan digunakan. <br>
terdapat 3 distribution family pada linux yaitu: redhat, debian dan suse. <br>
ketika menelusuri terminologi linux, kita akan bertemu dengan istilah yang kurang familiar berikut<br>
<p>
&nbsp;&nbsp; Kernel adalah penghubung antara hardware dan aplikasi contoh linux kernel <br><br>
&nbsp;&nbsp; distribution atau distro adalah kumpulan software yang membentu sebuah OS linux dasar contoh redhat enterprise linux, fedora, ubuntu dan gentoo<br><br>
&nbsp;&nbsp; boot loader adalah program yang menjalankan OS contoh: GRUB, ISOLINUX
&nbsp;&nbsp; service aadalah program yang berjalan di background process. init : httpd (web server), ftpd (ftp server), named (name server), dhcpd (dhcp server) <br><br>
&nbsp;&nbsp; filesystem adalah metode untuk storing dan organize file, contoh: ext3, ext4, fat, xfs dan btrfs <br><br>
&nbsp;&nbsp; X window system adalah sistem penyedia tools standart dan protokol untuk membangun grafic user interface di hampir seluruh sistem linux. contoh: gui= desktop (kde,gnome,xfce) ; windows manager ; x windows system/ x11. console= cli/shell ; kernel ; hardware <br><br>
&nbsp;&nbsp; desktop enviroment adalah gui (grafical user interface) dalam os, contoh: gnome, kde, xfce, fluxbox<br><br>
&nbsp;&nbsp; command line adalah interface untuk ketik perintah dalam os<br><br>
&nbsp;&nbsp; shell adalah command line interpreter yang menerjemahkan masukkan dan perintah ke os dan memerintahkan os untuk melaksanakan masukkan dan perintah, contoh: bash, tcsh, zsh<br><br>
</p>
&nbsp;&nbsp; Boot Process<br>
&nbsp;&nbsp; linux boot process adalah prosedur dari daya komputer di hidupkan hinga user interface siap beroperasi. <br>
power on - BIOS (basic input output system)- Master boot record (MBR) atau EFI partition - boot loader (GRUB) - kernel - initial RAM disk (initramfs) - /sbin/init (proses awal) - command shell pakai getty - GUI (x window atau wayland).<br>
<p>
BIOS - langkah awal <br>
ketika linux menjalankan banyak hardware termasuk layar dan keyboard, dan test memory utama. proses ini juga disebut POST (power of self test). BIOS software tersimpan pada ROM (read-only memory) chip pada motherboard. selanjutnya, sisa boot process di kontrol oleh OS. 
</p>
<p>
MBR - Master Boot Record, EFI Partition, dan Boot Loader <br>
setelah POST selesai, system control oper dari BIOS ke boot loader. boot loader biasanya tersimpan pada salah satu system milik storage device, hardisk atau ssd drive, salahsatunya di boot sector (untuk BIOS jadul/ MBR system) atau EFI partisi (EFI/UEFI system). dalam tahap ini, mesin tak dapat akses media penyimpanan. lalu informasi tanggal waktu dan periperal penting tersimpan pada CMOS.
</p>
<p>
boot loader yg eksis untuk Linux atau yang paling umum adalah GRUB (GRand Unified Boot loader), ISOLINUX (untuk boot melalui media external) dan DAS U-Boot (untuk booting pada device tanam). ketika booting linux, boot loader bertanggung jawab memuat kernel image dan initial RAM disk atau filesystem<br>
<br><b>gambar bios boot (MBR) vs uefi</b>
</p>
<p>
boot loader memiliki dua tahapan berbeda: <br>
untuk sistem pengguna metode BIOS/MBR, boot loader berada pada sector awal hardisk, besaran MBR hanya 512 bytes. pada tahap ini, boot loader cek partition table dan mencari bootable partisi. ketika ketemu partisi bootable, lanjut cari untuk tahap kedua boot loader, contoh GRUB, dan memuat ke RAM. <br>
untuk system pengguna metode UEFI/EFI, uefi firmware membaca data boot manager untuk memutuskan aplikasi uefi mana yang akan di luncurkan dan dari mana (contoh, dari disk atau partisi mana efi partisi yg diluncurkan dapat ditemukan). firmware lalu meluncurkan uefi aplikasi, contoh grub sebagai boot entry pada firmware boot manager. prosedur ini lebih rumit tapi lebih cakap dari metode MBR yang lebih usang.<br>
tahap kedua boot loader berada pada /boot. splash screen muncul, membolehkan kita untuk memilih OS dan atau kernel untuk di boot. setelah OS dan kernel dipilih, boot loader memuat kernel OS ke RAM dan mengoper control kesana. kernel hampir selalu terkompres, jadi tugas utama sistem ada membuka kompres. lanjut, sistem akan analisa harware dan meng-initialize driver perangkat ke kernel.
</p>