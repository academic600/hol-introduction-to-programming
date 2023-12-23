Latihan Soal 
===================
Buatlah sebuah program mengenai restoran udon yang berjudu **MaERugame Udon**, restoran ini dibuat untuk membantu pemilik toko mengelola menu udon miliknya. 

Berikut tampilan menu program: 

.. image:: /images/soal/menu-image.jpg

Program diatas terdiri dari beberapa menu, yaitu : 

**1. Insert Udon** 

Pada menu ini user diminta untuk memasukan beberapa keperluan data sesuai dengan kriteria dibawah ini : 

- **Nama Udon** harus berupa *alphabetic*, terdiri dari **2 - 25 huruf**, serta wajib **diakhiri** oleh kata **"Udon"**. 
- **Harga Udon** harus diantara **30000 - 100000** saja.
- **Topping Udon** harus diantara **"Tempura"**, **"Beef"** atau **"Egg"**, dengan **case sensitve**
- Setelah memasukan data diaa=tas, buatlah random ID berdasarkan format berikut: 
  
  .. image:: /images/soal/format-id.jpg

  **YY** adalah **2 huruf pertama** **nama udon** yang dimasukkan, sedagnkan ``[0-9][0-9][0-9]`` adalah angka **random** ``1-10``
- Lalu tambahkan data **udon** ke dalam **Array List / Vector**

.. image:: /images/soal/menu-1.jpg


**2. View Udon Menu**

Pada menu ini  pengguna dapat **melihat** data **udon** yang telah di masukkan ke dalam array list / vector. Jika tidak ada data, lakukan validasi dan tampilkan **"no data"** kepada pengguna.

.. image:: /images/soal/no-data.jpg

Jika ada data maka, tampilkan semua data yang ada di dalam List yang sudah di urutkan dengan **bubble sort** secara **ascending** berdasarkan **udon price** : 

.. image:: /images/soal/view-udon.jpg

**3. Delete Udon Menu**

Pada menu ini pengguna dapat **menghapus** menu **udon** yang sudah dibuat sebelumnya. Hapus menu udon berdasarkan **indeksnya**.

- Validasi **nomor udon** yang dipilih **harus ada**
- Validasi untuk memastikan ingin menghapus data nya atau tidak dengan pilihan **"Y/N"**. Jika pengguna memilih **"Y"** maka data akan di hapus dari list. Jika pengguna memilih **"N"** maka akan muncul pesan **"failed to delete"** yaitu tidak berhasil di hapus.
- **Update** juga **view** nya setelah data di hapus.

.. image:: /images/soal/deleting-udon.jpg




