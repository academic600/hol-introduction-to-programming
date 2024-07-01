Seleksi *If* 
============

Seleksi (*selection*) merupakan proses pengambilan keputusan berdasarkan kondisi atau nilai tertentu. Terdapat dua cara dalam melakukan seleksi, yaitu *if* dan *switch-case*. Pada bagian ini akan dibahas mengenai seleksi *if* dan jenisnya.

*If*
----

Berikut adalah *flowchart* dan *syntax* dari seleksi *if*.

.. image:: /images/session-04/if.png
    :width: 150
    :align: center
.. centered:: Seleksi *If*

.. code:: console

    if(<condition>) {
        <true-statements>
    }

Berdasarkan *flowchart* dan *syntax* di atas, terlihat bahwa apabila kondisi atau nilai yang diberikan benar (bernilai *true*), maka perintah benar (*true statements*) akan dijalankan.

Berikut adalah contoh implementasi seleksi *if*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int x = 50;
            if(x < 100) {
                System.out.println("Nilai x lebih kecil dari 50");
            }

            int y = 100;
            if(y < 100) {
                System.out.println("Nilai y lebih kecil dari 100");
            }
        }
    }

.. code:: console

    Nilai x lebih kecil dari 50

Pada baris ke-3, dibuat sebuah variabel bernama ``x`` dengan nilai 50. Pada baris ke-4, dibuat sebuah seleksi *if* dengan kondisi nilai ``x`` di bawah 100. Di dalam *scope* seleksi *if* (baris ke-5), terdapat sebuah perintah yang akan dijalankan hanya apabila kondisi tersebut terpenuhi, yakni perintah *output*. Karena kondisi terpenuhi (nilai x yaitu 50 lebih kecil dari 100), maka perintah tersebut dijalankan, sehingga muncul *output* pada *console*.

Sedangkan, pada seleksi *if* yang ke-2, kondisi tidak terpenuhi. Nilai y yaitu 100 tidak lebih kecil dari 100. Oleh karena itu, perintah di dalam seleksi *if* yang ke-2 tidak dijalankan, sehingga tidak menghasilkan *output* pada *console*. 

*If-Else*
---------

Berikut adalah *flowchart* dan *syntax* dari seleksi *if-else*.

.. image:: /images/session-04/if-else.png
    :width: 350
    :align: center
.. centered:: Seleksi *If-Else*

.. code:: console

    if(<condition>) {
        <true-statements>
    } else {
        <false-statements>
    }

Berdasarkan *flowchart* dan *syntax* di atas, terlihat bahwa apabila kondisi atau nilai yang diberikan benar (bernilai *true*), maka perintah benar (*true statements*) akan dijalankan. Apabila tidak sesuai, maka perintah salah (*false-statements*) akan dijalankan.

Berikut adalah contoh implementasi seleksi *if*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int x = 50;
            if(x < 100) {
                System.out.println("Nilai x lebih kecil dari 50");
            } else {
                System.out.println("Nilai x lebih besar atau sama dengan 100");
            }

            int y = 100;
            if(y < 100) {
                System.out.println("Nilai y lebih kecil dari 100");
            } else {
                System.out.println("Nilai y lebih besar atau sama dengan 100");
            }
        }
    }

.. code:: console

    Nilai x lebih kecil dari 50
    Nilai y lebih besar atau sama dengan 100

Pada seleksi *if* yang ke-1, kondisi terpenuhi (nilai x yaitu 50 lebih kecil dari 100), sehingga perintah benar (*true-statements*) dijalankan. Perintah salah (*false-statements*) akan diabaikan.

Sedangkan, pada seleksi *if* yang ke-2, kondisi tidak terpenuhi (nilai y yaitu 100 tidak lebih kecil dari 100), sehingga perintah benar (*true-statements*) tidak dijalankan, melainkan perintah salah (*false-statements*) yang akan dijalankan.

*If-Else If-Else*
-----------------

Berikut adalah *flowchart* dan *syntax* dari seleksi *if-else if-else*.

.. image:: /images/session-04/if-elseif-else.png
    :width: 450
    :align: center
.. centered:: Seleksi *If-Else If-Else*

.. code:: console

    if(<condition-1>) {
        <true-statements-1>
    } else if(<condition-n>) {
        <true-statements-n>
    } else {
        <false-statements-n>
    }

Berdasarkan *flowchart* dan *syntax* di atas, terlihat terdapat beberapa kondisi atau nilai yang dapat di cek. Apabila kondisi yang ke-1 sesuai, maka perintah benar ke-1 (*true-statements-1*) akan dijalankan. Apabila tidak, maka akan dilanjutkan pengecekan untuk kondisi yang ke-n. Hal itu akan terus dilakukan sampai selesai.

Berikut adalah contoh implementasi seleksi *if*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int y = 100;
            if(y < 100) {
                System.out.println("Nilai y lebih kecil dari 100");
            } else if(y == 100) {
                System.out.println("Nilai y adalah 100");
            } else {
                System.out.println("Nilai y lebih besar dari 100");
            }
        }
    }

.. code:: console

    Nilai y adalah 100

Pada seleksi *if* tersebut, pertama akan dilakukan pengecekan pada kondisi yang ke-1. Karena nilai y yaitu 100 tidak lebih kecil dari 100, maka perintah benar ke-1 (*true-statements-1*) tidak akan dijalankan. Pengecekan dilanjutkan pada kondisi yang ke-2. Hasil dari pengecekan tersebut adalah benar (*true*), karena nilai y adalah 100, sehingga perintah benar ke-2 (*true-statements-2*) akan dijalankan. Pada *console* akan muncul *output* sesuai yang di perintah. Seleksi *if* akan dihentikan, karena sudah ada kondisi yang terpenuhi.
