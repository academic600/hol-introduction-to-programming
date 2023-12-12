Debugging
=========

Apabila program yang dibuat tidak berjalan dengan seharusnya, pembuat program dapat mencari tahu hal apa yang membuat hal tersebut terjadi dengan melakukan *debugging*. Dengan kata lain, *debug* adalah suatu proses untuk menganalisa dan memperbaiki kesalahan yang ada di dalam program, sehingga program dapat berjalan tanpa *bug*.

Terdapat beberapa jenis *error* yang dapat terjadi ketika membuat program.

.. image::  /images/01/error.png
    :align: center


.. TODO: Tambahkan jenis-jenis error yang sering terjadi [halaman 42-44].

*Syntax Error*
--------------
Kesalahan sintaks disebabkan oleh kesalahan dalam konstruksi kode, seperti salah mengetik kata kunci, menghilangkan beberapa tanda baca yang diperlukan, atau menggunakan kurung kurawal pembuka tanpa kurung kurawal penutup yang sesuai. Kesalahan ini biasanya mudah dideteksi karena kompilator memberi 
tahu kita di mana letak kesalahan tersebut.

.. code:: java

.. image::  /images/session-01/error.png
    :align: center
    public class Main {
        public static void main(String[] args) {
            //syntax Error
            System.out.println("Halo nama ku adalah Budi")

        }

    }


.. code:: console

    Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
	Syntax error, insert ";" to complete BlockStatements

	at main.Main.main(Main.java:5)

Pada contoh kode di atas kekurangan syntax semicolon ``;`` setelah tanda tutup kurung, sehingga menyebabkan syntax error.
	

*Runtime Error*
---------------
Kesalahan runtime adalah kesalahan yang menyebabkan sebuah program berhenti secara tiba-tiba. 
Mereka terjadi saat program sedang berjalan jika lingkungan mendeteksi operasi yang tidak dapat dilakukan. 
Kesalahan pada `input` biasanya menjadi penyebab kesalahan `runtime`. 
Kesalahan masukan terjadi ketika program menunggu pengguna untuk memasukkan nilai, 
tetapi pengguna memasukkan nilai yang tidak dapat ditangani oleh program. 

**Contoh**: 
    - jika program mengharapkan untuk membaca angka, tetapi pengguna justru memasukkan string, ini menyebabkan kesalahan tipe data terjadi dalam program.
    - pembagian dengan angka nol, yang akan menyebabkan error

.. code:: java

    public class Main {
        public static void main(String[] args) {
            //pembagian angka bulat dengan 0
            System.out.println(1/0);

        }

    }

.. code:: console

    Exception in thread "main" java.lang.ArithmeticException: / by zero
	at main.Main.main(Main.java:5)

	


*Logic Error*
-------------
Kesalahan logika terjadi ketika sebuah program tidak berjalan sesuai dengan yang diinginkan. Kesalahan semacam ini terjadi karena banyak alasan yang berbeda. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
            System.out.print("Hasil dari 35 celcius ke farenheit: ");
            System.out.println((9 / 5) * 35 + 32);

        }

    }

.. code:: console

    Hasil dari 35 celcius ke farenheit: 67

Output di atas menghasilkan 67, hal ini adalah salah jawaban yang seharusnya adalah 95.0, terdapat kesalahan logical error diatas yaitu seharusnya ``(9.0/5)`` yang akan menghasilkan ``1.8``.





*Common Error*
--------------
Kesalahan umum bagi pemrogram pemula adalah kurangnya tanda kurung penutup, kurangnya titik koma, kurangnya tanda kutip untuk string, dan pengejaan yang salah untuk nama-nama.

*Common Error 1 : Missing Brace*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Kurung kurawal digunakan untuk menandai sebuah blok dalam program. Setiap tanda kurung buka harus diikuti oleh tanda kurung tutup. Kesalahan umum adalah kelupaan dalam menuliskan tanda kurung tutup. Untuk menghindari kesalahan ini, ketik tanda kurung tutup setiap kali mengetik tanda kurung buka

.. code:: java

    public class Main {

    } //-> langsung membuat tutup kurung

akan tetapi jika memakai IDE seperti NETBEANS, Eclipse akan terbuat tutup kurung secara otomatis.

*Common Error 2 : Missing Semicolon*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Kurangnya tanda titik koma pada setiap akhir baris code. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
            System.out.println("Programming sangat menyenangkan");
            System.out.println("Aku suka sekali programming") //hilangnya tanda `;`
        }

    }

*Common Error 3 : Missing Quotation Marks*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Kurangnya tanda petik yang digunakan pada kata (*string*) yang menyebabkan error.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            //kurangnya tanda  " pada akhir kalimat
            System.out.println("Programming sangat menyenangkan); 
           
        }

    }

*Common Error 3 : Misspelling Names*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Java bersifat case sensitive. Salah pengejaan pada nama-nama merupakan kesalahan umum bagi pemrogram pemula. Sebagai contoh, kata *"main"* dieja dengan kesalahan sebagai *"Main"* dan *"String"* dieja dengan kesalahan sebagai *"string"* dalam contoh berikut:  

.. code:: java

    public class Main {
        public static void main(String[] args) {
            //terjadi kesalahan pengejaan, yang seharusnya "String" menjadi "string"
            string nama = "Toni";
            
        }

    }