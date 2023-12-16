Operator Logika (*Logical*)
===========================

Operator logika merupakan operator yang digunakan untuk menggabungkan atau mengubah nilai kebenaran (*boolean*). Biasanya operator logika digunakan pada kondisi atau variabel dengan tipe data *boolean*. Berikut adalah contoh operator logika yang dapat digunakan.

.. list-table::
   :widths: 20 30 50
   :header-rows: 1

   * - Operator
     - Nama
     - Penjelasan
   * - ``&&``
     - *AND*
     - Apabila kedua operand bernilai *true* akan menghasilkan *true*. Apabila salah satu saja atau tidak ada yang bernilai *true* akan menghasilkan *false*.
   * - ``||`` 
     - *OR*
     - Apabila kedua atau salah satu operand bernilai *true* akan menghasilkan *true*. Apabila tidak ada yang bernilai *true* akan menghasilkan *false*.
   * - ``!`` 
     - *NOT*
     - Untuk membalikan nilai kebeneran (*boolean*). Apabila operand bernilai *true* diubah menjadi *false*, dan sebaliknya.

Untuk mempermudah penjelasan di atas, berikut adalah tabel kebenaran (*truth table*) yang menunjukan semua kemungkinan *input* dan *output* pada operator logika.

.. list-table::
   :widths: 25 25 25 25
   :header-rows: 1

   * - *Input* 1
     - *Input* 2
     - *Output* && (*AND*)
     - *Output* || (*OR*)
   * - *true*
     - *true*
     - *true*
     - *true*
   * - *true*
     - *false*
     - *false*
     - *true*
   * - *false*
     - *true*
     - *false*
     - *true*
   * - *false*
     - *false*
     - *false*
     - *false*

Berikut adalah contoh penerapan dari operator logika.

.. code:: java 

    public class Main {

        public static void main(String[] args) {
            int a = 10;
            int b = 20;
            
            System.out.println("a dan b adalah bilangan genap (a % 2 == 0 && b % 2 == 0) = " + (a % 2 == 0 && b % 2 == 0));
            System.out.println("a dan b bernilai 10 (a == 10 && b == 10) = " + (a == 10 && b == 10));
            
            System.out.println("a atau b bernilai 10 (a == 10 || b == 10) = " + (a == 10 || b == 10));
            System.out.println("a atau b bernilai 0 (a == 0 || b == 0) = " + (a == 0 || b == 0));
            
            boolean c = true;
            System.out.println("Kebalikan dari c (!c) = " + !c);
            System.out.println("Kebalikan dari hasil a bernilai 10 (!(a == 10)) = " + !(a == 10));
        }
    }

.. code:: console

    a dan b adalah bilangan genap (a % 2 == 0 && b % 2 == 0) = true
    a dan b bernilai 10 (a == 10 && b == 10) = false
    a atau b bernilai 10 (a == 10 || b == 10) = true
    a atau b bernilai 0 (a == 0 || b == 0) = false
    Kebalikan dari c (!c) = false
    Kebalikan dari hasil a bernilai 10 (!(a == 10)) = false
