# Writing Test (10-12 Oktober 2022)

## JAVASCRIPT INTERMEDIATE

### Asynchronous - Fetch 



### Asynchronous - Async Await
### Git & Github Lanjutan

- __GIT ADD__
    Setelah cek status dengan `git status`, selanjutnya kita ubah status untrackted file dan unmodified menjadi modified dengan menggunakan:

    `git add .`


- __GIT COMMIT__
    Lakukan `git commit` untuk save perubahan pada version control.

    `git commit -m "first commit"`

- __GIT LOG__
    ![revisi](img/revisifile.png)

    Kedua revisi diatas kita anggap sebagai checkpoint. Jika nanti ada kesalahan, kita bisa kembali pada checkpoint ini. 

    Dari dua revisi yang sudah dilakukan kita dapat melihat catatal log dari revisi - revisi tersebut dengan menggunakan perintah berikut ini:

    `git log`

- __GIT CHECKOUT, GIT RESET, GIT REVERT__
    Jika perubahan yang sedang dilakukan terjadi kesalahan dan kita ingin mengembalikan keadaan seperti sebelumnya maka itu bisa dilakukan.

    - Untuk Membatalkan Perubahan Belum Stagged dan Belum Commited, maka bisa dilakukan dengan perintah `git checkout` berikut ini: 
        `git checkout index.html`
    - Untuk Membatalkan Perubahan Sudah Stagged namun Belum Commited, maka bisa dilakukan dengan perintah `git reset` berikut ini:
        `git reset index.html`
    - Untuk membatalkan semua perubahan yang ada tanpa menghapus commit terakhir. maka bisa dilakukan dengan perintah `git revert` berikut ini:
        `git revert -n <nomor commit>`
    Jika menggunakan GIT Reset, commit terakhir akan hilang.

- __GIT BRANCH__
  - Merupakan fitur yang WAJIB digunakan jika berkolaborasi dengan developer atau dalam tim.
  - Untuk menghindari conflict code yang dikembangkan. Kita tidak boleh berkolaborasi dalam project di satu branch yang sama! Misalnya Bowo akan mengerjakan fitur A dan Gigih mengerjakan fitur B. Masing-masing fitur harus dibuat branch masing-masing.
  - Untuk membuat branch, gunakan perintah berikut ini:
    `git branch <branch>`

    Misalkan kita ingin membuat fitur register. Jadi kita akan membuat branch baru.
    `git branch fitur_register`
  - Untuk melihat list branch, maka kita bisa menggunakan:
    `git branch`
  - Untuk menuju kedalam suatu branch tertentu. dapat menggunakan perintah seperti berikut ini:
    `git checkout fitur_register`
  - Untuk menghapus sebuah branch, dapat menggunakan perintah seperti berikut ini:
    `git branch -d <branch>`

- __GIT MERGE__
  Untuk menyatukan branch cabang fitur yang telah kita kembangkan. Gunakan perintah seperti berikut ini:
  1.  Checkout dahulu ke branch master
        `git checkout master`
  2.  Melakukan merge
        `git merge halaman-login`


### Responsive Web Design

Responsive web design adalah bertujuan untuk membuat design website kita dapat diakses dalam device apapun.

Setiap developer website wajib menggunakan tools bawaan dari setiap browser yang dapat memudahkan development website. Pada browser chrome biasa disebut dengan chrome dev tools.

cara menggunakan chrome dev toools dari RWD.
1. Membuka browser chrome dan menggunakan shortcut ini: `ctrl+shift+j` 
2. Klik icon yang mengilustrasikan phone dan tablet
3. Add viewport in HTML
4. Menggunakan elemen max-width agar panjang image menjadi overflow karena mengikuti width real bawaan dari file image. 
5. Menggunakan media query. Jenis media query ada 2 yakni, max-width dan min width.
6. Menggunakan Breakpoint yang merupakan perubahan yang terjadi pada tampilan saat berganti device atau ukuran width.

### Bootstrap 5