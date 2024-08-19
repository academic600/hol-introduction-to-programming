Repetisi *While*
================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Pada repetisi *while*, perintah akan dilakukan secara berulang selama kondisi yang diberikan bernilai benar (*true*) secara tak terhitung. Disebut tak terhitung kanena biasanya jumlah perulangan tidak diketahui atau tidak dapat dihitung.

Berikut adalah *flowchart* dan *syntax* dari repetisi *while*.

.. image:: /images/session-05/while.png
    :width: 200
    :align: center
.. centered:: Repetisi *While*

.. code:: console

    while(<repetition-condition>) {
        <body-statements>
    }

Berdasarkan *flowchart* dan *syntax* di atas, program akan mengecek terlebih dahulu kondisi repetisi *while* (*repetition-condition*). Apabila kondisi tersebut sesuai, perintah yang ada di dalam scope repetisi *while* (*body-statements*) akan dijalankan. Setelah itu, program akan mengecek kembali kondisi repetisi *while* sampai kondisi tidak sesuai.

Berikut adalah contoh implementasi seleksi *while*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int j = 0; 
            while(j < 5) {
                System.out.println("Iterasi ke-" + j);
                j++;
            }  
        }
    }

.. code:: console

    Iterasi ke-0
    Iterasi ke-1
    Iterasi ke-2
    Iterasi ke-3
    Iterasi ke-4

Pada kode di atas, program akan melakukan pengecekan (*repetition-condition*) variabel ``j`` apakah kurang dari 5. Karena variabel ``j`` bernilai 0, maka kondisi tersebut terpenuhi, sehingga perintah yang ada di dalam *scope* (*body-statements*) akan dijalankan. Ada dua perintah yang akan dijalankan, yaitu *output* dan menaikan nilai variabel ``j`` sebanyak 1. Hal ini terus dilakukan sampai variabel ``j`` bernilai 5, karena sudah tidak masuk ke dalam kondisi.
