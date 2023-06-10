# UAP_Adsis

Nama	: Muhammad Hafizh Adhyaksa

NIM	: 215150707111019

Tugas UAP Administrasi TI-E

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.001.jpeg)


Jawaban

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.002.png)![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.003.png)

**Gambar 1.1**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.002.png)![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.004.png)

**Gambar 1.2**



![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.002.png)![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.005.png)

**Gambar 1.3** 

`	`**Penjelasan :**

Membuat direktori dengan nama **UAP-Adsis** dengan menggunakan perintah **mkdir,** kemudian membuat file dengan nama **catatanya-hafizh.txt** dengan menggunakan perintah **touch.** Lalu pada isi file tersebut menuliskan nama dan NIM sesuai dengan perintah yang ada pada soal. Kemudian save file dengan menekan **CTRL + X,** lalu klik **Yes** dan **Enter.** Selanjutnya mengatur permission menjadi view only untuk user dengan menjalankan perintah **sudo chmod 400 <Nama File>.** Kemudian kita bisa mengecek apakah file tersebut sudah berubah menjadi view only dengan menjalankan perintah **ls -l.**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.006.png)

**Gambar 2.1**

**Penjelasan :**

Sebelum Melakukan Konfigurasi, saya mengecek antarmuka jaringan mana yang akan saya ubah IP nya, lalu saya melakukan konfigurasi pada ens33 dengan IP sebelumnya 192.168.86.128 menjadi 192.168.56.**17** dengan menjalankan perintah **sudo ifconfig ens33 192.168.56.17**.** angka 17 pada IP terakhir merupakan nomor absen saya pada kelas administrasi TI-E. kemudian setelah selesai melakukan konfigurasi pada IP selanjutnya mengkonfigurasi Default Gateway dengan menjalankan perintah **sudo route add default gw 192.168.56.17.** Selanjutnya untuk mengecek default gatewaynya sudah berubah atau belum dapat menjalankan perintah **sudo route -n.**



![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.007.png)

**Gambar 3.1**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.008.png)

**Gambar 3.2**



`    `**![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.009.png)**

`  `**Gambar 3.3**

**Penjelasan :**

Pada webmin terdapat pilhan **System** kemudian didalamnya terdapat pilihan **User and Grup.** Lalu dapat dilihat pada gambar 3.1 saya membuat user pada webmin dengan nama **Hafizh**, selanjurnya pada gambar 3.2 saya membuat grup dengan nama **Adsis\_TI-E.** pada gambar 3.3 dapat terlihat bahwa user dengan nama **hafizh** sudah masuk kedalam grup dengan nama **Adsis\_TI-E**


![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.010.png)

**Gambar 4.1**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.011.png)

**Gambar 4.2**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.012.png)

**Gambar 4.3**

**Penjelasan :**

Saya melakukan ping ke IP yang sebelumnya telah saya konfigurasikan menjadi IP 192.168.56.17 yang dapat dilihat pada gambar 4.1 dan berhasil melakukan ping. Kemudian selanjutnya pada bagian menu networking terdapat linux firewall lalau saya lakukan add rule **drop dan reject** dengan network protocol ICMP lalu lakukan apply konfigurasi yang dapat dilihat pada gambar 4.2. selanjutnya pada gambar 4.3 saya melakukan ping Kembali ke IP 192.168.56.17 dan hasilnya adalah gagal melakukan ping yang dikarenakan setelah melakukan reject dan drop artinya sistem menolak paket untuk mencapai sistem ubuntu karena terjadi pemblokiran pada protocol ICMP yang digunakan untuk melakukan ping.


![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.013.png)

**Gambar 5.1**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.014.png)![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.015.png)

**Gambar 5.2**

![](Aspose.Words.7ec84313-4080-485d-ad67-41cc1740f490.016.png)

**Gambar 5.3**

**Penjelasan :**

Pada gambar 5.1 saya menjalankan perntah sudo **crontab -e** dimana perintah ini untuk mengatur jadwal tugas otomatis (cron jobs) pada sistem operasi Linux. Kemdian saya melakukan konfigurasi pada /tmp/crontab.TNKjJ9/crontab dengan memasukan **\*/2 \* \* \* \* ping filkom.ub.ac.id**. Selanjutnya saya menjalankan perintah **ps aux | grep ping** untuk menampilkan daftar proses yang sedang berjalan di sistem Linux yang terkait dengan kata kunci "ping" dimana nanti setiap 2 menit akan melakukan ping otomatis ke filkom.ub.ac.id seperti yang ada pada gambar 5.3


