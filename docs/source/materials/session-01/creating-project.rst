Pembuatan *Java Project*
========================


.. TODO: Tambahkan cara membuat project Java di Eclipse.

Cara Membuat Project Java
~~~~~~~~~~~~~~~~~~~~~~~~~~
**STEP 1** 

Pilih direktori yang menyimpan project kalian

.. image:: /images/01/directory.jpg

**STEP 2**

Buatlah projek java baru dengan cara:

``Klik file``, lalu pilih ``new``, dan pilih ``java project``

.. image:: /images/01/homepage.jpg

.. image:: /images/01/create-java-project.jpg


**STEP 3**

Berikan nama pada project lalu klik finish.

.. image:: /images/01/create0project.jpg

Cara membuat Class 
~~~~~~~~~~~~~~~~~~~
**STEP 1**

``Klik kanan`` pada project java yang telah terbuat, pilih ``new`` lalu pilih ``class``
atau bisa menggunakan short cut ``alt + shift + n`` lalu pilih ``c``

.. image:: /images/01/create-class.jpg

**STEP 2**

Berikan ``nama class``, lalu namma package (optional) jika tidak diberi nama maka java class akan berada pada ``package default``.
``Pilih jenis modifier`` class yang kalian butuhkan, lalu pilih juga main method , setelah itu ``klik finish``.

.. TODO: Tambahkan cara menjalankan project Java di Eclipse.

Cara Menjalankan Project Java di Eclipse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Dalam eclipse kita bisa menjalankan project dengan cara menekan tombol run.
Setelah compile maka akan di lakukan run untuk melihat hasil dari implementasi code kita. 
Run pada java berfungsi untuk mengeksekusi code kita dan menampilakan suatu output. 
Biasanya pada java kita menjalankan dengan menekan tombol run 
untuk short cut pada keyboard kita bisa menggunakan ``F11``

.. image:: /images/session-01/run.jpg
  
.. TODO: Tambahkan penjelasan menu atau tab yang sering digunakan pada Eclipse.


Menu atau Tab yangs Sering Digunakan Pada Eclipse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. **Package Explorer**: Menampilkan struktur proyek Anda dan berbagai file yang terkait. Anda dapat mengorganisir, membuat, dan mengelola file di sini.
   
   .. image:: /images/01/package-explorer.jpg

2. **Editor Tab**: Setiap kali Anda membuka file untuk diedit, tab ini menampilkan konten dari file tersebut. Ini adalah tempat di mana Anda menulis dan mengedit kode.
   
   .. image:: /images/01/editor-tab.jpg

3. **Outline**: Memberikan pandangan keseluruhan dari struktur kode di file yang sedang diedit, menampilkan fungsi, variabel, dan bagian penting lainnya dalam file tersebut.
   
   .. image:: /images/01/outline.jpg

4. **Console**: Menampilkan output dari program yang dijalankan dan pesan kesalahan (error) jika ada.
   
   .. image:: /images/01/console.jpg

5. **Toolbar**: Berisi ikon-ikon yang memberikan akses cepat ke fungsi-fungsi umum seperti menjalankan program, mengompilasi, debug, dan lainnya.
   
   .. image:: /images/01/toolbar.jpg

6. **Menu Bar**: Berisi menu-menu utama seperti File, Edit, View, Project, Run, Window, dan lainnya. Di sini Anda dapat menemukan akses ke banyak fungsi dan pengaturan penting dalam Eclipse.
   
   .. image:: /images/01/menu-bar.jpg



Method Utama (*Public Static Void Main*)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. TODO: Tambahkan penjelasan mengenai public static void main() [halaman 35].

.. image:: /images/01/main-method.jpg

.. image:: /images/01/hello-wolrd.jpg

Program dieksekusi dari ``main mehtod``. Sebuah kelas dapat berisi beberapa metode. ``main method`` merupakan method utama
yang menjadi titik masuk di mana program memulai eksekusinya.
Metode utama dalam program ini berisi pernyataan System.out.println. Pernyataan ini menampilkan string Hello world to Java di konsol (baris 4).

*Scope* 
~~~~~~~~
Scope merupakan cakupan sebuah kode program. 

Sebuah pasangan tanda kurung kurawal dalam sebuah program membentuk blok yang mengelompokkan komponen-komponen program. Dalam Java, setiap blok dimulai dengan kurung kurawal pembuka ({) dan diakhiri dengan kurung kurawal penutup (}). 

Contoh Scope atau Blok : 

.. image:: /images/01/scope.jpg



.. TODO: Tambahkan penjelasan scope code [halaman 35].
.. TODO: Tambahkan penjelasan special characters [halaman 36].

*Special Characters*
~~~~~~~~~~~~~~~~~~~~~~~
``special characters`` merujuk pada karakter-karakter yang memiliki makna khusus dalam konteks bahasa pemrograman.
Di dalam java jika kita terdapat kesalahan dalam memakai special karakter, misal kita lupa ``;`` pada akhir baris kode kita
maka akan menimbulkan syntax error pada program kita. 

.. list-table::
   :header-rows: 1

   * - *Special Character*
     - Penjelasan
   * - Kurung Kurawal ``{}``
     - untuk memulai dan mengakhiri scope
   * - Kurung buka-tutup ``()``
     - digunakan pada methods
   * - Kurung siku ``[]``
     -  digunakan mendeklarasi array
   * - Petik dua ``""``
     -  digunakan untuk string (huruf/kata/kalimat)
   * - Garis miring dua ``\\``
     - digunakan untuk comment
   * - Titik koma ``;``
     -  digunakan untuk mengakhiri suatu statement