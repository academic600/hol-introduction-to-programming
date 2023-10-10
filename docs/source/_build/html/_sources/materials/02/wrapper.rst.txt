Wrapper class
==============

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
