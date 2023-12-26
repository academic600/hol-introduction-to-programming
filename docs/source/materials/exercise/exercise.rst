Latihan Soal 
============

Buatlah sebuah program untuk restoran udon bernama *MaERugame Udon* dengan kriteria sebagai berikut.

Program ini memiliki 4 buah menu, yaitu "*Insert Udon Menu*", "*View Udon Menu*", "*Delete Udon Menu*", dan "*Exit*".

.. code:: console

    MaERugame Udon
    ==============
    1. Insert Udon Menu
    2. View Udon Menu
    3. Delete Udon Menu
    4. Exit
    >> 

1. *Insert Udon Menu* 

Pada menu ini, pengguna program akan diminta untuk memasukan menu udon sesuai dengan kriteria berikut.

- **Nama udon**, hanya berisikan *alphabet* yang terdiri dari 3 - 25 huruf dan diakhiri kata "Udon" secara *case-sensitive*.
- **Harga udon**, harus diantara 30.000 - 100.000 secara *inclusive*.
- **Topping udon**, harus diantara "*Tempura*", "*Beef*", atau "*Egg*" secara *case-sensitive*.

Setelah itu, buatlah ID udon secara acak berdasarkan format berikut. ``XX`` merupakan dua huruf pertama dari nama udon dan ``[0-9]`` merupakan angka acak antara 0 - 9.

.. centered:: XX[0-9][0-9][0-9]

Terakhir, masukan menu udon tersebut ke dalam *dynamic array* (*ArrayList* atau *Vector*).

.. code:: console

    Input Udon Name [3-25 characters, alphabetic, ends with 'Udon' case-sensitive]: curry
    Input Udon Name [3-25 characters, alphabetic, ends with 'Udon' case-sensitive]: curry udon
    Input Udon Name [3-25 characters, alphabetic, ends with 'Udon' case-sensitive]: Curry Udon
    Input Udon Pirce [30000-100000]: 10000
    Input Udon Pirce [30000-100000]: 40000
    Input Udon Topping [Tempura|Beef|Egg, case sensitive]: egg
    Input Udon Topping [Tempura|Beef|Egg, case sensitive]: Egg

    Udon menu created succesfully with ID CU898.

2. *View Udon Menu*

Pada menu ini, program akan mengecek apakah pada *dynamic array* terdapat menu udon atau tidak. Apabila belum ada menu udon yang dimasukan, tampilkan pesan sebagai berikut.

.. code:: console

    There is no data, please insert udon menu first.

Sedangkan, apabila sudah ada menu udon yang dimasukan, program akan menampilkan seluruh menu udon yang sudah dimasukan secara *ascending* berdasarkan harga udon.

.. code:: console

    Udon Menu
    ---------
    Menu No 1
    CU898 - Curry Udon (with Egg)
    Rp. 30000

    Menu No 2
    BE273 - Beef Udon (with Beef)
    Rp. 45000

    Menu No 3
    TA232 - Tamago Udon (with Egg)
    Rp. 50000

    Menu No 4
    CO023 - Complete Udon (with Tempura)
    Rp. 67000

3. *Delete Udon Menu*

Pada menu ini, pengguna program akan diminta untuk memasukan menu udon yang akan dihapus berdasarkan index menu. Pastikan index menu yang dimasukan sudah sesuai. Setelah itu, pengguna program akan diminta melakukan konfirmasi penghapusan menu udon dengan memilih antara "Y" atau "n" secara *case-sensitive*. Apabila pengguna program memilih "Y", maka menu udon akan dihapus dari *dynamic array*. Sedangkan, apabila pengguna program memilih "n", maka program akan kembali ke menu utama.

.. code:: console

    Udon Menu
    ---------
    Menu No 1
    CU898 - Curry Udon (with Egg)
    Rp. 30000

    Menu No 2
    BE273 - Beef Udon (with Beef)
    Rp. 45000

    Menu No 3
    TA232 - Tamago Udon (with Egg)
    Rp. 50000

    Menu No 4
    CO023 - Complete Udon (with Tempura)
    Rp. 67000

    Choose Udon Menu [1-4]: 0
    Choose Udon Menu [1-4]: 1

    Are you sure want to delete CU898 - Curry Udon [Y|n, case-sensitive]? Y

    CU898 - Curry Udon deleted succesfully from the menu.
