@ -0,0 +1,185 @@
Array 
=====

*Array* merupakan salah satu jenis struktur data yang digunakan untuk menyimpan beberapa data dengan tipe data yang sama. Pada saat membuat variabel, pembuat program dapat langsung menggunakan nama variabel untuk mengakses dan memberikan nilai. Namun, pada *array* perlu menggunakan *index* dalam mengakses dan memberikan nilai. *Index* sendiri merupakan sebuah angka numerik yang dimulai dari nol (0) untuk menunjukan urutan data pada *array*.

Deklarasi *Array*
-----------------

Cara dalam mendeklarasi sebuah *array* hampir mirip dengan cara mendeklarasikan sebuah variabel. Perbedaannya terletak pada tanda sepasang kurung siku (``[]``) yang berfungsi untuk menunjukan bahwa variabel yang dibuat merupakan sebuah *array*. Terdapat dua cara untuk mendeklarasikan sebuah *array*, yaitu deklarasi tanpa inisialisasi dan deklarasi dengan inisialisasi.

Deklarasi *array* tanpa inisialisasi artinya pembuat program hanya membuat sebuah array sebanyak yang dibutuhkan dengan nilai *default*. Pada tipe data numerik (seperti ``int`` dan ``double``) memiliki nilai *default* nol (0), tipe data boolean memiliki nilai *default false*, dan tipe data referensi (seperti ``String``) memiliki nilai ``null``. Berikut adalah *syntax* dalam mendeklarasikan *array* tanpa inisialisasi.

.. code:: console

    tipe_data[] nama_array = new tipe_data[jumlah_data];

.. note:: 

    Pada bahasa pemrograman, ``null`` digunakan untuk memberikan tanda bahwa variabel tersebut tidak memiliki referensi atau nilai.

Sedangkan, deklarasi *array* dengan inisialisasi artinya pembuat program membuat sebuah *array* dengan langsung memberikan nilai. Nilai tidak bersifat tetap, artinya dapat diubah apabila diperlukan. Berikut adalah *syntax* dalam mendeklarasikan *array* dengan inisialisasi.

.. code:: console

    tipe_data[] nama_array = {data1, data2, data3, ...};

Berikut ini adalah contoh implementasi kode untuk kedua cara deklarasi *array* yang sudah dijelaskan di atas.

.. code:: java

    public class Main {
        public static void main(String args[]) {
            String[] names = new String[3];
            for (int i = 0 ; i < names.length ; i++) {
                System.out.println("names[" + i + "] = " + names[i]);
            }
            
            int[] ages = new int[3];
            for (int i = 0 ; i < ages.length ; i++) {
                System.out.println("ages[" + i + "] = " + ages[i]);
            }
            
            double[] scores = {90.5, 94.4, 45.3};
            for (int i = 0 ; i < scores.length ; i++) {
                System.out.println("scores[" + i + "] = " + scores[i]);
            }
        }
    }

.. code:: console

    names[0] = null
    names[1] = null
    names[2] = null
    ages[0] = 0
    ages[1] = 0
    ages[2] = 0
    scores[0] = 90.5
    scores[1] = 94.4
    scores[2] = 45.3


Berdasarkan kode di atas, bagian paling atas merupakan deklarasi *array* bernama ``names`` untuk tipe data ``String`` sebanyak 3 buah data yang berisikan nilai *default*, yaitu ``null``. Pada bagian tengah merupakan deklarasi *array* bernama ``ages`` untuk tipe data ``int`` sebanyak 3 buah data yang berisikan nilai *default*, yaitu nol (0). Pada bagian terakhir merupakan deklarasi *array* bernama ``scores`` untuk tipe data ``double`` sebanyak 3 buah data yang berisikan nilai sesuai yang diberikan.

Menetapkan dan Mengakses *Array*
--------------------------------

Sesuai dengan yang sudah dijelaskan pada bagian sebelumnya, setiap data atau elemen dapat *array* dapat diakses menggunakan *index* yang dimulai dari nol (0). Berikut adalah implementasi kode untuk menetapkan dan mengakses nilai dari sebuah array.

