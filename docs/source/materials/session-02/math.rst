Math
====

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


*Math* merupakan sebuah *class* yang sudah disediakan oleh bahasa pemrograman *Java* untuk melakukan perhitungan matematika. *Class* ini sudah menyediakan beberapa *method* yang dapat dipanggil secara langsung, tanpa menginstansiasi object *Math*.

Berikut adalah beberapa *math method* umum yang sering digunakan.

round()
-------

*Method* ``round()`` digunakan untuk membulatkan bilangan desimal menjadi bilangan bulat (dalam tipe data *long*) terdekat.

.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            double number1 = 3.7;
            long rounded1 = Math.round(number1);
            System.out.println(rounded1); // Output: 4

            double number2 = 3.4;
            long rounded2 = Math.round(number2);
            System.out.println(rounded2); // Output: 3
        }
    }

pow(base, exp)
--------------

*Method* ``pow(base, exp)`` digunakan untuk menghitung hasil dari sebuah pangkat. Perhitungannya adalah *paramater* ``base`` dipangkatkan dengan *parameter* ``exp``.

.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            double pow1 = Math.pow(2, 3);
            System.out.println(pow1); // Output: 8.0

            double pow2 = Math.pow(4, 3);
            System.out.println(pow2); // Output: 64.0
        }
    }

random()
--------

*Method* ``random()`` digunakan untuk menghasilkan bilangan desimal acak antara 0.0 (inklusif) sampai 1.0 (eksklusif).

.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            double randomDouble = Math.random();
            System.out.println(randomDouble); // Output: random decimal value between 0.0 (inclusive) until 1.0 (exclusive).

            int minimum_value = 1;
            int maximum_value = 100;
            int randomInt = (int) (Math.random() * (maximum_value - minimum_value + 1) + minimum_value);
            System.out.println(randomInt); // Output: random integer value between minimum_value (inclusive) until maximum_value (exclusive).
        }
    }

ceil(double a)
-----------------

*Method* ``ceil()`` digunakan untuk membulatkan bilangan Double ke bilangan yang lebih besar. 

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            double a = 3.1;
            System.out.println(Math.ceil(a)) // 4.0
        }
    }


floor(double a)
------------

*Method* ``floor()`` digunakan untuk membulatkan bilangan ke angka yang lebih kecil terdekat.

.. code:: java 
    
    public class Main {
        public static void main(String[] args) {
            double a = 4.7; 
            System.out.println(Math.floor(a)); // 4.0
        }
    }


