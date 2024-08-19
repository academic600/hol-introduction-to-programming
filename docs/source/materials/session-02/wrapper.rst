*Wrapper Class*
===============

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Setiap tipe data primitif yang ada pada bahasa pemrograman *Java* memiliki *wrapper class*. Dengan kata lain, *wrapper class* merupakan merupakan tipe data primitif yang dibuat atau dibungkus dalam bentuk *class* sehingga dapat digunakan sebagai *object*. Umumnya tipe data primitif ditulis dalam format huruf kecil, sedangkan *wrapper class* ditulis dalam format huruf kapital. Berikut adalah beberapa contohnya.

.. list-table::
    :header-rows: 1

    * - Primitif
      - *Wrapper Class*
    * - char
      - Character
    * - int
      - Integer
    * - double
      - Double
    * - boolean
      - Boolean

.. note:: 

    Tipe data primitif hanya menyimpan nilai yang diberikan dalam tipe data tertentu. Namun, *wrapper class* dapat menyimpan nilai seperti tipe data primitif dan memiliki *method* yang dapat digunakan mengolah nilai tersebut. 

Berikut adalah contoh penggunaan *wrapper class* untuk *Double*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            Double myDouble = 5.99;
            System.out.println(myDouble.intValue());
        }
    }

.. code:: console
    
    5

Pada baris ke-3 kode diatas, dilakukan deklarasi variabel bernama ``myDouble`` dengan tipe data *Double* yang memiliki nilai desimal 5.99. Pada baris ke-4 kode diatas, dilakukan *output* untuk variabel ``myDouble`` dengan *method* ``intValue``, artinya nilai yang ada pada variabel akan diubah menjadi nilai integer, sehingga hasil yang tampil pada *console* adalah 5 (pembulatan ke bawah).


Setiap wrapper class memiliki method-method nya tersendiri. Beberapa dari method wrapper class ada yang memiliki 
methode yang sama dengan methode lainnya. 

           

