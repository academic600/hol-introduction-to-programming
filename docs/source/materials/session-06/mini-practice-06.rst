Mini Practice 
================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Lakukanlah instruksi pembuatan program dibawah ini dan sesuaikan dengan hasil **output** yang diberikan.

Lakukanlah instruksi pembuatan program dengan menggunakan bahasa *Java*.

- Buatlah sebuah menu sederhana yang berisikan sebagai berikut. 
    - 1. Beli Barang 
    - 2. Retur Barang 
    - 3. Exit 
- Masukkan sebuah **input** untuk **menentukan menu** yang dipilih. 
- Lakukan handle error dengan menggunakan ``try-catch``, jika data yang diinput tidak berupa angka maka lakukan throw error pada ``catch``

*Input* dan *output* ketika data yang dimasukkan tidak sesuai.
---------------

Input 

.. code:: console

    Selamat datang di ZYResto
    ==========================
    1. Beli Barang
    2. Retur Barang
    3. Exit
    >> a


Output 

.. code:: console 

    // ketika salah memasukkan input maka program akan meminta input kembali
    Tolong masukkan angka! // Output error dari hasil catch error pada input


*Input* dan *Output* ketika data yang dimasukkan sesuai.

Input 

.. code:: console 

    Selamat datang di ZYResto
    ==========================
    1. Beli Barang
    2. Retur Barang
    3. Exit
    >> 1

Output 

.. code:: console 
    
    // Output yang ditampilkan ketika memilih menu 1
    Anda memilih menu Beli barang

