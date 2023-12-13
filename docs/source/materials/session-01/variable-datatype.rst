Variabel & Tipe Data
====================

Definisi Variabel
-----------------

Variabel dalam bahasa pemrograman adalah sebuah tempat (atau lokasi memori yang diberi nama) untuk menyimpan sebuah nilai yang akan digunakan oleh program pada proses selanjutnya. Nilai pada variabel dapat berubah sesuai dengan keinginan pembuat program atau hasil dari perhitungan program. 

Tipe Data Primitif
------------------

Pada bahasa pemrograman *Java*, setiap variabel wajib memiliki tipe data untuk menentukan jenis nilai yang dapat disimpan di dalam variabel. Secara garis besar, terdapat dua jenis variabel yang biasanya digunakan, yaitu tipe data primitif dan tipe data non-primitif. Bagian ini hanya akan membahas mengenai tipe data primitif saja.

Berikut adalah beberapa contoh tipe data primitif yang biasanya digunakan.

.. list-table::
   :widths: 20 50 30
   :header-rows: 1

   * - Tipe Data Primitif
     - Penjelasan
     - Contoh
   * - *int*
     - Untuk menyimpan bilangan bulat.
     - ``1``, ``5``, ``20``, ``-90``
   * - *double*
     - Untuk menyimpan bilangan desimal (*floating-point*).
     - ``3.6``, ``8.4``, ``14.5``, ``-65.4``
   * - *char*
     - Untuk menyimpan sebuah karakter.
     - ``A``, ``a``, ``Z``, ``z``
   * - *boolean*
     - Untuk menyimpan nilai kebenaran.
     - ``true``, ``false``


Deklarasi Variabel
------------------

Untuk dapat mendeklarasikan sebuah variabel dapat menggunakan *syntax* di bawah ini. Pertama, tentukan tipe data yang akan digunakan. Kedua, tentukan nama variabel yang dibuat. Pastikan nama variabel tersebut unik atau tidak pernah dibuat sebelumnya. Ketiga, gunakan simbol sama dengan (=) untuk memberikan nilai terhadap variabel tersebut. Keempat, tentukan nilai dari variabel tersebut sesuai dengan tipe data yang digunakan.

.. code:: console

  tipe_data nama_variabel = nilai_variabel

Berikut adalah contoh program yang mengimplementasikan beberapa jenis tipe data.

.. code-block:: java 
    
  public class Main {
        public static void main(String[] args) {
            // Mendeklarasikan variable bilangan bulat (integer) dengan nama 'myAge' bernilai 20
            int myAge = 20;

            // Mendeklarasikan variable bilangan desimal (double) dengan nama 'phi' bernilai 3.14
            double phi =  3.14;

            // Mendeklarasikan variable nilai kebenaran (boolean) dengan nama 'isStudent' bernilai true
            boolean isStudent = true;
        }
    }

.. note:: 

    Terdapat aturan yang harus dipenuhi dalam menentukan nama variabel. Berikut adalah aturan-aturan tersebut.

    - Penamaan menggunakan format *lowercase* (huruf kecil). Apabila lebih dari satu kata, maka penamaan menggunakan format *camelcase* (huruf besar untuk setiap awal kata). Contohnya: ``jumlah``, ``jumlahMahasiswa``.
    - Penamaan dapat menggunakan rangkaian karakter termasuk huruf, angka, tanda garis bawah (``_``), dan tanda dolar (``$``). Namun, penamaan tidak dapat dimulai dengan angka. Contohnya: ``data1``, ``_temp``.
    - Penamaan tidak boleh menggunakan kata kunci pada pemrograman. Contohnya: ``int``, ``void``, ``true``.
