Operator Aritmatika (*Arithmetic*)
==================================

Operator aritmatika merupakan operator yang digunakan untuk melakukan operasi dasar matematika pada operand bilangan bulat ataupun desimal. Berikut adalah contoh operator aritmatika yang dapat digunakan.

.. list-table::
   :widths: 20 30 50
   :header-rows: 1

   * - Operator
     - Nama
     - Penjelasan
   * - ``+``
     - Penjumlahan
     - Untuk menjumlahkan dua buah operand.
   * - ``-`` 
     - Pengurangan
     - Untuk mengurangkan operand pertama dengan operand kedua.
   * - ``*`` 
     - Perkalian
     - Untuk mengalikan dua buah operand. 
   * - ``/`` 
     - Pembagian
     - Untuk membagi operand pertama dengan operand kedua.
   * - ``%`` 
     - Modulo
     - Untuk mencari sisa pembagian operand pertama dengan operand kedua.
  
Berikut adalah contoh penerapan dari operator aritmatika.

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            int a = 15;
            int b = 3;
            
            System.out.println("Hasil penjumlahan (a + b) = " + (a + b));
            System.out.println("Hasil pengurangan (a - b) = " + (a - b));
            System.out.println("Hasil perkalian (a * b) = " + (a * b));
            System.out.println("Hasil pembagian (a / b) = " + (a / b));
            System.out.println("Hasil modulo (a % b) = " + (a % b));
        }
    }

.. code:: console

    Hasil penjumlahan (a + b) = 18
    Hasil pengurangan (a - b) = 12
    Hasil perkalian (a * b) = 45
    Hasil pembagian (a / b) = 5
    Hasil modulo (a % b) = 0

Selain itu, pada bahasa pemrograman Java, terdapat cara mudah untuk menambahkan atau mengurangi nilai variabel sebanyak satu. Untuk menambahkan nilai (*increment*) dapat menggunakan tanda ``++``. Sedangkan, untuk mengurangi nilai (*decrement*) dapat menggunakan tanda ``--``.

Terdapat dua jenis penggunaan operator ini, yaitu *prefix* dan *postfix*. Perbedaannya terletak pada kapan dilakukannya penjumlahan atau pengurangan tersebut, hasil akhir keduanya akan tetap sama.

- *Prefix* atau *pre-increment*/*pre-decrement*, artinya penambahan atau pengurangan nilai dilakukan terlebih dahulu sebelum melakukan suatu operasi.
- *Postfix* atau *post-increment*/*post-decrement*, artinya penambahan atau pengurangan nilai dilakukan setelah melakukan suatu operasi.

.. code:: java

    public class Main {
      public static void main(String[] args) {
        int a = 10;
        System.out.println("Pre-increment (++a) = " + (++a));
        System.out.println("Hasil a = " + a);

        int b = 10;
        System.out.println("Post-increment (b++) = " + (b++));
        System.out.println("Hasil b = " + b);
        
        int c = 10;
        System.out.println("Pre-decrement (--c) = " + (--c));
        System.out.println("Hasil c = " + c);

        int d = 10;
        System.out.println("Post-decrement (d--) = " + (d--));
        System.out.println("Hasil d = " + d);
      } 
    }

.. code:: console

    Pre-increment (++a) = 11
    Hasil a = 11
    Post-increment (b++) = 10
    Hasil b = 11
    Pre-decrement (--c) = 9
    Hasil c = 9
    Post-decrement (d--) = 10
    Hasil d = 9

Berdasarkan contoh di atas, operasi yang dilakukan adalah *output*. Pada kode baris ke-4, dilakukan operasi *pre-increment*, yang artinya variabel ``a`` akan ditambahkan satu terlebih dahulu sebelum dilakukan *output*, sehingga menghasilkan nilai 11 (*console* baris ke-1). Pada kode baris ke-9, dilakukan operasi *post-increment*, yang artinya variabel ``b`` akan ditambahkan satu setelah dilakukan *output*, sehingga masih bernilai 10 (*console* baris ke-3), namun hasilnya tetap menjadi 11 (*console* baris ke-4). Hal yang sama ini berlaku untuk *pre-decrement* dan *post-decrement*, hanya saja bersifat mengurangi nilai.
