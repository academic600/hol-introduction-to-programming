Output dan Input
================

Output
------

*Output* merupakan informasi yang dihasilkan dari program dan ditampilkan ke *console* pengguna. Beberapa cara dalam melakukan *output* adalah sebagai berikut.

System.out.print()
~~~~~~~~~~~~~~~~~~

``System.out.print()`` dapat digunakan untuk mencetak teks tanpa karakter *newline* (baris baru) di akhir.

.. code-block:: java

    public class Main {
        public static void main(String[] args) {
            System.out.print("Hello");
            System.out.print("World");
            System.out.print("!");
        }
    }

.. code-block:: console

    HelloWorld!

System.out.println()
~~~~~~~~~~~~~~~~~~~~

``System.out.println()`` dapat digunakan untuk mencetak teks dengan menambahkan karakter *newline* (baris baru) di akhir.

.. code-block:: java

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello");
            System.out.println("World");
            System.out.println("!");
        }
    }

.. code-block:: console

    Hello
    World
    !
    (blank)

System.out.printf()
~~~~~~~~~~~~~~~~~~~

``System.out.printf()`` dapat digunakan untuk mencetak teks dalam format tertentu. Beberapa format yang dapat digunakan adalah sebagai berikut.

.. list-table::
   :header-rows: 1

   * - Format
     - Penjelasan
   * - %d
     - Digunakan untuk format bilangan bulat (*integer*).
   * - %f
     - Digunakan untuk format bilangan desimal (*floating-point*).
   * - %c
     - Digunakan untuk format karakter.
   * - %s
     - Digunakan untuk format kalimat (*string*).
   * - %b
     - Digunakan untuk format nilai kebenaran (*boolean*).

.. code-block:: java

    public class Main {
        public static void main(String[] args) {
            System.out.printf("%s %d\n", "Session", 1);
        }
    }

.. code-block:: console

    Session 1
    (blank)

.. note:: 

    *Escape sequence* adalah karakter khusus yang dimulai dengan karakter *escape* atau *backslash* (\\). Beberapa *escape sequence* yang dapat digunakan dalam melakukan output adalah sebagai berikut.

    .. list-table::
       :header-rows: 1

       * - *Escape Sequence*
         - Penjelasan
       * - \\n
         - Membuat sebuah karakter *newline* (baris baru).
       * - \\t
         - Membuat sebuah *tab* horizontal.
       * - \\b
         - Menghapus satu karakter dalam sebuah *string*.
       * - \\r
         - Menggerakkan kursor ke awal baris (tanpa membuat baris baru).
    

Komentar
--------

Komentar merupakan *syntax* yang digunakan untuk mendokumentasikan program dan akan diabakan oleh *compiler* (tidak akan muncul pada *console* pengguna). Terdapat dua jenis komentar yang dapat digunakan, yaitu:

Komentar Baris (*Line Comment*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Komentar baris diawali dengan dua garis miring (//).

.. code-block:: java

    public class Main {
        public static void main(String[] args) {
            // This is a line comment
        }
    }

Komentar Blok (*Block Comment*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Komentar blok diawali dengan garis miring & bintang (/\*) dan diakhiri dengan bintang & garis miring (\*/). Informasi atau kode yang diapit oleh kedua simbol tersebut tidak akan muncul pada *console* pengguna.

.. code-block:: java

    public class Main {
        public static void main(String[] args) {
            /* This is a 
               multiline 
               comment */
        }
    }

Input
-----

*Input* merupakan informasi yang diterima oleh program dari hasil ketikan pengguna lewat *console*. Untuk melakukan *input* dapat digunakan *class* ``Scanner`` yang berasal dari *package* ``java.utils``. Langkah yang harus dilakukan untuk membuat *input* adalah sebagai berikut.

Pertama, membuat *object* ``Scanner`` dengan kode di bawah ini. ``Scanner`` merupakan sebuah *class* yang sudah disediakan oleh *Java* untuk membaca *input* dari berbagai sumber. ``scan`` merupakan nama *variable* yang dibuat sebagai *object*. ``System.in`` merupakan bagian yang menunjukan bahwa *input* akan diambil dari ketikan pengguna program. ``new`` merupakan *syntax* yang digunakan untuk membuat sebuah *object* dari *class*.

.. code-block:: java
    
    Scanner scan = new Scanner(System.in);

Kedua, mendapatkan hasil ketikan pengguna dengan *method* di bawah ini.

.. list-table::
   :header-rows: 1

   * - *Method*
     - Penjelasan
   * - nextLine()
     - Digunakan untuk membaca input dalam bentuk kalimat (*string*). 
   * - nextShort()
     - Digunakan untuk membaca bilangan bulat dengan tipe data *short*.
   * - nextInt()
     - Digunakan untuk membaca bilangan bulat dengan tipe data *integer*.
   * - nextLong()
     - Digunakan untuk membaca bilangan bulat dengan tipe data *long*.
   * - nextDouble()
     - Digunakan untuk membaca bilangan desimal dengan tipe data *double*.   

Berikut adalah contoh program untuk mendapatkan *input* dalam bentuk bilangan bulat dan menampilkan kembali *input* tersebut.

.. code-block:: java

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            // Membuat objek 'Scanner'
            Scanner scan = new Scanner(System.in);

            // Membuat variabel bilangan bulat (integer) dengan nama 'myInput'
            int myInput;

            // Meminta pengguna program untuk memasukan sebuah bilangan bulat 
            System.out.print("Masukan sebuah bilangan bulat: ");

            // Mengambil input (dalam bentuk bilangan bulat) dari pengguna program 
            myInput = scan.nextInt();
            scan.nextLine();

            // Menampilkan input yang dimasukan oleh pengguna program
            System.out.printf("Bilangan bulat yang di masukan adalah %d", myInput);
        }

    }

.. code-block:: console

    Masukan sebuah bilangan bulat: 5
    Bilangan bulat yang di masukan adalah 5

.. note:: 

    Setiap kali ingin mengambil input selain kalimat (*string*) harus diakhiri dengan *method* ``nextLine()`` untuk menangkap sisa *newline* (baris baru, '\\n').

Import
------

Dari kode diatas, dapat dilihat bahwa saat ingin menggunakan ``Scanner`` perlu untuk melakukan *import* (dengan *syntax* ``import``) dari ``java.util.scanner`` terlebih dahulu.

*Import* digunakan untuk memasukkan *class* dari suatu *package* yang ada di luar ke dalam program. Tujuannya adalah agar pembuat program tidak perlu menulis kode dari awal untuk kode yang sudah disediakan dari luar.

.. code:: java

    import java.util.Scanner;

Pada kode di atas, program akan melakukan *import* untuk *class* ``Scanner`` dari *package* ``java.util``.

.. note:: 

    Untuk mempermudah dan mempercepat pembuatan program, Anda dapat menggunakan ``ctrl + space`` untuk menampilkan saran atau *autocomplete* yang dibuat oleh IDE *Eclipse*.

    .. image:: /images/session-01/autocomplete-print.png
        :align: center

    Dengan menggunakan ``ctrl + space`` tersebut juga, apabila terdapat sebuah *class* yang berasal dari *package* yang ada di luar, secara otomatis IDE *Eclipse* akan melakukan *import* pada kelas tersebut, sehingga Anda tidak perlu mengetik *syntax* ``import`` secara manual.

    .. image:: /images/session-01/autocomplete-scanner.png
        :align: center
