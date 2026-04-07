pada materi linux fondation, akan diberikan informasi mengenai komponen pembentuk linux. komponen inti yaitu kernel, sebagai jembatan penghubung hardware dan software untuk menjalankan fungsi dan memproses perintah. ada 3 (distribusi linux) turunan utama dari kernel, debian yang memiliki cabang ubuntu. rhel (red hat enterprise linux) cabang centos dan fedora. dan suse dengan turunan sles dan open suse. serta banyak turunan lainnya. <br> 
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
</p><br>
<br><b>Initial RAM Disk</b>
</p>
<p>initramfs filesystem image terdapat program dan binary file yang dibutuhkan untuk memuat (mount) root filesystem, termasuk menyediakan kebutuhan kernel untuk filesystem spesifik yang akan digunakan, dan memuat driver device untuk mass storage controllers