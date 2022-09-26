## Tugas 2 Pemerosesan Citra Digital
Nama   : Sesilia Miranda<br>
Nim    : 2110131220010


<h2 align="center">STRUKTUR SISTEM OPERASI</h2>
<hr>

<p align = "justify">Sebuah sistem yang besar dan kompleks seperti sistem operasi modern harus diatur dengan cara membagi task kedalam komponen-komponen kecil agar dapat berfungsi dengan baik dan mudah dimodifikasi. Pada bab ini, kita akan membahas cara komponen-komponen ini dihubungkan satu sama lain. Menurut Silberschatz dan kawan-kawan, ada tiga cara yaitu:</p>

- Struktur Sederhana.
- Pendekatan Berlapis.
- Kernel Mikro.

<p align = "justify">Sedangkan menurut Stallings, kita bisa memandang sistem sebagai seperangkat lapisan. Tiap lapisan menampilkan bagian fungsi yang dibutuhkan oleh sistem operasi. Bagian yang terletak pada lapisan yang lebih rendah akan menmpilkan fungsi yang lebih primitif dan menyimpan detail fungsi tersebut.</p>

### System Monolitic (Struktur Sederhana)

<p align = "justify">System monolitik ini berisikan kumpulan dari berbagai prosedur yang dapat dipanggil oleh persedur lainnya untuk menjalankan sistem. Sehingga antar prosedur dapat saling bekerja sama dalam menjalankan sebuah sistem.</p>

<p align = "justify">Beberapa sistem komersial lebih berfokus pada menyediakan fungsional yang lebih sedikit dan tidak bisa dibagi dalam beberapa modul dan masih belum memiliki stuktur yang cukup baik. Kondisi ini menyebabkan sistem operasi yang digunakan cukup sederhana, kecil, dengan beberapa keterbatasan. Dua contoh sistem tersebut adalah MS DOS dan UNIX, dengan ciri khas :</p>

- MS DOS = fokus pada fungsional tertentu dan tidak dapt dibagi dalam beberapa modul.
- UNIX = fokus pada setiap prosedur yang memanggil prosedur lainnya, sehingga menyebabkan tiap prosedur dapat saling berkomunikasi dan kernel berisikan semua layanan yang disediakan oleh sistem ke pengguna.

<p align = "justify">Walaupun mudah digunakan, struktur monolitik memiliki kekurangan yang cukup berbahaya. Program-program malware dapat mudah memodifikasi sistem dan merusak keseluruhan sistem operasi yang anda gunakan.</p>

<p align = "justify">Selain itu, struktur ini dapat menyebabkan pemborosan jika setiap kernelnya harus menjalankan kernel monolitik yang sangat besar. Perlu diingat juga bahwa satu saja kesalahan pemrograman dari salah satu bagian kernel dapat menyebabkan matinya keseluruhan sistem monolitik yang digunakan.</p>

### Layered System (Sistem Berlayer)

<p align = "justify">Sistem operasi berlapis memiliki beberapa lapis yang beragam, mulai dari bagian atas hingga bagian bawah. Masing-masing lapisan ini memiliki fungsi dan tujuannya tersendiri yang saling mendukung satu sama lain. Lapisan paling bawah digunakan untuk perangkat keras, sedangkan lapisan paling atas digunakan untuk user interface.</p>

<p align = "justify">Sistem berlapis banyak digunakan karena dapat mengurangi kompleksitas rancangan dari implementasi sebuah sistem operasi. Setiap lapisan struktur tersebut berasal dari hasil implementasi objek abstrak.</p>

<p align = "justify">Kondisi ini menyebabkan hasil implementasi berasal dari data yang terenkapsulasi dan operasi yang dapat dimanipulasi. Salah satu contoh struktur sistem berlapis adalah The System.</p>

<p align = "justify">Setiap lapisan layer dari struktur tersebut merupakan hasil implementasi dari objek abstrak. Dimana hasil implementasi tersebut merupakan enkapsulasi data dan operasi yang bisa dimanipulasi. Agar lebih jelas, berikut jenis layer yang digunakan dalam sistem operasi:</p>

#### 1. Lapisan Perangkat Keras

<p align = "justify">Lapisan perangkat keras merupakan lapisan paling bawah pada sistem operasi berlapis. Lapisan ini terdiri dari sirkuit elektronik yang berfungsi untuk membersihkan register ataupun membaca lokasi memori, set instruksi pada prosesor, serta interupsi yang berisikan perintah yang dijalankan.</p>

#### 2. Lapisan Sistem Operasi

<p align = "justify">Lapisan sistem operasi merupakan sebuah lapisan yang berhubungan secara langsung dengan program spesifik pada bagian sistem operasinya.</p>

<p align = "justify">Lapisan ini memiliki kerja yang bersifat teknis dan terdiri dari penyimpanan sekunder komputer, ide dalam eksekusi program, dan lamat logic dari setiap proses yang berlangsung. Kode program sangat diperlukan pada lapisan ini agar dapat terlaksanakan dengan benar dan sesuai dengan yang diharapkan.</p>

#### 3. Lapisan Kelengkapan

<p align = "justify">Lapisan kelengkapan masih berhubungan dengan program karena termasuk dari kelengkapan sebuah sistem operasi. Lapisan ini memiliki tugas utama sebagai pengaturan komunikasi informasi yang berlangsung, termasuk menerima pesan-pesan dan proses pengirimannya.</p>

<p align = "justify">Lapisan ini juga memiliki tugas dalam penyimpanan jangka panjang, menyediakan akses pada perangkat keras eksternal yang menggunakan user interface standar, dan bertanggung jawab dalam hubungan identifier internal atau eksternal.</p>

#### 4. Lapisan Program Aplikasi

<p align = "justify">Lapisan program aplikasi bertujuan untuk menghubungkan pengguna dengan aplikasi yang digunakan, dimana sangat berhubungan erat dengan user interface. Lapisan inin akan memproses segala informasi yang dibutuhkan oleh pengguna dalam aplikasi.</p>

### Kernel Mikro

<p align = "justify">Kernel mikro adalah sistem operasi yang mempermudah komunikasi antara program klien dengan beragam layanan pada ruang user.</p>

<p align = "justify">Komunikasi yang terjadi antar module user menggunakan passing massage. Kernel mikro dapat memperluas sistem operasi dan mudah diatur jika ada transformasi ke arsitektur yang baru. Kode program yang digunakan pada sistem ini juga lebih kecil dan lebih aman.</p>

<p align = "justify">Beberapa manfaat yang dapat anda terima dari struktur sistem mikro kernel adalah :</p>

- Mudah untuk dikembangkan
- Mudah untuk porting sistem operasi ke arsitektur baru
- Mudah diandalkan
- Hanya menggunakan sedikit kode
- Lebih aman

<p align = "justify">Walaupun demikian, struktur sistem mikro kernel sering mengalami overhead kinerja dari komunikasi ruang ke pengguna ruang kernel. Pastikan anda sudah mempertimbangkan kekurangan ini sebelum menerapkan struktur sistem mikro kernel.</p>

<p align = "justify">Beberapa sistem operasi yang menerapkan mikro kernel adalah :</p>

- Tru64 UNIX
- MacOSX
- QNX