Static Vs Dynamic Array 
============================
Tedapat dua  jenis array yaitu array static dan array dinamic. Masing-masing memiliki karakter yang berbeda. 

Static Array 
~~~~~~~~~~~~~~
``Static array`` adalah struktur data yang memiliki ukuran tetap yang ditentukan saat kompilasi. Ukuran statisnya tidak bisa diubah setelah dideklarasikan.
**Karakteristik:**
Ukuran array ditentukan pada saat kompilasi dan tidak bisa diubah.
Memori dialokasikan pada saat program dimulai.


.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            // Static Array dengan ukuran tetap 5
            int[] staticArray = new int[5];

            // Menginisialisasi nilai array
            for (int i = 0; i < staticArray.length; i++) {
                staticArray[i] = i + 1;
            }

            // Mengakses nilai array
            for (int i = 0; i < staticArray.length; i++) {
                System.out.println("Nilai indeks ke-" + i + ": " + staticArray[i]);
            }

        }
    }


.. code:: console 


    Nilai indeks ke-0: 1
    Nilai indeks ke-1: 2
    Nilai indeks ke-2: 3
    Nilai indeks ke-3: 4
    Nilai indeks ke-4: 5


Dynamic Array 
~~~~~~~~~~~~~~~~
``Dynamic Array`` adalah struktur data yang memungkinkan ukurannya berubah secara dinamis saat program berjalan. Ini menggunakan alokasi memori dinamis untuk menyesuaikan ukurannya. ``Dynamic array`` dalam Java umumnya diwakili oleh kelas  ``ArrayList`` dan juga ``vector``, yang memungkinkan kita untuk menambah dan mengurangi elemen secara dinamis.

.. code:: java


    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            // Membuat objek ArrayList untuk menyimpan bilangan bulat
            ArrayList<Integer> dynamicArray = new ArrayList<>();

            // Menambahkan elemen ke dalam ArrayList
            dynamicArray.add(10);
            dynamicArray.add(20);
            dynamicArray.add(30);

            // Menampilkan isi ArrayList
            for (int i = 0; i < dynamicArray.size(); i++) {
                System.out.println("Elemen ke-" + i + ": " + dynamicArray.get(i));
            }
        }
    }

.. code:: console

    Elemen ke-0: 10
    Elemen ke-1: 20
    Elemen ke-2: 30

