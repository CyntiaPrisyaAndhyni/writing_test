# WRITING TEST (24-28 Oktober 2022)

## WEB SERVER & RESTFUL API

### Web Server

__Apa Itu Web Server?__

Web server adalah sebuah software (perangkat lunak) yang memberikan layanan berupa data. Berfungsi untuk menerima permintaan HTTP atau HTTPS dari klien atau kita kenal dengan web browser (Chrome, Firefox). Selanjutnya ia akan mengirimkan respon atas permintaan tersebut kepada client dalam bentuk halaman web.

Web Server terdiri dari 2 komponen penting, yaitu:
- Hardware
  Di sisi perangkat keras, web server adalah komputer yang menyimpan perangkat lunak web server dan file komponen situs web. (misalnya, dokumen HTML, gambar, CSS stylesheet, dan file JavaScript) web server terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.
- Software
  Di sisi perangkat lunak, web server mencakup beberapa bagian yang mengontrol bagaimana pengguna web mengakses file yang dihosting. Minimal, ini adalah server HTTP. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser Anda untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir.

![Konsep Web Server](img/web%20server.png)

__Apa Itu Server Side Programming?__

Server web menunggu pesan permintaan klien, memprosesnya saat tiba, dan membalas browser web dengan pesan respons HTTP. Respons berisi baris status yang menunjukkan apakah permintaan berhasil atau tidak (mis. "HTTP/1.1 200 OK" untuk berhasil).

Isi respons yang berhasil atas permintaan akan berisi sumber daya yang diminta (misalnya halaman HTML baru, atau gambar, dll...), yang kemudian dapat ditampilkan oleh browser web.

- Static Sites
  
  ![Static Site Architecture](img/static%20site.png)

  Diagram diatas menunjukkan arsitektur server web dasar untuk static sites (static sites adalah situs yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta). Saat pengguna ingin menavigasi ke halaman, browser mengirimkan permintaan "GET" HTTP yang menentukan URL-nya.

- Dynamic Sites
  Dynamic Sites adalah situs di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan. Di situs web dinamis, halaman HTML biasanya dibuat dengan memasukkan data dari database ke dalam placeholder di template HTML (ini adalah cara yang jauh lebih efisien untuk menyimpan konten dalam jumlah besar daripada menggunakan situs web statis). Berikut ini merupakan arsitektur situs web dinamis:

  ![Dynamic Sites Architecture](img/dynamic%20site.png)

- Perbedaan Static and Dynamic Sites
  - Mereka memiliki tujuan dan perhatian yang berbeda.
  - Mereka umumnya tidak menggunakan bahasa pemrograman yang sama (pengecualiannya adalah JavaScript, yang dapat digunakan di sisi server dan klien).
  - Mereka berjalan di dalam lingkungan sistem operasi yang berbeda.

__Apa saja yang dapat dilakukan di Server-Side?__

- Menyimpan dan mengirim informasi yang efisien
- Menyesuaikan pengalaman pengguna
- Mengontrol akses ke konten
- Menyimpan informasi sesi atau status
- Komunikasi dan notifikasi
- Analisis data


### RESTful API

Rest merupakan arsitektur design untuk membuat web service. Rest memiliki beberapa gaya arsitektur:
- Uniform Interface
- client-server
- Statelessness
- cacheable
- layered system
- Code on Demand (bersifat optional)

RESTful API merupakan API yang menerapkan gaya arsitektur milik Rest.

__Cara Kerja RESTful API__

1. Klien mengirimkan permintaan ke server. Klien mengikuti dokumentasi API untuk memformat permintaan dalam format yang dipahami oleh server.
1. Server mengautentikasi klien dan mengonfirmasi bahwa klien memiliki hak untuk membuat permintaan.
Server menerima permintaan dan memproses secara internal.
1. Server mengembalikan respons kepada klien. Respons berisi informasi yang memberitahu klien jika permintaannya berhasil. Respons juga termasuk informasi apa saja yang diminta klien.

__Isi Permintaan RESTful API Client__

