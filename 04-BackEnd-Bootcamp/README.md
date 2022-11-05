# WRITING TEST (31 OKTOBER - 4 NOVEMBER 2022)

## Database MySQL Basic 

- Database merupakan tempat penyimpanan data yang terstruktur.
- Untuk mengakses database, dapat menggunakan DBMS
- Didalam DBMS, dapat digunakan untuk membuat beberapa/banyak database.
- Macam-macam DBMS yang bertipe SQL yaitu MySQL, MariaDB, PosgreSQL, Oracle, IBM DB2
- MySQL bersifat opensource dan compatible untuk banyak platform
- Tampilan dari MySQL Workbench
  ![Tampilan MySQL Workbench](img/sql%20workbench.png)
- Saat membuat database harus ada server yang berjalan yaitu MySQL Server dengan nomor port pada umumnya yaitu 3306, untuk mengakses MySQL Server dapat menggunakan MySQL Workbench / Dbeaver / TablePlus / Php My Admin.
- Cara connect SQL, dapat melakukan klik tanda + pada MySQL Connection di workbench. Kemudian, mengisi nama koneksi, hostname, port, username, dan password. Maka akan tampil tampilan berikut pada saat setelah klik test connection.
  ![Test Connection](img/koneksi%20my%20SQL.png)
- Berikut ini, tampilan workbench setelah melakukan test connection
  ![Tampilan Workbench](img/workbench%20setelah%20test%20koneksi.png)
  Pada tampilan diatas, terlihat terdapat nama koneksi yaitu localhost.
- Setelah itu, melakukan klik 2 kali pada nama koneksi localhost. Dan berikut ini adalah tampilannya.
  ![Tampilan Localhost](img/localhost.png)
- Didalam SQL terdapat beberapa macam tipe data yaitu:
  - Number : int, float, decimal
  - Boolean : Char, VarChar, Text, Enum
  - String : True or False
  - Tanggal : DATE, DATETIME, TIME, timestamp
  - Default : NULL
- Istilah dalam database
  - Table : kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisikan atribut dari sebuah data.
  - Field/atribut : kolom dari sebuah tabel dimana masing-masing field memiliki tipe data masing-masing.
  - Record : kumpulan nilai yang saling terkait. Record merupakan isi dari sebuah tabel.
- Terdapat 4 Perintah Dasar di SQL:
  ![Perintah SQL](img/perintah%20sql.png)
  - DDL, bermain di table
  - DML, bermain di data
- Cara membuat dan menggunakan database 
  ![membuat database](img/createnuse%20database.png)
- Cara Membuat Table
  ![create table](img/create%20table.png)
- Untuk melihat apa saja table yang terdapat pada database
  ![show table](img/melihat%20table.png)
- Untuk melihat kolom yang ada pada table
  ![desc table](img/melihat%20isi%20table.png)
- Untuk menghapus table
  ![drop table](img/drop%20table.png)
- Menambahkan atribut pada table
  ![alter table](img/menambahkan%20atribut.png)
  Alter dapat menambah kolom atau menghapus kolom pada table.
- Untuk menambahkan data dalam table dan melihat isi table
  ![insert dan select](img/menambahkan%20data.png)
- Untuk memperbarui data dalam table
  ![update data](img/update%20data.png)
- Untuk menghapus data 
  ![delete data](img/delete.png)
- Untuk mengubah nama kolom hanya sementara pada saat ingin dilihat
  ![](img/mengubah%20nama%20sementara.png)
- Untuk mencari data yang memiliki email gmail
  ![](img/like.png)
- Untuk memanggil data dengan jumlah tertentu
  ![](img/limit.png)
- Untuk memanggil data dari id terbesar
  ![](img/desc.png)


## MySQL Lanjutan
## Authentication & Authorization in Express
## Sequalize
