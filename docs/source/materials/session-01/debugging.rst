Debugging
=========

Apabila program yang dibuat tidak berjalan dengan seharusnya, pembuat program dapat mencari tahu hal apa yang membuat hal tersebut terjadi dengan melakukan *debugging*. Dengan kata lain, *debug* adalah suatu proses untuk menganalisa dan memperbaiki kesalahan yang ada di dalam program, sehingga program dapat berjalan tanpa *bug*.

Terdapat beberapa jenis *error* yang dapat terjadi ketika membuat program.

*Syntax Error*
--------------

*Syntax error* dapat disebabkan oleh kesalahan dalam pembuatan kode seperti salah mengetikan kata kunci, menghilangkan beberapa tanda yang diperlukan, menggunakan kurung kurawal pembuka (``{``) tanpa kurung kurawal penutup (``}``), dan sebagainya. Kesalahan ini biasanya mudah dideteksi karena *compiler* akan memberi 
tahu letak kesalahan tersebut.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            //Syntax Error (kurang tanda ;)
            System.out.println("Hello World")
        }
    }

.. code:: console

    Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
        Syntax error, insert ";" to complete BlockStatements

        at Main.main(Main.java:4)

Kode di atas merupakan contoh dari *syntax error*. Berdasarkan informasi *error* yang tampil pada *console*, terlihat bahwa kode tersebut kurang tanda titik koma (``;``) pada file *Main.java* baris ke-4.

*Runtime Error*
---------------

*Runtime error* merupakan kesalahan yang terjadi saat program berjalan sehingga program harus berhenti secara tiba-tiba. Biasanya hal ini terjadi saat *input* yang dimasukan tidak sesuai atau format data yang diproses kurang sesuai.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            //Runtime Error (pembagian dengan angka 0)
            System.out.println(1/0);
        }
    }

.. code:: console

    Exception in thread "main" java.lang.ArithmeticException: / by zero
        at Main.main(Main.java:4)

Kode di atas merupakan contoh dari *runtime error*. Berdasarkan informasi error yang tampil pada *console*, terlihat bahwa terjadi *ArithmeticException* yaitu angka yang dibagi dengan 0 pada file *Main.java* baris ke-4. Contoh *runtime error* lainnya adalah ketika program meminta *input* sebuah angka, namun pengguna program memasukan *input* sebuah *string*, sehingga terjadi ketidaksesuaian tipe data.

*Logic Error*
-------------

*Logic error* terjadi ketika sebuah program tidak berjalan sesuai dengan yang diinginkan. Program akan tetap berjalan tanpa *error*, sehingga pembuat program harus mengecek secara manual informasi yang dihasilkan dari program tersebut.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            double celsius = 35;

            //Logic Error (kesalahan hasil pembagian)
            double fahrenheit = 9 / 5 * 35 + 32;

            System.out.printf("%.1f Celsius = %.1f Fahrenheit", celsius, fahrenheit);
        }
    }

.. code:: console

    35.0 Celsius = 67.0 Fahrenheit

Kode di atas merupakan contoh dari *logic error*. Hasil perhitungan menunjukan bahwa 35 derajat celsius sama seperti 67 derajat fahrenheit. Jawaban perhitungan tersebut salah, seharusnya adalah 95 derajat fahrenheit. Kesalahan tersebut terjadi karena salah tipe data dalam perhitungan pembagian. Pembagian antara 9 dengan 5 menghasilkan angka 1, karena pembagian dilakukan dengan tipe data *integer* (tidak menyimpan nilai desimal). Oleh karena itu, rumus tersebut harus diubah menjadi 9.0 / 5, sehingga pembagian dilakukan dengan tipe data *double*, menghasilkan 1.8.

*Common Error*
--------------

*Common error* dapat terjadi apabila pembuat program kurang teliti. Berikut adalah beberapa *common error* yang sering terjadi.

*Common Error 1 : Missing Brace*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Kurung kurawal (``{}``) digunakan untuk menandai sebuah *scope* dalam program. Setiap tanda kurung pembuka (``{``) harus diikuti oleh tanda kurung penutup (``}``). Hal ini sering menjadi kesalahan umum karena kurangnya pasangan kurung kurawal. Untuk menghindari kesalahan tersebut, pembuat program dapat melengkapi pasangan kurung kurawal yang kurang. Apabila menggunakan aplikasi *Eclipse*, secara otomatis akan langsung dibuat pasangan tanda tersebut.

.. code:: java

    public class Main {
    } // <- pastikan memiliki pasangan kurung kurawal

*Common Error 2 : Missing Semicolon*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Setiap perintah yang dibuat harus diakhiri oleh tanda titik koma (``;``). Hal ini sering menjadi kesalahan umum karena kurangnya tanda titik koma pada akhir perintah. Untuk menghindari kesalahan tersebut, pembuat program dapat melengkapi akhir perintah dengan tanda titik koma.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello World"); // <- pastikan memiliki tanda ;
        }
    }

*Common Error 3 : Missing Quotation Marks*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Setiap kalimat harus diapit dengan tanda kutip dua (``""``). Hal ini sering menjadi kesalahan umum karena kurangnya pasangan kutip dua. Untuk menghindari kesalahan tersebut, pembuat program dapat melengkapi pasangan kutip dua yang kurang.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello World"); // <- pastikan memiliki pasangan kutip dua 
        }
    }

*Common Error 4 : Misspelling Names*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Bahasa pemrograman Java bersifat *case sensitive*, artinya huruf kapital dianggap berbeda dengan huruf kecil. Hal ini sering menjadi kesalahan umum karena perbedaan nama *variabel*, *method*, atau *keyword*. Untuk menghindari kesalahan tersebut, pembuat program harus memperhatikan penamaan tersebut.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String variabel = "Hello World";
            System.out.println(variabel); // <- pastikan penamaan variabel dan keyword sudah sesuai
        }
    }