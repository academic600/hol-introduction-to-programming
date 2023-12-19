Array 
=========
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





.. note:: 

    Ketika memproses elemen-elemen ``array``, seringkali kita akan menggunakan ``loop for`` karena salah satu dari dua alasan berikut:

    - Semua elemen dalam ``array`` memiliki tipe yang sama. Mereka diproses secara merata dengan cara yang sama secara berulang menggunakan sebuah ``loop``.
    - Karena ukuran array diketahui, lebih alami untuk menggunakan ``loop for``.

