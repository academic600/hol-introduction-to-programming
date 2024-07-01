Operator Penugasan (*Assignment*)
=================================

Operator penugasan merupakan operator yang digunakan untuk memberikan nilai ke sebuah variabel. Operator ini juga dapat digabungkan dengan operator aritmatika. Berikut adalah contoh operator penugasan yang dapat digunakan.

.. list-table::
   :widths: 20 30 50
   :header-rows: 1

   * - Operator
     - Nama
     - Penjelasan
   * - ``=``
     - Penugasan
     - Untuk memberikan nilai pada sebuah variabel.
   * - ``+=``
     - Penjumlahan
     - Untuk menjumlahkan sebuah variabel dengan variabel atau nilai lainnya.
   * - ``-=`` 
     - Pengurangan
     - Untuk mengurangkan sebuah variabel dengan variabel atau nilai lainnya.
   * - ``*=`` 
     - Perkalian
     - Untuk mengalikan sebuah variabel dengan variabel atau nilai lainnya.
   * - ``/=`` 
     - Pembagian
     - Untuk membagi sebuah variabel dengan variabel atau nilai lainnya.
   * - ``%=`` 
     - Modulo
     - Untuk mencari sisa pembagian sebuah variabel dengan variabel atau nilai lainnya.

Berikut adalah contoh penerapan dari operator penugasan.

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            int x = 3;
            System.out.println("Nilai x = " + x);

            int a = 15;
            a += x; // sama seperti a = a + x
            System.out.println("Hasil penjumlahan (a + x) = " + a);
            
            int b = 15;
            b -= x; // sama seperti b = b - x
            System.out.println("Hasil pengurangan (b - x) = " + b);

            int c = 15;
            c *= x; // sama seperti c = c * x
            System.out.println("Hasil perkalian (c * x) = " + c);
            
            int d = 15;
            d /= x; // sama seperti d = d / x
            System.out.println("Hasil pembagian (d / x) = " + d);
            
            int e = 15;
            e %= x; // sama seperti e = e % x
            System.out.println("Hasil modulo (e % x) = " + e);
        }
    }

.. code:: console

    Nilai x = 3
    Hasil penjumlahan (a + x) = 18
    Hasil pengurangan (b - x) = 12
    Hasil perkalian (c * x) = 45
    Hasil pembagian (d / x) = 5
    Hasil modulo (e % x) = 0
