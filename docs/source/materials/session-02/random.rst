Random
======

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


*Random* merupakan sebuah *class* yang sudah disediakan oleh bahasa pemrograman *Java* untuk mendapatkan bilangan acak. Hal ini sama seperti yang dilakukan oleh *class* ``Math`` dengan *method* ``random()``, namun bisa menambahkan konfigurasi dan bisa mendapatkan bilangan acak berdasarkan tipe data yang diinginkan. Untuk melakukannya dapat digunakan *class* ``Random`` yang berasal dari *package* ``java.utils``. Langkah yang harus dilakukan adalah sebagai berikut.

Pertama, membuat *object* ``Random`` dengan kode di bawah ini.

.. code:: java
    
    Random random = new Random();

Kedua, mendapatkan hasil bilangan acak dengan *method* di bawah ini.

.. list-table::
   :header-rows: 1

   * - *Method*
     - Penjelasan 
   * - nextInt(max)
     - Digunakan untuk menghasilkan bilangan bulat antara 0 (inklusif) sampai max (eksklusif) dengan tipe data *integer*.
   * - nextDouble()
     - Digunakan untuk menghasilkan bilangan desimal antara 0.0 (inklusif) sampai 1.0 (eksklusif) dengan tipe data *double*.   
   * - nextBoolean()
     - Digunakan untuk menghasilkan nilai kebenaran (*boolean*) secara acak. 

Berikut adalah contoh program untuk melakukan *random*.

.. code-block:: java

    import java.util.Random;

    public class Main {
        public static void main(String[] args) {
            Random random = new Random();

            double randomDouble = random.nextDouble();
            System.out.println(randomDouble); // Output: random decimal value between 0.0 (inclusive) until 1.0 (exclusive).

            int randomInt1 = random.nextInt(50);
            System.out.println(randomInt1); // Output: random integer value between 0.0 (inclusive) until 50.0 (exclusive).
            
            int minimum_value = 50;
            int maximum_value = 100;
            int randomInt2 = random.nextInt(maximum_value - minimum_value + 1) + minimum_value;
            System.out.println(randomInt2); // Output: random integer value between minimum_value (inclusive) until maximum_value (exclusive).
        }
    }