- Identifikasi URL (Uniform Resource Locator) 
  Server mengidentifikasi setiap sumber daya dengan pengidentifikasi sumber daya yang unik. Untuk layanan REST, server biasanya melakukan identifikasi sumber daya dengan menggunakan URL. URL menentukan jalur ke sumber daya. URL mirip dengan alamat situs web yang Anda masukkan ke peramban untuk mengunjungi halaman web mana pun. URL juga disebut titik akhir permintaan dan dengan jelas menentukan server yang dibutuhkan klien.

- Method
  Developer sering mengimplementasikan RESTful API dengan menggunakan Hypertext Transfer Protocol (HTTP). Metode HTTP memberi tahu server hal-hal yang perlu dilakukan terhadap sumber daya. Berikut ini adalah empat metode HTTP umum:
  - GET : mengakses sumber daya yang berada di URL yang ditentukan pada server.
  - POST : mengirim data ke server.
  - PUT/PATCH : memperbarui sumber daya yang ada di server.
  - DELETE : menghapus sumber daya.

__Isi Respons dari RESTful API__
- Baris Status
  Baris status berisi kode status tiga digit yang mengomunikasikan keberhasilan atau kegagalan permintaan. Misalnya, kode 2XX menunjukkan berhasil, tetapi kode 4XX dan 5XX menunjukkan kesalahan. Kode 3XX menunjukkan pengalihan URL.
  Berikut ini adalah beberapa kode status umum:
  - 200: Respons sukses umum
  - 201: Respons sukses metode POST
  - 400: Permintaan salah yang tidak dapat diproses oleh server
  - 404: Sumber daya tidak ditemukan

## INTRO NODE.JS

Node.js merupakan platform JavaScript yang dapat berjalan di backend atau server-side, di komputer kita secara langsung.

__Arsitektur Node.js__

![Arsitektur Node.js](img/arsitektur%20node.png)

- Single Thread
  - Thread dalam ilmu komputer adalah eksekusi menjalankan beberapa tugas atau program secara bersamaan. Setiap unit yang mampu mengeksekusi kode disebut thread.
  - Javascript menggunakan konsep single thread, yang berarti hanya memiliki satu tumpukan panggilan yang digunakan untuk menjalankan program.
  
  ![Single Thread](img/single%20thread.png)

  - Javascript menggunakan call stack untuk melakukan manajemen single thread. Ketika terdapat perintah baru maka akan ditambahkan (push) dan akan di keluarkan ketika perintahnya sudah selasai (pop)


- Event Loop
  - Dengan menggunakan konsep arsitektur javascript, walaupun menggunakan single thread tetapi kita dapat melihat javascript seperti menggunakan multi thread
  - Terdapat event queue yang berguna sebagai penampung ketika terdapat perintah baru yang akan dieksekusi.
  - Event loop akan memfasilitasi kondisi ini, event loop akan memeriksa terus menerus, ketika antrian kosong di call stack maka akan menambah antrian baru dari event queue sampai semua perintah selesai di eksekusi.


- Server side scripting
  - Javascript merupakan bahasa pemrograman yang digunakan di front end side. Sehingga kita hanya bisa mengerjakan javascript dengan menggunakan browser untuk menampilkan hasil eksekusinya. 
  - Dengan menggunakan NodeJS kita dapat menjalankan javascript di server side menggunakan terminal command line menggunakan perintah “node”. 

__Build In Module Node JS__
- Console : digunakan sebagai debug atau menampilkan code secara interface
- Process : digunakan sebagai debug atau menampilkan code secara interface
- OS : digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan user.
- Util : merupakan alat bantu / utilities untuk mendukung kebutuhan internal API di Node JS
- Events
- Errors : digunakan untuk mendefinisikan error di Node JS sehingga lebih informatif. 
- Buffer : digunakan untuk mengakses, mengelola dan mengubah tipe data raw atau tipe data bytes
- FS : untuk membaca file dengan ekstensi .txt, .csv, dan .json
- Timers : digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu

## EXPRESS JS

- Merupakan framework untuk membuat web server.
- Framework yang dibangun diatas Node.js bersifat open-source dan gratis.
- berfungsi untuk membantu pengelolaan aliran data dari server ke aplikasi
- bagian dari MERN, MEAN, MEVN stack (MongoDB, Express, React | Anguler | Vue, NodeJS)

