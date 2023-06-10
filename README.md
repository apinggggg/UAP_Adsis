# UAP_Adsis

Nama	: Muhammad Hafizh Adhyaksa

NIM	: 215150707111019

Tugas UAP Administrasi TI-E

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP1.1.png" >
</p>


Jawaban

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP1.1.png" >
</p>
<p align="center">Gambar 1.1</p>


<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP1.2.png" >
</p>
<p align="center">Gambar 1.2</p>



<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP1.3.png" >
</p>
<p align="center">Gambar 1.3</p>


`	`**Penjelasan :**

Membuat direktori dengan nama **UAP-Adsis** dengan menggunakan perintah **mkdir,** kemudian membuat file dengan nama **catatanya-hafizh.txt** dengan menggunakan perintah **touch.** Lalu pada isi file tersebut menuliskan nama dan NIM sesuai dengan perintah yang ada pada soal. Kemudian save file dengan menekan **CTRL + X,** lalu klik **Yes** dan **Enter.** Selanjutnya mengatur permission menjadi view only untuk user dengan menjalankan perintah **sudo chmod 400 <Nama File>.** Kemudian kita bisa mengecek apakah file tersebut sudah berubah menjadi view only dengan menjalankan perintah **ls -l.**

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP2.1.png" >
</p>
<p align="center">Gambar 2.1</p>



**Penjelasan :**

Sebelum Melakukan Konfigurasi, saya mengecek antarmuka jaringan mana yang akan saya ubah IP nya, lalu saya melakukan konfigurasi pada ens33 dengan IP sebelumnya 192.168.86.128 menjadi 192.168.56.**17** dengan menjalankan perintah **sudo ifconfig ens33 192.168.56.17**.** angka 17 pada IP terakhir merupakan nomor absen saya pada kelas administrasi TI-E. kemudian setelah selesai melakukan konfigurasi pada IP selanjutnya mengkonfigurasi Default Gateway dengan menjalankan perintah **sudo route add default gw 192.168.56.17.** Selanjutnya untuk mengecek default gatewaynya sudah berubah atau belum dapat menjalankan perintah **sudo route -n.**



<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP3.1.png" >
</p>
<p align="center">Gambar 3.1</p>

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP3.2.png" >
</p>
<p align="center">Gambar 3.2</p>


<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP3.3.png" >
</p>
<p align="center">Gambar 3.3</p>

**Penjelasan :**

Pada webmin terdapat pilhan **System** kemudian didalamnya terdapat pilihan **User and Grup.** Lalu dapat dilihat pada gambar 3.1 saya membuat user pada webmin dengan nama **Hafizh**, selanjurnya pada gambar 3.2 saya membuat grup dengan nama **Adsis\_TI-E.** pada gambar 3.3 dapat terlihat bahwa user dengan nama **hafizh** sudah masuk kedalam grup dengan nama **Adsis\_TI-E**


<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP4.1.png" >
</p>
<p align="center">Gambar 4.1</p>

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP4.2.png" >
</p>
<p align="center">Gambar 4.2</p>

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP4.3.png" >
</p>
<p align="center">Gambar 4.3</p>

**Penjelasan :**

Saya melakukan ping ke IP yang sebelumnya telah saya konfigurasikan menjadi IP 192.168.56.17 yang dapat dilihat pada gambar 4.1 dan berhasil melakukan ping. Kemudian selanjutnya pada bagian menu networking terdapat linux firewall lalau saya lakukan add rule **drop dan reject** dengan network protocol ICMP lalu lakukan apply konfigurasi yang dapat dilihat pada gambar 4.2. selanjutnya pada gambar 4.3 saya melakukan ping Kembali ke IP 192.168.56.17 dan hasilnya adalah gagal melakukan ping yang dikarenakan setelah melakukan reject dan drop artinya sistem menolak paket untuk mencapai sistem ubuntu karena terjadi pemblokiran pada protocol ICMP yang digunakan untuk melakukan ping.


<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP5.1.png" >
</p>
<p align="center">Gambar 5.1</p>

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP5.2.png" >
</p>
<p align="center">Gambar 5.2</p>

<p align="center">
  <img src="https://github.com/apinggggg/UAP_Adsis/blob/main/Images/UAP5.3.png" >
</p>
<p align="center">Gambar 5.3</p>

**Penjelasan :**

Pada gambar 5.1 saya menjalankan perntah sudo **crontab -e** dimana perintah ini untuk mengatur jadwal tugas otomatis (cron jobs) pada sistem operasi Linux. Kemdian saya melakukan konfigurasi pada /tmp/crontab.TNKjJ9/crontab dengan memasukan **\*/2 \* \* \* \* ping filkom.ub.ac.id**. Selanjutnya saya menjalankan perintah **ps aux | grep ping** untuk menampilkan daftar proses yang sedang berjalan di sistem Linux yang terkait dengan kata kunci "ping" dimana nanti setiap 2 menit akan melakukan ping otomatis ke filkom.ub.ac.id seperti yang ada pada gambar 5.3


