Wrapper class
===============

Merupakan kelas pembungkus yang mengelilingi tipe data *primitive*, agar dapat digunakan sebagai objek.

Tujuan : agar bisa digunakan dalam kegiatan yang berhubungan dengan objek 

Berikut Primitive dan Wrapper Class nya : 

.. list-table::
    :header-rows: 1

    * - Primitif
      - *Wrapper Class*
    * - boolean
      - Boolean
    * - byte
      - Byte
    * - char
      - character
    * - int
      - Integer
    * - float
      - Float
    * - double
      - Double
    * - long
      - Long
    * - short
      - Short
  
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



Tipe Data Primitive
-------------------
Berikut beberapa contoh tipe-tipe data di dalam java: 

.. list-table::
    :header-rows: 1

    * - Nama
      - *Range*
      - *Storage size*
    * - byte
      - -2 :sup:`2` to 2 :sup:`2` -1 (-128 to 127)
      - 8-bit
    * - short
      - -2 :sup:`15` to 2 :sup:`2`` -1 (-32768 to 32767)
      - 16-bit
    * - int
      - -2 :sup:`31` to 2 :sup:`31` 1 (-2147483648 to 2147483647)
      - 32-bit
    * - long
      - -2 :sup:`63` to 2 :sup:`63` -1(i.e., -9223372036854775808 to 9223372036854775807)
      - 64-bit
    * - float
      - Negative range: -3.4028235E + 38 to -1.4E -45 , Positive range: 1.4E -45 to 3.4028235E+38
      - 32-bit IEEE 754 
    * - double
      - Negative range: -1.7976931348623157E+308 to -4.9E -324, Positive range: 4.9E -324 to 1.7976931348623157E+308
      - 64-bit IEEE 754

Tipe data di dalam java dibagi menjadi dua yaitu *primitive* dan *non-primitive* 

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


.. note:: 
    **Primitive Vs Wrapper class**

    Wrapper Class digunakan untuk mengonversi tipe primitif menjadi objek dan objek kembali ke tipe primitif sedangkan tipe primitif adalah tipe data yang telah ditentukan yang disediakan oleh bahasa pemrograman Java.
