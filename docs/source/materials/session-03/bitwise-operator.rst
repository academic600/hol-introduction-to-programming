Operator Bit (*Bitwise*)
========================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Operator bit adalah operator yang digunakan untuk mengubah nilai dari sebuah bit. Berikut adalah contoh operator bit yang dapat digunakan.

.. list-table::
   :widths: 20 30 50
   :header-rows: 1

   * - Operator
     - Nama
     - Penjelasan
   * - ``&``
     - *AND* (*bitwise*)
     - Apabila kedua bit bernilai 1 akan menghasilkan 0. Apabila salah satu saja atau tidak ada yang bernilai 1 akan menghasilkan 0.
   * - ``|`` 
     - *OR* (*bitwise*)
     - Apabila kedua atau salah satu bit bernilai 1 akan menghasilkan 1. Apabila tidak ada yang bernilai 1 akan menghasilkan 0.
   * - ``^`` 
     - *XOR* (*bitwise*)
     - Apabila kedua bit bernilai berbeda akan menghasilkan 1. Apabila kedua bit bernilai sama akan menghasilkan 0.
   * - ``~`` 
     - *NOT* (*bitwise*)
     - Untuk membalikan nilai kebeneran (*boolean*). Apabila bit bernilai 1 diubah menjadi 0, dan sebaliknya.
   * - ``<<`` 
     - *Shift* Kiri
     - Untuk menggeser bit ke kiri sebanyak yang ditentukan.
   * - ``>>`` 
     - *Shift* Kanan
     - Untuk menggeser bit ke kanan sebanyak yang ditentukan.

Untuk mempermudah penjelasan di atas, berikut adalah tabel kebenaran (*truth table*) yang menunjukan semua kemungkinan *input* dan *output* pada operator bit.

.. list-table::
   :widths: 20 20 20 20 20
   :header-rows: 1

   * - *Input* 1
     - *Input* 2
     - *Output* & (*AND*)
     - *Output* | (*OR*)
     - *Output* ^ (*XOR*)
   * - 1
     - 1
     - 1
     - 1
     - 0
   * - 1
     - 0
     - 0
     - 1
     - 1
   * - 0
     - 1
     - 0
     - 1
     - 1
   * - 0
     - 0
     - 0
     - 0
     - 0

Berikut adalah contoh penerapan dari operator bit.

.. code:: java 

    public class Main {

        public static void main(String[] args) {
            int a = 5;  // Binary: 00000101
            int b = 3;  // Binary: 00000011
            
            // 00000101
            // 00000011
            // -------- &
            // 00000001  (bernilai 1)
            System.out.println("a & b = " + (a & b));
            
            // 00000101
            // 00000011
            // -------- |
            // 00000111  (bernilai 7)
            System.out.println("a | b = " + (a | b));
            
            // 00000101
            // 00000011
            // -------- |
            // 00000110  (bernilai 6)
            System.out.println("a ^ b = " + (a ^ b));
            
            // 00000101
            // -------- ~
            // 11111010  (bernilai -6)
            System.out.println("~a = " + (~a));
            
            // 00000101
            // -------- << 2
            // 00010100  (bernilai 20)
            System.out.println("a << 2 = " + (a << 2));
            
            // 00000101
            // -------- >> 1
            // 00000010  (bernilai 2)
            System.out.println("a >> 1 = " + (a >> 1));
        }
    }

.. code:: console

    a & b = 1
    a | b = 7
    a ^ b = 6
    ~a = -6
    a << 2 = 20
    a >> 1 = 2
