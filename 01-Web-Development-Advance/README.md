# Writing Test (3-7 Oktober 2022)

## JAVASCRIPT INTERMEDIATE

### ARRAY

#### Apa itu Array?

- Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.
- Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

#### Contoh Array

    const cars = [                    
    "Saab",
    "Volvo",             
    "BMW"
    ];

--- 

    const cars = [];
    cars[0]= "Saab";
    cars[1]= "Volvo";
    cars[2]= "BMW";

--- 

    const cars = new Array("Saab", "Volvo", "BMW");



#### Membuat dan Memanggil Array

- Membuat Array
  
  `const array_name = [item1, item2, ...]; `

- Memanggil Array
  
  ![array](img/array.png)

  `console.log(array_name);`
  atau
  `console.log(array_name[index]);`

- Contoh
  
        let arrBuah = [
        "jeruk", 
        "semangka", 
        "pepaya", 
        "rambutan",
        "melon",
        "belimbing"
        ]

        console.log(arrBuah);

  ![Output_Array](img/contohArray.png)


#### Update Array
Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array. Contohnya:

![Update_Array](img/updateArray.png)

#### Const in Array

- Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
- Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const

![Error](img/ErrorConstArray.png)
![Const Array](img/ConstArray.png)

#### Array Properties

- Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.
- Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
    - Constructor
        Properti constructormengembalikan fungsi yang membuat prototipe Array. Untuk array JavaScript, `constructor` properti mengembalikan:
        `function Array() { [native code] }`
        syntax:
        `array.constructor`
        contoh:

            <script>
            const fruits = ["Banana", "Orange", "Apple", "Mango"];
            let text = fruits.constructor;

            document.getElementById("demo").innerHTML = text;
            </script>

            //output : function Array() { [native code] }

    - Length
        Properti length menetapkan atau mengembalikan jumlah elemen dalam array. contoh:

            <script>
            const fruits = ["Banana", "Orange", "Apple", "Mango"];
            let length =  fruits.length;

            document.getElementById("demo").innerHTML = length;
            </script>
             
            //output : 4
        atau


            <script>
            const fruits = ["Banana", "Orange", "Apple", "Mango"];
            fruits.length = 2;

            document.getElementById("demo").innerHTML = fruits;
            </script>

            //output : Banana, Orange

    - Prototype
      - `prototype` memungkinkan untuk menambahkan properti dan metode baru ke array. syntax:
        `Array.prototype.name = value`
      - Properti `prototype` JavaScript memungkinkan untuk menambahkan properti baru ke objek. contoh:
  
            <script>
            function Person(first, last, age, eye) {
            this.firstName = first;
            this.lastName = last;
            this.eyeColor = eye;
            }
            const myFather = new Person("John", "Doe", "blue");
            const myMother = new Person("Sally", "Rally", "green");

            Person.prototype.nationality = "English";

            document.getElementById("demo").innerHTML =
            "My father is " + myFather.nationality + "<br>" +
            "My mother is " + myMother.nationality;
            </script>
            //output : My father is English
                       My mother is English


#### Array Methods

- Array memiliki method atau biasa disebut built-in methods.
- Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. 
- Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
- contoh:
  - `.push()` adalah method untuk menambahkan item  array pada urutan yang paling akhir.
  - `.pop()` adalah method yang menghapus item array index terakhir.
  - `.shift()` adalah method untuk menghapus item Array pada index pertama
  - `.unshift()` adalah method untuk menambahkan item Array pada index pertama
  - `.sort()` adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric.

#### Looping in Array

- Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()
    - `.forEach()` adalah method untuk melakukan looping pada setiap elemen array. Menggunakan `.forEach()` jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
    
            // ========= contoh kasus ===========
            // Merubah angka desimal menjadi persen
            let angkaDes = [
            0.45,
            0.67,
            0.23,
            0.76,
            ]

            // Cara forEach
            let angkaPersenForEach = []
            angkaDes.forEach((item) => {
            angkaPersenForEach.push(item * 100 + "%")
            })
            console.log(angkaPersenForEach)

        Output:
        ![ForEach](img/outputFor.png)

    - `.map()` melakukan perulangan/looping dengan membuat array baru. Menggunakan `.map()` jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.
            
            // ========= contoh kasus ===========
            // Merubah angka desimal menjadi persen
            let angkaDes = [
            0.45,
            0.67,
            0.23,
            0.76,
            ]

            // Cara map
            // kasus seperti ini lebih dianjurkan menggunakan map
            let angkaPersenMap = angkaDes.map((item) => {
            return item * 100 + "%"
            })
            console.log(angkaPersenMap);

        Output:
        ![map](img/outputMap.png)

- Bisa lihat bahwa `.map()` dan `forEach()` sama-sama melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan.
- Perbedaannya adalah `.forEach` tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping.
- Dari segi performance juga sangat jauh.


### MULTIDIMENSIONAL ARRAY

### OBJECT
### RECURSIVE
### WEB STORAGE
### ASYNCRONOUS