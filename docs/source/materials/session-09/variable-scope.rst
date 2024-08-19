*Scope* Variabel
================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Kita juga sudah mempelajari mengenai *scope* pada sebuah kode di materi sebelumnya. Namun, pada materi ini akan dibahas lebih detail mengenai *scope*. Hal ini penting dipelajari untuk mengentahui pada bagian mana variabel atau *method* dapat diakses atau digunakan.

*Block Scope*
-------------

Variabel yang di deklarasikan pada sebuah *block* hanya dapat digunakan dalam *block* tersebut saja. Contoh block yang dimaksud adalah *block* ``if``, ``for``, ``while``, ``try``, dan sebagainya.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int x = 10; // Variabel x dapat digunakan dimanapun di dalam method ini
            if (x > 5) {
                int y = 20; // Variabel y hanya dapat digunakan di dalam block if
                System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam method ini
                System.out.println(y); // Bukti bahwa variabel y dapat digunakan, karena masih di dalam scope if
            }
            System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam method ini
            // System.out.println(y); // Error, karena variabel y tidak dapat digunakan di luar scope if
        }
    }

.. code:: console 

    10
    20
    10

.. note:: 

    Apabila ingin membuat variabel dapat diakses dalam seluruh *method*, deklarasikan variabel di dalam *scope method* dan di luar dari *block* apapun, seperti pada variabel ``x``.

*Method Scope*
--------------

Variabel yang di deklarasikan pada sebuah *method* hanya dapat digunakan dalam *method* tersebut saja.

.. code:: java

    public class Main {
        public void example1() {
            int x = 10; // Variabel x dapat digunakan dimanapun di dalam method ini
            if (true) {
                System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam method ini
            }
        }
        
        public void example2() {
            int y = 20; // Variabel y dapat digunakan dimanapun di dalam method ini
            if (true) {
                System.out.println(y); // Bukti bahwa variabel y dapat digunakan, karena masih di dalam method ini
                // System.out.println(x); // Error, karena variabel x di deklerasikan pada method yang berbeda
            }
        }
        
        public Main() {
            example1();
            example2();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    10
    20

Variabel Global
---------------

Sesuai dengan namanya, variabel global merupakan variabel yang dapat diakses secara global, dari manapun. Variabel global dapat digunakan pada *block* dan *method* manapun, tanpa terkecuali. Deklarasi variabel global ini dilakukan pada *scope class* dan diluar dari *method* apapun.

.. code:: java

    public class Main {
        int x = 10; // Variabel x merupakan variabel global yang dapat digunakan di manapun
        
        public void example1() {
            System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam class ini
        }
        
        public void example2() {
            System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam class ini
        }
        
        public Main() {
            System.out.println(x); // Bukti bahwa variabel x dapat digunakan, karena masih di dalam class ini
            example1();
            example2();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }


.. code:: console

    10
    10
    10
