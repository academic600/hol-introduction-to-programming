Array Multidimensi
============================

Array multidimensi adalah kumpulan dari array-array. array yang memiliki satu ``[]`` disebut sebagai array satu dimensi, namun jika sebuah array memiliki 
lebih dari satu ``[]``, maka di sebut array multidimensi, jika memiliki dua ``[][]`` biasanya disebut sebagai ``array dua dimensi``.

Array multidimensi berguna ketika kita ingin menyimpan data dalam bentuk tabel, seperti tabel dengan baris dan kolom.

Berikut sintaks untuk membuat array dua dimensi : 

.. code:: console

    tipeData[][] nama variable = { value };

.. code:: console

    int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };

Akses & Ubah elemen array 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Untuk mengakses elemen dari array kita bisa menggunakan ``[index]``.

.. code:: java

    public class Main {

        public static void main(String[] args) {
            
                //Mengakses elemen array 
                int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
                System.out.println("nilai array sebelum di ubah: " + myNumbers[1][2]);
                
                //Mengubah value array di baris 1 kolom 2 
                myNumbers[1][2] = 9;
                System.out.println("hasil nilai yang diubah : " + myNumbers[1][2]);                
                
        }

    }


.. code:: console

    nilai array sebelum di ubah: 7
    hasil nilai setelah diubah : 9




**Mengeprint Array multidimensi:**

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
            for (int i = 0; i < myNumbers.length; ++i) {
            for(int j = 0; j < myNumbers[i].length; ++j) {
                System.out.println(myNumbers[i][j]);
            }
            }
        }
    }

.. code:: console

    1
    2
    3
    4
    5
    6
    7



.. note:: 

    Salah satu kegunaan array dua dimensi :

    *Permainan dan Grafik Komputer*: Dalam pengembangan permainan, ``array`` dua dimensi digunakan untuk merepresentasikan peta, level permainan, papan permainan, atau tata letak grafis lainnya. Contohnya, permainan papan seperti catur atau permainan video dengan grid map menggunakan array dua dimensi untuk mengatur posisi dan status dari elemen-elemen permainan.






