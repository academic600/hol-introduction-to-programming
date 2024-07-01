Repetisi *Do-While*
===================

Pada repetisi *do-while*, perintah akan dijalankan setidaknya satu kali tanpa memerika kondisi, dan setelahnya baru akan diulang selama kondisi masih sesuai secara tak terhitung.

.. note:: 

    Perbedaan utama antara repetisi *while* dengan *do-while* adalah pada hal yang dilakukan lebih dahulu. Pada repetisi *while*, program akan langsung melakukan pengecekan sehingga perintah yang ada di dalam *scope* hanya akan dijalankan apabila kondisinya sesuai. Sedangkan, pada repetisi *do-while*, program akan melakukan perintah yang ada di dalam *scope* dahulu, baru kemudian mengecek kondisi repetisi, sehingga perintah akan dijalankan setidaknya satu kali.


Berikut adalah *flowchart* dan *syntax* dari repetisi *do-while*.

.. image:: /images/session-05/do-while.png
    :width: 200
    :align: center
.. centered:: Repetisi *Do-While*

.. code:: console

    do {
        <body-statements>
    } while(<repetition-condition>);

Berdasarkan *flowchart* dan *syntax* di atas, program akan menjalankan perintah yang ada di dalam *scope* (*body-statements*) terlebih dahulu. Kemudian, program akan mengecek kondisi repetisi (*repetition-condition*). Apabila kondisi sesuai, maka program akan menjalankan kembali perintah yang ada di dalam *scope*. Hal ini akan dilakukan sampai kondisi tidak sesuai.

Berikut adalah contoh implementasi seleksi *do-while*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int k = 0;
            do {
                System.out.println("Iterasi ke-" + k);
                k++;
            } while (k < 5);

            k = 50;
            do {
                System.out.println("Iterasi ke-" + k);
                k++;
            } while (k < 5);
        }
    }

.. code:: console

    Iterasi ke-0
    Iterasi ke-1
    Iterasi ke-2
    Iterasi ke-3
    Iterasi ke-4
    Iterari ke-50

Pada kode di atas bagian pertama, program akan menjalankan perintah yang ada di dalam *scope* (*body-statements*) terlebih dahulu. Ada dua perintah yang akan dijalankan, yaitu *output* dan menaikan nilai variabel ``k`` sebanyak 1. Setelah itu, program akan mengecek apakah variabel ``k`` kurang dari 5. Karena kondisi terpenuhi, maka perintah yang ada di dalam *scope* (*body-statements*) akan dijalankan kembali. Hal ini akan terus dilakukan sampai variabel ``k`` bernilai 5.

Pada kode di atas bagian kedua, program terlihat dapat menghasilkan *output* pada *console* baris ke-6. Hal ini dikarenakan program akan menjalankan perintah setidaknya satu kali, baru setelahnya akan mengecek kondisi repetisi.
