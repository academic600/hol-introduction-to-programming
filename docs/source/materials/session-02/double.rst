*Double Method*
====================

*Double* merupakan tipe data untuk menyimpan bilangan decimal. Karena *Double* merupakan wrapper class yang sudah disediakan oleh *Java*, oleh sebab itu, terdapat berbagai build-in function yang bisa digunakan.

Berikut adalah beberapa *string method* umum yang sering digunakan.


compare(int x, int y)
------------------

*Method* ``compare(int x, int y)`` digunakan untuk membandingkan nilai mana yang lebih besar diantara 2 bilangan yang dibandingkan di dalam parameter. nilai yang direturn adalah, -1, 0, dan 1. Akan return 0 jika kedua data bernilai sama, akan return -1 jika x lebih kecil dari y, dan akan return 1 jika nilai x lebih besar dari y.

.. code:: java 
    public class Main {
        public static void main(String[] args) {
            System.out.println(Double.compare(1.0, 2.0)) // Output: -1
        }
    }


sum(double x, double y)
---------------------
*Method* ``sum(double x, double y)`` digunakan untuk melakukan kalkulasi penjumlahan diantara 2 bilangan.

.. code:: java 
    public class Main {
        public static void main(String[] args) {
            System.out.println(Double.sum(3.5, 1.2)) // Output: 4.7
        }
    }


max(double x, double y)
-------------------------

*Method* ``max(double x, double y)`` digunakan untuk menentukan nilai *Double* yang terbesar diantara dua nilai *Double* yang dimasukkan.

.. code:: java 
    public class Main {
        public static void main(String[] args) {
            System.out.println(Double.max(3.4, 5.6)) // Output: 5.6
        }
    }


parseDouble(String d)
-----------------------
*Method* ``parseDouble(String d)`` bisa digunakan untuk mengubah tipe data *String* yang dapat dikoenversi menjadi *Double*. 

.. code:: java 
    public class Main {
        public static void main(String[] args) {
            System.out.println(Double.parseDouble("3.0")) // Output: 3.0 (Double)
        }
    }


toString()
----------------

*Method* ``toString()`` digunakan untuk mengubah tipe data *Double* menjadi *String*. 

.. code:: java 
    public class Main {
        public static void main(String[] args) {
            System.out.println(Double.toString(2.1)); // Output: 2.1 (String)
        }
    }