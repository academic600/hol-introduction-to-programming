*Method* dan *Parameter*
========================

Sebenarnya pada materi sebelumnya, kita sudah membuat dan menggunakan *method*, yaitu ``public static void main(String[] args)``. Semua perintah yang ingin dilakukan, semuanya dimasukan ke dalam *mehtod* tersebut. Apabila sebuah program semakin besar dan kompleks, maka kode yang ada di dalam *method* tersebut juga akan semakin banyak. Selain itu, terdapat juga kemungkinan adanya kode yang duplikat dalam menjalankan tugas tertentu.

Oleh karena masalah tersebut, bahasa pemrograman *Java* memungkinkan pembuat program dapat membuat dan menggunakan *method* buatan sendiri. Secara singkat, *method* merupakan kumpulan perintah yang digunakan untuk menjalankan suatu tugas tertentu. Sebuah *method* dapat mengembalikan atau tidak mengembalikan sebuah nilai dari tugas tersebut. Tujuan dibuatnya sebuah *method* adalah untuk memecahkan sebuah kode menjadi bagian-bagian yang lebih kecil. Selain itu, *method* juga dapat digunakan untuk menghilangkan bagian kode yang duplikat.

Berikut adalah syntax dalam membuat dan memanggil sebuah *method*.

.. code:: console

    access_modifier return_type method_name(parameter1, ...) {
        // statements
        return data; // opsional, apabila mengembalikan sebuah nilai
    }

    mehtod_name(parameter1, ...);

*Access Modifier*
-----------------

*Access modifier* merupakan kata kunci yang digunakan untuk sifat dari sebuah variabel, *class*, atau *method*. Sifat yang dimaksud adalah visibilitas dari elemen tersebut. Berikut adalah *access modifier* yang dimiliki oleh bahasa pemrograman *Java*.

.. list-table::
   :widths: 20 80
   :header-rows: 1

   * - Nama
     - Penjelasan
   * - ``public``
     - Dapat diakses secara publik dari mana saja, baik di dalam *class* yang sama, *package* yang berbeda, atau melalui pewarisan.
   * - ``private``
     - Hanya dapat diakses dari dalam *class* yang sama. Tidak dapat diakses dari *class* lain atau melalui pewarisan.
   * - ``protected``
     - Hanya dapat diakses dari dalam *class* yang sama, *sub-class* (melalui pewarisan), dan *package* yang sama. Tidak dapat diakses dari *package* yang berbeda, kecuali melalui pewarisan.
   * - ``default``
     - Hanya dapat diakses dari dalam *package* yang sama. Tidak dapat diakses dari *package* yang berbeda, atau melalui pewarisan.

.. note:: 

    Pada bagian ini akan digunakan *access modifier* ``public`` saja untuk mempermudah penjelasan materi. *Access modifier* lain akan digunakan lebih banyak dan bervariasi ketika masuk ke dalam materi *Object Oriented Programming* (OOP).

*Return Type*
-------------

*Return type* dapat diartikan sebagai nilai yang dikembali ketika *method* tersebut dipanggil. Namun, tipe data nilai yang dikembalikan harus ditentukan terlebih dahulu.

.. note:: 

    Apabila tidak ada nilai yang dikembalikan, maka tipe data yang digunakan adalah ``void``.

Berikut adalah beberapa contoh deklarasi method dengan tipe data yang berbeda-beda.

.. code:: java

    public class Main {
        // Deklarasi method getValidation dengan return type boolean
        public boolean getValidation() {
            return true;
        }

        // Deklarasi method getMessage dengan return type String
        public String getMessage() {
            return "Hello World!";
        }

        // Deklarasi method displayMessage dengan return type void (tidak mengembalikan nilai)
        public void displayMessage() {
            System.out.println("Java Programming");
        }

        public Main() {
            // Memanggil method getValidation
            boolean result = getValidation();
            System.out.println("Hasil dari method getValidation adalah " + result);
            
            // Memanggil method getMessage
            System.out.println("Hasil dari method getMessage adalah " + getMessage());
            
            // Memanggil method displayMessage 
            System.out.print("Hasil dari method displayMessage adalah ");
            displayMessage();
        }

        public static void main(String[] args) {
            new Main();   
        }
    }

.. code:: console

    Hasil dari method getValidation adalah true
    Hasil dari method getMessage adalah Hello World!
    Hasil dari method displayMessage adalah Java Programming

.. note:: 

    Sebelumnya semua kode dituliskan ke dalam *method* ``public static void main(String[] args)``. *Method* tersebut memiliki kata kunci ``static``, artinya terikat pada *class*, bukan *object* dari *class* tersebut. Apabila semua kode yang ada pada *scope constructor* ``public Main()`` dipindahkan ke *method* ``public static void main(String[] args)``, akan muncul error sebagai berikut.

    .. code:: console

        Main.java:20: error: non-static method getValidation() cannot be referenced from a static context
            boolean result = getValidation();
                             ^
        Main.java:24: error: non-static method getMessage() cannot be referenced from a static context
            System.out.println("Hasil dari method getMessage adalah " + getMessage());
                                                                        ^
        Main.java:28: error: non-static method displayMessage() cannot be referenced from a static context
            displayMessage();  
            ^
        3 errors
    
    Terdapat dua cara untuk mengatasi hal ini. Pertama, *method* yang dipanggil juga harus ditambahkan kata kunci ``static``. Contohnya adalah ``public static boolean getValidation()``. Kedua, kode tersebut dipidahkan ke dalam *constructor* ``public Main()``, seperti pada kode di atas. Penjelasan mengenai *constructor* akan dibahas pada materi *Object Oriented Programming* (OOP).

*Parameter* 
-----------

Pada bahasa pemrograman *Java*, *parameter* adalah nilai yang diberikan ketika sebuah *method* dipanggil. Dengan kata lain, *parameter* digunakan untuk mengirimkan data ke dalam method untuk digunakan di dalamnya. *Parameter* tersebut dideklarasikan di dalam sepasang tanda kurung (``()``). Apabila terdapat lebih dari satu *parameter*, data tersebut dipisahkan dengan tanda koma (``,``).

.. code:: Java

    public class Main {
        // Deklarasi method greeting dengan satu parameter
        public void greeting(String username) {
            System.out.println("Hello, " + username + "!");
        }

        // Deklarasi method greeting dengan dua parameter
        public int add(int x, int y) {
            return x + y;
        } 

        public Main() {
            // Memanggil method greeting
            String username = "Alice";
            greeting(username);

            // Memanggil method add
            int result = add(10, 20);
            System.out.println("Hasil penjumlahannya " + result);
        }

        public static void main(String[] args) {
            new Main();
        }
    }


.. code:: console

    Hello, Alice!
    Hasil penjumlahannya 30

*Return* dan *Parameter Array*
------------------------------

Berikut adalah contoh implementasi *array* pada sebuah *method*.

.. code:: java

    public class Main {	
        public int[] addTwo(int[] array) {
            for (int i = 0; i < array.length; i++) {
                array[i] += 2;
            }
            return array;
        }

        public Main() {
            int[] array = new int[]{3, 1, 2, 6, 4, 2};
            int[] newArray = addTwo(array);
            for (int i = 0; i < array.length; i++) {
                System.out.print(newArray[i] + " ");
            } 
        }

        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    5 3 4 8 6 4 