.. code:: java

    public class Main {

        public static void main(String[] args) {
            int[] numbers = new int[5];

            numbers[0] = 10;
            numbers[1] = 20;
            numbers[2] = 30;
            numbers[3] = 40;
            numbers[4] = 50;

            System.out.println("Nilai dari numbers[0] adalah " + numbers[0]);
            System.out.println("Nilai dari numbers[2] adalah " + numbers[2]);
            System.out.println("Nilai dari numbers[4] adalah " + numbers[4]);
        }
    }

.. code:: console

    Nilai dari numbers[0] adalah 10
    Nilai dari numbers[2] adalah 30
    Nilai dari numbers[4] adalah 50

Beradasarkan kode di atas, dilakukan inisialisasi *array* bernama ``numbers`` dengan tipe data ``int`` sebanyak 5 buah. Nilai dari array tersebut adalah ``0``, ``0``, ``0``, ``0``, dan ``0``. Kemudian, dilakukan penetapan nilai pada masing-masing *index* dari *array* tersebut. Sehingga, nilai pada *array* berubah menjadi ``10``, ``20``, ``30``, ``40``, dan ``50``. Kemudian, dilakukan akses nilai dari *array* yang akan ditampilakan ke *console*. Hasil yang muncul pada *console* sesuai dengan yang ditetapkan sebelumnya, bahwa *index* ke-0 adalah 10, dan seterusnya.

Contoh Implementasi *Array*
---------------------------

Dalam membuat sebuah program, *array* digunakan untuk menyimpan beberapa informasi yang sejenis, sehingga tidak perlu membuat variabel satu per-satu. Kemudian, informasi tersebut akan diolah agar mendapatkan hasil akhir yang di inginkan. Contoh pengolahan yang sering dilakukan adalah operasi menambahkan, menghilangkan, dan mengurutkan.

Berikut adalah contoh program untuk menginisialisasikan sebuah *array* dari hasil input pengguna program.

.. code:: java

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            Scanner scan = new Scanner(System.in);
            
            double[] myList = new double[5];
            System.out.print("Masukan " + myList.length + " nilai (dipisahkan dengan spasi): ");
            
            for (int i = 0; i < myList.length; i++) {
                myList[i] = scan.nextDouble();
            }
            scan.nextLine();
            

            System.out.print("Nilai yang dimasukkan adalah ");
            for (int i = 0; i < myList.length; i++) {
                System.out.print(myList[i] + " ");
            }
        }
    }

.. code:: console

    Masukan 5 nilai (dipisahkan dengan spasi): 10 20 30 40 50
    Nilai yang dimasukkan adalah 10.0 20.0 30.0 40.0 50.0 

Berikut adalah contoh program untuk menginisialisasikan sebuah *array* secara acak antara 1 sampai 100.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            double[] myList = new double[5];

            for (int i = 0; i < myList.length; i++) {
                myList[i] = Math.random() * 100 + 1;
            }

            System.out.print("Nilai yang dimasukkan adalah ");
            for (int i = 0; i < myList.length; i++) {
                System.out.print(myList[i] + " ");
            }
        }
    }

.. code:: console

    Nilai yang diacak adalah 15.066742382542174 29.191672930720145 13.798400638026541 28.819978107219022 89.15207046808115


Iterasi *ForEach Array*
-----------------------

Selain dengan *iterasi* ``for`` menggunakan *index*, bahasa pemrograman *Java* telah menyediakan iterasi yang lebih praktis tanpa menggunakan *index*, yang dikenal dengan nama ``foreach``. Berikut adalah *syntax* yang dapat diguankan untuk melakukan ``foreach``.

.. code:: console

    for (tipe_data nama_data : nama_array) {

    }

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String[] words = {"Hello", "World", "Java", "Programming"};

            for (String word : words) {
                System.out.print(word + " ");
            }
        }
    }

.. code:: console

    Hello World Java Programming

Pada kode di atas, dilakukan deklarasi array bernama ``words`` yang berisikan 4 buah kata. Kemudian, dilakukan iterasi untuk setiap kata yang ada di dalam *array* ``words`` menjadi variabel ``word``.
