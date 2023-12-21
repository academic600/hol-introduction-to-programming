Vector 
=============
``Vector`` dalam *Java* adalah kelas yang ada dalam paket ``java.util`` yang mewakili sebuah koleksi objek yang bertindak seperti array dinamis.
Mirip dengan ``ArrayList``, tetapi beberapa perbedaan kecil dalam perilakunya dan penggunaannya.

Berikut sintaks vector : 

.. code:: console

    Vector<tipeData> namaVector = new Vector<>();

Karakteristik Vector 
~~~~~~~~~~~~~~~~~~~~~~~
- **Alokasi Dinamis**: Mirip dengan ArrayList, Vector juga dapat memperluas ukurannya secara otomatis ketika elemen baru ditambahkan.
- **Thread-Safe**: Vector memiliki metode yang bersifat sinkronized atau thread-safe secara alami, membuatnya lebih cocok untuk lingkungan multithreading dibandingkan dengan ArrayList.
- **Operasi pada Elemen**: Menyediakan berbagai metode untuk menambah, menghapus, mengakses, dan mengubah elemen dalam vektor, seperti add, remove, get, set, dan lainnya.

Operasi pada vector
~~~~~~~~~~~~~~~~~~~~
Pada ``vector`` mirip dengan ``array list`` untuk menambahkan data kita bisa memakai ``.add()``, untuk menghapus data kita bisa memakai ``.remove()``, lalu mendelete sintaks nya. lalu unut mendapatkan nilai ``vector`` kita bisa pakai method ``.get()``

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            // Membuat objek Vector yang menyimpan tipe data String
            Vector<String> bookVector = new Vector<>();

            // Menambahkan elemen ke dalam Vector
            bookVector.add("Java Programming");
            bookVector.add("Data Structures");
            bookVector.add("Algorithms");

            // Mengakses elemen dalam Vector
            String elementAtIndex1 = bookVector.get(1);
            System.out.println("Elemen pada indeks 1: " + elementAtIndex1);

            // Menghapus elemen dari Vector
            bookVector.remove(1);

            // Menampilkan isi Vector setelah penghapusan
            for (int i = 0; i < bookVector.size(); i++) {
                System.out.println("Elemen ke-" + i + ": " + bookVector.get(i));
            }
        }
    }


.. code:: console


    Elemen pada indeks 1: Data Structures
    Elemen ke-0: Java Programming
    Elemen ke-1: Algorithms


Vector Vs ArrayList 
~~~~~~~~~~~~~~~~~~~~~~

+-----+--------------------------------------+--------------------------------------+
| No. | Array List                           | Vector                               |
+=====+======================================+======================================+
| 1   | ArrayList tidak disinkronisasi.      | Vector disinkronisasi.               |
+-----+--------------------------------------+--------------------------------------+
|| 2  || Vector menambah kapasitas sebesar   ||                                     |
||    || 50% dari ukuran array saat jumlah   || 100%, menggandakan ukuran array     |
||    || elemen melebihi kapasitasnya.       || saat jumlah total elemen melebihi   |
||    ||                                     || kapasitasnya.                       |
+-----+--------------------------------------+--------------------------------------+
|| 3  || ArrayList lebih cepat karena tidak  || Vector lebih lambat karena          |
||    || disinkronisasi.                     || disinkronisasi, artinya di          |
||    ||                                     || lingkungan multithreading, Vector   |
||    ||                                     || menahan thread lain dalam keadaan   |
||    ||                                     || runnable atau non-runnable sampai   |
||    ||                                     || thread saat ini melepaskan kunci    |
||    ||                                     || objeknya.                           |
+-----+--------------------------------------+--------------------------------------+
|| 4  || Kinerja ArrayList lebih tinggi.     ||	Kinerja Vector lebih rendah.        |
+-----+--------------------------------------+--------------------------------------+
| 5   | Memungkinkan multiple threads.       | Hanya satu thread yang diizinkan.    |
+-----+--------------------------------------+--------------------------------------+
|| 6  || ArrayList bukanlah kelas warisan    || Vector adalah kelas warisan         |
||    || (legacy class). Diperkenalkan dalam || (legacy class).                     |
||    || JDK 1.2.                            ||                                     |
+-----+--------------------------------------+--------------------------------------+
