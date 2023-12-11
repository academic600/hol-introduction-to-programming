Wrapper class
===============

Merupakan kelas pembungkus yang mengelilingi tipe data primitive, agar dapat digunakan sebagai objek.

Tujuan : agar bisa digunakan dalam kegiatan yang berhubungan dengan objek 

Berikut Primitive dan Wrapper Class nya : 

.. image:: /images/02/Wrapper-Class.png

Example
-------
.. code:: java

    public class Main(){
    
        public static void main(String[] args) {
            Integer myInt = 5;
            Double myDouble = 5.99;
            Character myChar = 'A';
            System.out.println(myInt);
            System.out.println(myDouble);
            System.out.println(myChar);

        }
    
    }

.. code:: console
    
    5
    5.99
    A


Primitive Vs Wrapper class
--------------------------
Wrapper Class digunakan untuk mengonversi tipe primitif menjadi objek dan objek kembali ke tipe primitif sedangkan tipe primitif adalah tipe data yang telah ditentukan yang disediakan oleh bahasa pemrograman Java.

Tipe Data Primitive
-------------------
Berikut beberapa contoh tipe-tipe data di dalam java: 

image:: /images/01/type-data.jpg

Tipe data di dalam java dibagi menjadi dua yaitu primitive dan non-primitive 

.. .. image:: /images/01/tipe-data.jpg
..     :width: 500

.. list-table:: Perbedaan Primitive dan Non-primitive
   :widths: 10 45 45
   :header-rows: 1
   

   * - Perbedaan
     - Primitive 
     - Non-primitive
   * - Passing Data
     - Menyimpan nilai yang sebenarnya (pass by value) dalam sebuah method
     - Menyimpan Alamat ke alokasi memori (pass by reference) dalam sebuah method
   * - Nilai Default
     - memiliki nilai default apabila tidak di inisialisasi, cth : int = 0
     - Memiliki nilai default “null”
   * - Penulisan
     - Di awali dengan huruf kecil 
     - Di awali dengan huruf besar