Method 
=====================
*Method* adalah sebuah module blok code yang akan dijalankan ketika di panggil.
Fungsi dari method adalah agar kita bisa memecahkan program menjadi bagian-bagian yang lebih kecil dan kompleks agar bisa dipakai kembali. 
``Method`` dapat mengembalikan nilai tertentu (memiliki ``return value``), dan ada juga method yang tidak memiliki return value ``(void)``

Berikut sintaks method: 

.. code:: console

    [modifiers] returnType methodName(parameterList) {
        // kode di dalam metode
        // bisa termasuk pernyataan, ekspresi, pemanggilan metode lain, dll.
        return value; // opsional jika returnType bukan void
    }

*Modifier*
~~~~~~~~~~

*Modifier* adalah kata kunci yang digunakan untuk mengatur atau memodifikasi sifat dari kelas, variabel, atau metode. ``Modifiers`` memengaruhi visibilitas, sifat, dan perilaku dari elemen-elemen dalam program Java.

+------------------+---------------------------------------------------------------+
| Modifier         | Cakupan Akses yang Dapat Diakses                              |
+==================+===============================================================+
|| public          || Dapat diakses dari mana saja, baik di dalam kelas yang sama, |
||                 || package yang berbeda, atau melalui pewarisan.                |
+------------------+---------------------------------------------------------------+
|| private         || Hanya dapat diakses di dalam kelas yang sama. Tidak dapat    |
||                 || diakses dari kelas lain atau melalui pewarisan.              |
+------------------+---------------------------------------------------------------+
|| protected       || Dapat diakses di dalam kelas yang sama, subclass, dan        |
||                 || package yang sama. Tidak bisa diakses dari package yang      |
||                 || berbeda, kecuali melalui pewarisan.                          |
+------------------+---------------------------------------------------------------+
|| default /       || Hanya dapat diakses di dalam package yang sama. Tidak bisa   |
|| package-private || diakses dari package yang berbeda atau melalui pewarisan.    |
+------------------+---------------------------------------------------------------+

*Return type*
~~~~~~~~~~~~~~~~~
*Return type* dalam Java mengacu pada tipe data nilai yang dikembalikan oleh sebuah metode. Saat mendefinisikan metode, kita harus menentukan tipe data yang akan dikembalikan oleh metode tersebut setelah kata kunci ``return``. Jika metode tidak mengembalikan nilai, maka tipe data kembalian ditetapkan sebagai ``void``.

.. code:: java

    public class Main {

        // Metode dengan return type int
        public static int add(int a, int b) {
            return a + b;
        }

        // Metode dengan return type String
        public String getMessage() {
            return "Hello, World!";
        }

        // Metode dengan return type void (tidak mengembalikan nilai)
        public void displayMessage(String message) {
            System.out.println(message);
        }
        
        //Panggil method di constructor
        public Main() {
            //Memanggil method add dalam variabel 
            int hasil = add(10 , 7);
            System.out.println("Hasil dari method add : "+ hasil);
            
            System.out.println("Hasil dari method get message : " + getMessage());
            
            //memanggil method diplay message 
            displayMessage("Java Sangat Menyenangkan!");
            
            
        }

        public static void main(String[] args) {
            
            //memanggil constructor
            new Main();
        }
    }

.. code:: console

    Hasil dari method add : 17
    hasil dari methid get message : Hello, World!
    Java Sangat Menyenangkan!


Parameter 
~~~~~~~~~~~~~~~~
Parameter dalam Java adalah nilai yang diterima oleh sebuah metode saat dipanggil. Mereka digunakan untuk mengirim data ke dalam metode untuk diproses atau digunakan di dalamnya.
Parameter dideklarasikan dalam tanda kurung ``()`` setelah nama metode dan dapat memiliki beberapa parameter, dipisahkan oleh koma.

.. code:: Java

    public class Main {
    // Metode dengan satu parameter
        public static void greetUser(String name) {
            System.out.println("Hallo, " + name + "! Selamat datang.");
        }

        public static void main(String[] args) {
            String userName = "Alice";

            // Memanggil metode greetUser() dengan satu argumen
            greetUser(userName);
        }
    }


.. code:: console

    Hallo, Alice! Selamat datang.


Memanggil method 
~~~~~~~~~~~~~~~~~~~~~~~
Untuk memanggil method yang sudah kita buat, kita bisa menggunakan sintaks berikut : 

.. code:: console

    namaMethod(parameter)  //pakaikan parameter bila ada


.. code:: java

    public class Main {
        //method dengan return ty
        public static int penjumlahanAngka(int a, int b) {
            int hasil = a + b;
            return hasil;
        }
        
        public static void main(String[] args) {

            //menampung method ke dalam variabel terlebih dahulu
            int hasil = penjumlahanAngka(2,3);
            System.out.println("Hasil yang di dapat: "  + hasil);

            //langsung memanggill saat print
            System.out.println("Hasil penjumlahan angka: " + penjumlahanAngka(10, 3));
        }


    }


.. code:: console

    Hasil yang di dapat: 5
    Hasil penjumlahan angka: 13


Passing Array ke Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Sama seperti kita dapat meneruskan nilai tipe primitif ke ``method``, Anda juga dapat meneruskan array ke ``mehtod``.

.. code:: java

   public class Main {
	
    public static void printArray(int[] array) {
        for (int i = 0; i < array.length; i++) {
        	System.out.print(array[i] + " ");
        }
        
    }

    public static void main(String[] args) {
    	printArray(new int[]{3, 1, 2, 6, 4, 2});
    
    }
    
}

.. code:: console

    3 1 2 6 4 2 


Mengembalikan Array dari Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Kita dapat ``passing array`` saat memanggil sebuah metode. Sebuah metode juga dapat mengembalikan  ``(return)`` sebuah array. Sebagai contoh, metode berikut mengembalikan sebuah array yang merupakan kebalikan dari array lainnya.

.. code:: java

    public class Main {
	
        public static int[] createArray() {
            // Mendeklarasikan dan menginisialisasi sebuah array
            int[] numbers = {1, 2, 3, 4, 5};
            return numbers; // Mengembalikan array numbers
        }

        public static void main(String[] args) {
            int[] returnedArray = createArray(); // Memanggil metode createArray dan menyimpan hasilnya

            // Menampilkan elemen-elemen array yang dikembalikan
            System.out.println("Isi array yang dikembalikan:");
            for (int num : returnedArray) {
                System.out.print(num + " ");
            }
        }
    
    }

.. code:: console

    Isi array yang dikembalikan:
    1 2 3 4 5 