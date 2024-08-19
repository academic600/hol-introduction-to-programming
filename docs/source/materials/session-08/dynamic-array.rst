*Dynamic Array*
================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Sebelumnya, telah dibahas mengenai *array* dan *multidimentional array*. Kedua hal tersebut tergolong sebagai *static array*, karena ukurannya tidak dapat berubah-ubah sewaktu program berjalan. Oleh karena itu, bahasa pemrograman *Java* membuat *dynamic array*, yakni *array* yang ukurannya dapat berubah-ubah sesuai dengan kebutuhan saat program berjalan. 

Pada bagian ini hanya akan dibahas dua buah *dynamic array* yang sering digunakan, yaitu ``Vector`` dan ``ArrayList``. Perbedaan antara kedua dynamic array tersebut adalah sebagai berikut.

.. list-table::
   :widths: 20 40 40
   :header-rows: 1

   * - Perbedaan
     - *Vector*
     - *ArrayList*
   * - Sinkronisasi
     - Akses secara otomatis disinkronisasikan (*thread-safe*).
     - Akses tidak disinkronisasikan. Apabila ingin disinkronisasikan perlu menggunakan *method* ``synchronizedList()``.
   * - Kinerja
     - Lebih lambat dibandingkan ``ArrayList``, karena akses tersinkronisasi.
     - Lebih cepat dibandingkan ``Vector``.
   * - Kapasitas
     - Otomatis menambahkan kapasitas sebesar dua kali lipat (100%).
     - Otomatis menambahkan kapasitas sebesar setengah kali lipat (50%).
