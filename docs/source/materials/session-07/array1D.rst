Array 
===========
*Array* digunakan untuk menyimpan kumpulan data, tetapi seringkali kita menemukan lebih berguna untuk memandang ``array`` sebagai kumpulan variabel dengan tipe yang sama. 
Kita mendeklarasikan satu variabel array seperti numbers dan menggunakan ``numbers[0], numbers[1], . . . ,`` dan ``numbers[99]`` untuk merepresentasikan variabel-variabel individual tersebut.
Setiap array memiliki index yang di mulai dari ``0``


Deklarasi *Array*
~~~~~~~~~~~~~~~~~~~~~~
Untuk menggunakan ``array`` dalam sebuah program, Anda harus mendeklarasikan sebuah variabel yang merujuk pada array dan menentukan tipe elemen dari ``array`` tersebut. Berikut adalah sintaks untuk mendeklarasikan variabel ``array``:

.. code:: console

    tipeData [] namaVariable = 





Pembuatan *Array*
~~~~~~~~~~~~~~~~~~~~


Tidak seperti deklarasi untuk variabel tipe data *primitif*, deklarasi variabel ``array`` tidak mengalokasikan ruang di memori untuk ``array``,
tetapi hanya menciptakan lokasi penyimpanan untuk referensi ke sebuah ``array``. Jika sebuah variabel tidak berisi referensi ke ``array``, nilai dari variabel tersebut adalah ``null``.
kita tidak dapat menetapkan elemen-elemen ke dalam ``array`` kecuali ``array`` tersebut sudah dibuat. Setelah variabel array dideklarasikan,
Kita dapat membuat sebuah ``array`` dengan menggunakan operator ``new`` dan menetapkan referensinya ke variabel dengan sintaks berikut:

.. code:: console

    tipeData [] namaVariabel = new tipeData[ukuranArray];


Mengakses Nilai *Array*
~~~~~~~~~~~~~~~~~~~~~~~~~~

Elemen-elemen ``array`` diakses melalui ``indeks``. Indeks ``array`` dimulai dari 0.
Berikut sintaks mengakses nilai array: 

.. code:: console

    namaVariavbelArray [index];


.. code:: java

    public class Main {

        public static void main(String[] args) {
            int[] angka = new int[5];

                // Menetapkan nilai ke dalam array
                angka[0] = 10;
                angka[1] = 20;
                angka[2] = 30;
                angka[3] = 40;
                angka[4] = 50;

                // Mengakses dan mencetak nilai dari array
                System.out.println("Nilai dari angka[0]: " + angka[0]);
                System.out.println("Nilai dari angka[2]: " + angka[2]);
                System.out.println("Nilai dari angka[4]: " + angka[4]);

        }

    }

.. code:: console

    Nilai dari angka[0]: 10
    Nilai dari angka[2]: 30
    Nilai dari angka[4]: 50

*Array initializer*
~~~~~~~~~~~~~~~~~~~~~
Java memiliki notasi singkat, yang dikenal sebagai ``array initializer``, yang menggabungkan deklarasi, penciptaan, dan inisialisasi array dalam satu pernyataan menggunakan sintaks berikut:

.. code:: console

    tipeData[] namaVariabel = {value0, value1, ..., valuek};


.. code:: java

    double[] myList = {1.9, 2.9, 3.4, 3.5};


Memproses *Array*
~~~~~~~~~~~~~~~~~~~~~~
Memproses ``array`` adalah pengolahan atau manipulasi data dalam ``array``. Ini mencakup berbagai operasi seperti menambahkan, menghapus, mencari nilai tertentu, mengurutkan, atau melakukan perubahan lain pada elemen-elemen dalam ``array``.

**Insialisasi array dengan nilai input :**
   
.. code:: java

    import java.util.Scanner;

    public class Main {

        public static void main(String[] args) {
            Scanner input = new Scanner(System.in);
            double[] myList = new double[5];
                System.out.print("Masukkan " + myList.length + " nilai: ");
                
                for (int i = 0; i < myList.length; i++) {
                    myList[i] = input.nextDouble();
                }
                

                System.out.println("Nilai yang dimasukkan:");
                for (int i = 0; i < myList.length; i++) {
                    System.out.print(myList[i] + " ");
                }
                    
        }



    }


.. code:: console

    Masukkan 5 nilai: 1 2 3 4 5
    Nilai yang dimasukkan:
    1.0 2.0 3.0 4.0 5.0 

**Inisialisasi array dengan nilai acak:**

Loop berikut menginisialisasi array myList dengan nilai acak antara 0.0 dan 100.0, tetapi kurang dari 100.0:

.. code:: java

    public class Main {

	  public static void main(String[] args) {
	        double[] myList = new double[5];

	        for (int i = 0; i < myList.length; i++) {
	            myList[i] = Math.random() * 100;
	        }

	        System.out.println("Nilai acak antara 0.0 dan 100.0:");
	        for (int i = 0; i < myList.length; i++) {
	            System.out.print(myList[i] + " ");
	        }
	    }


    }

.. code:: console

    Nilai acak antara 0.0 dan 100.0:
    17.09124077714349 89.41099356774917 32.70821348268378 16.41171221784835 47.1386890790769 


Iterasi foreach Array
~~~~~~~~~~~~~~~~~~~~~~~~~

Java mendukung for loop yang praktis, dikenal sebagai foreach loop, yang memungkinkan Anda untuk menelusuri array secara berurutan tanpa menggunakan variabel indeks.

.. code:: console

    for (tipeData variabel : namaArray atau namaKoleksi) {
        // melakukan sesuatu dengan variabel
    }


.. code:: java

    public class Main {
        public static void main(String[] args) {
            String[] words = {"Hello", "World", "Java", "Programming"};

            // Menggunakan foreach loop untuk menampilkan setiap elemen dalam array string
            System.out.println("Kata dalam array:");
            for (String word : words) {
                //menambagkan spasi ke setiap kata yang di print
                System.out.print(word + " ");
            }
        }
    }

.. code:: console

    Kata dalam array:
    Hello World Java Programming



.. note:: 

    Ketika memproses elemen-elemen ``array``, seringkali kita akan menggunakan ``loop for`` karena salah satu dari dua alasan berikut:

    - Semua elemen dalam ``array`` memiliki tipe yang sama. Mereka diproses secara merata dengan cara yang sama secara berulang menggunakan sebuah ``loop``.
    - Karena ukuran array diketahui, lebih alami untuk menggunakan ``loop for``.

