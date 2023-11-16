Break and Continue
---------------------
kata kunci ``break`` kita sudah pernah melihat di switch case yang berfungsi untuk berpindah ke case yang lain.

``break`` juga digunakan untuk memberhentikan suatu loop. 

**Contoh Code**

.. code:: java

    for (int i = 0; i < 10; i++) {
        if (i == 4) {
            break;
        }
        System.out.println(i);
    }

**Output**

.. code:: console

    0
    1
    2
    3


Pada code diatas dapat terlihat suatu for loop ingin melakukan iterasi dari 0 sampai 9,
lalu di dalam for loop terdapat kondisi, jika ``i==4`` maka akan melakukan ``break``. Hal ini apabila melakukan iterasi sebanyak 4 kali maka i akan keluar dari loop dan loop akan berhenti. 

Continue
~~~~~~~~~
Pernyataan ``continue`` menghentikan satu iterasi (di dalam perulangan) jika suatu kondisi tertentu terjadi, dan melanjutkan dengan iterasi berikutnya dalam perulangan tersebut.

**Contoh Code**

.. code:: java

    for (int i = 0; i < 10; i++) {
        if (i == 4) {
            continue;
        }
        System.out.println(i);
    }

**Output**

.. code:: console

    0
    1
    2
    3
    5
    6
    7
    8
    9

Pada code diatas terdapat kondisi setelah for loop diman, jika ``i==4`` maka ``continue``, 
Hal ini di artikan jika sudah sampai di iterasi ke-4 maka lanjutkan saja, sampai jumlah iterasi for loop terpenuhi.



