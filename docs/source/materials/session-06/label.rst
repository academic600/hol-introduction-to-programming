*Label* 
=======

Penggunaan ``break`` dan ``continue`` hanya berdampak pada repetisi di level tersebut. Sehingga apabila terdapat repetisi *for* yang bersarang (*nested-for*), hal tersebut tidak dapat dilakukan secara langsung. Oleh karena itu, bahasa pemrograman Java telah menyediakan penggunaan ``label`` untuk mengidentifikasikan sebuah kode tertentu. Tujuannya adalah agar program dapat langsung menjalankan operasi lompat (*jump operation*) setelah bagian ``label`` yang dituju. 

Untuk dapat menggunakan ``label`` diperlukan dua buah hal, yaitu membuat ``label`` dan memanggil ``label`` tersebut.

.. code:: console

    <nama_label>;           // Membuat sebuah label
    break <nama_label>;     // Memanggil label dengan kata kunci break
    continue <nama_label>;  // Memanggil label dengan kata kunci continue

Berikut adalah contoh implementasi ``label`` dalam operasi lompat (*jump operation*).

.. code:: java

    public class Main {
        public static void main(String[] args) {
            outerLoop:
            for (int i = 0; i < 3; i++) {
                for (int j = 0; j < 3; j++) {
                    if (i == 1 && j == 1) {
                        break outerLoop;
                    }
                    System.out.println("i = " + i + ", j = " + j);
                }
            }
            System.out.println("End of statement.");
        }
    }

.. code:: console

    i = 0, j = 0
    i = 0, j = 1
    i = 0, j = 2
    i = 1, j = 0
    End of statement.


Pada kode di atas, terdapat repetisi *for* yang bersarang (*nested-for*). Di luar kedua repetisi, dibuat sebuah ``label`` dengan nama *outerLoop*. Apabila variabel ``i`` dan ``j`` bernilai 1, maka dijalankan perintah ``break outerLoop;``. Program akan mengakhiri repetisi yang berada di luar dan menlanjutkan ke perintah selanjutnya.
