*Exception Handling*
====================

Pada bahasa pemrograman *Java*, *exception handling* adalah proses untuk menangani kesalahan pada saat program dijalankan (*exception*). Ketika terjadi kesalahan tersebut, biasanya akan terjadi *crash* atau program yang berhenti secara tiba-tiba. Contoh kesalahan yang sering ditemui adalah pembagian oleh nol, akses ke data yang tidak tersedia, dan masalah koneksi jaringan. Oleh karena itu, kesalahan tersebut dapat dan perlu di validasikan agar program dapat berjalan dengan baik.

Salah satu cara untuk melakukan *exception handling* adalah menggunakan ``try-catch``. Berikut adalah *syntax* yang dapat digunakan dalam membuat ``try-catch``.

**Syntax**

.. code:: console

    try {
        <kode yang ingin di validasikan>
    }
    catch(Exception e) {
        <kode yang dijalankan ketika error>
    }

Berikut adalah contoh implementasi ``try-catch`` ketika mengakses data dalam bentuk *array* yang tidak tersedia.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            try {
                int[] myNumbers = {1, 2, 3};
                System.out.println(myNumbers[10]);
            } catch (Exception e) {
                System.out.println("Data tidak ditemukan");
            }
        }   
    }


.. code:: console

    Data tidak ditemukan

Apabila tidak menggunakan ``try-catch``, pada *console* akan muncul *error* sebagai berikut.

.. code:: console

    Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 10 out of bounds for length 3
        at Main.main(Main.java:5)

Berdasarkan kode di atas, terdapat sebuah *array* dengan nama ``myNumbers`` yang hanya memiliki 3 buah data. Karena hanya ada 3 buah data saja, artinya *index* yang dapat diakses hanya sampai *index* ke-2 (karena *index* dimulai dari 0). Pada kode ingin dilakukan *output* untuk *index* ke-10 yang tidak didefinisikan, sehingga muncul *error*. Karena kode sudah di validasikan dengan ``try-catch``, maka ketika kode yang berada di dalam *scope* ``try`` *error*, yang dijalankan adalah kode yang ada di dalam *scope* ``catch``.
