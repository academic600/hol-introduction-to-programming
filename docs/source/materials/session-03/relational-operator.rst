Operator Perbandingan (*Relational*)
====================================

Operator perbandingan merupakan operator yang digunakan untuk membandingkan dua buah operand. Berikut adalah contoh operator perbandingan yang dapat digunakan.

.. list-table::
   :widths: 20 30 50
   :header-rows: 1

   * - Operator
     - Nama
     - Penjelasan
   * - ``==``
     - Sama Dengan
     - Untuk mengecek apakah dua buah operand tersebut sama.
   * - ``!=`` 
     - Tidak Sama Dengan
     - Untuk mengecek apakah dua buah operand tersebut tidak sama.
   * - ``>`` 
     - Lebih Besar
     - Untuk mengecek apakah operand kiri lebih besar dari operand kanan.
   * - ``>=`` 
     - Lebih Besar Sama Dengan
     - Untuk mengecek apakah operand kiri lebih besar atau sama dengan operand kanan. 
   * - ``<`` 
     - Lebih Besar
     - Untuk mengecek apakah operand kiri lebih kecil dari operand kanan.
   * - ``<=`` 
     - Lebih Besar Sama Dengan
     - Untuk mengecek apakah operand kiri lebih kecil atau sama dengan operand kanan. 

Berikut adalah contoh penerapan dari operator perbandingan.

.. code:: java 

    public class Main {

        public static void main(String[] args) {
            int a = 12;
            int b = 4;
            
            System.out.println("a sama seperti b (a == b) = " + (a == b));
            System.out.println("a tidak sama seperti b (a != b) = " + (a != b));
            System.out.println("a lebih besar dari b (a > b) = " + (a > b));
            System.out.println("a lebih besar atau sama dengan b (a >= b) = " + (a >= b));
            System.out.println("a lebih kecil dari b (a < b) = " + (a < b));
            System.out.println("a lebih kecil atau sama dengan b (a <= b) = " + (a <= b));
        }
    }

.. code:: console

    a sama seperti b (a == b) = false
    a tidak sama seperti b (a != b) = true
    a lebih besar dari b (a > b) = true
    a lebih besar atau sama dengan b (a >= b) = true
    a lebih kecil dari b (a < b) = false
    a lebih kecil atau sama dengan b (a <= b) = false