__Install Express__

![install express](img/install%20express.png)

__Basic Routes__

- Routes adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes kita perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan
- Method yang dalam REST API seperti POST, PUT, PATCH dan DELETE
- Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut. Terdapat banyak response yang bisa kita buat selain yang dicontohkan.
- Dalam pengaplikasian back end application, perlu memberikan status code sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.
- Query merupakan parameter yang digunakan untuk membantu menentukan tindakan yang lebih spesifik daripada hanya sekedar router biasa. Biasanya query ditaruh di akhir route dengan memberikan informasi diawali dengan “?” kemudian tedapat key dan data yang dapat ditindak lanjuti. Ex : “?q=hello&age=23”. ExpressJS dapat membaca query menggunakan req.query.
- Nested route digunakan ketika terdapat banyak route yang memiliki nama yang sama atau ingin membuat route yang lebih mendalam


__Middleware__

- Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.
- Cara Kerja
  - Jika pada tahap mana pun middleware function menentukan bahwa suatu HTTP Request adalah request yang buruk dan salah, maka middleware function memiliki kemampuan untuk menghentikan request-response cycle.

  - Berlaku juga sebaliknya, jika middleware function menentukan suatu HTTP Request baik dan benar, maka middleware function memiliki kemampuan untuk melanjutkan request-response cycle ke proses selanjutnya.

  - Setelah sebuah HTTP Request melewati semua middleware yang ada di aplikasi, HTTP Request tersebut akan mencapai handler function — yang, dalam kasus contoh ilustrasi ini, adalah Anda yang menjual minuman lemon (atau, lebih khusus lagi, proses membuat minuman lemon).

  - Setelah sebuah HTTP Request melewati semua middleware yang ada di aplikasi Anda, HTTP Request tersebut akan mencapai handler function — yang, dalam kasus contoh ilustrasi ini, adalah Anda yang menjual minuman lemon (atau, lebih khusus lagi, proses membuat minuman lemon).

  - Ini hanya contoh sederhana. Dalam skenario nyata, Kita mungkin perlu menggunakan beberapa middlewares untuk melakukan satu tugas, seperti melakukan pencatatan setiap HTTP Request ataupun melakukan validasi inputan user.

__Tugas Function Middleware__
- Menjalankan kode apapun.
- Memodifikasi Object Request dan Object Response.
- Menghentikan request-response cycle.
- Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.

## DESIGN DATABASE WITH MYSQL
- Entitas
  - Sesuatu yang dapat diidentifikasi dalam lingkungan kerja pengguna
  - Objek dalam dunia nyata yang dapat dibedakan dari objek lain
  - Entitas dapat berupa orang, benda, tempat, kejadian, konsep
    Contoh:
    - Orang: MAHASISWA, DOSEN, PEMASOK, PENJUAL
    - Benda: MOBIL, MESIN, RUANGAN
    - Tempat: NEGARA, DESA
    - Kejadian: PENJUALAN, REGISTRASI
    - Konsep: REKENING, KURSUS
- Atribut
  - Setiap entitas memiliki atribut untuk mendeskripsikan karakteristik dari entitas tersebut
    Contoh:
    - Mahasiswa = (NPM, Nama_Mhs, Alamat, Email)
    - Mobil = (Kode_Mobil, Merk_Mobil, Warna)
- Relasi
  - One to One : Setiap entitas pada himpunan A berhubungan paling banyak dengan satu pada himpunan B, begitu pula sebaliknya.
  - One to Many : Setiap entitas pada himpunan A dapat berhubungan dengan banyak entitas pada himpunan B, tetapi tidak sebaliknya, dimana setiap entitas himpunan B berhubungan dengan paling banyak dengan satu entitas.
  - Many to Many : Setiap entitas pada himpunan entitas A dapat berhubungan dengan banyak entitas pada himpunan B, demikian juga sebaliknya.
- Tipe Data
  - Primary Key : tanda pengenal unik yang membedakan satu record dari yang lain.
  - Foreign Key : pengenal unik atau kombinasi pengenal unik yang menghubungkan dua tabel atau lebih dalam database.


