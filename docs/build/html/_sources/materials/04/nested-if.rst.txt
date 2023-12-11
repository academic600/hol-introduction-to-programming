Nested IF
----------
Nested if adalah dimana terdapat if-else di dalam if-else. 

**Tujuan** :
untuk memeriksa beberapa kondisi berjenjang atau bersarang, untuk melakukan pengujian tambahan atau tindakan berdasarkan hasil dari pengujian pertama.

**Syntax nested-if**

.. code:: console

    if (kondisi1) {
        // Kode yang dijalankan jika kondisi_1 benar
        if (kondisi2) {
            // Kode yang dijalankan jika kondisi_2 juga benar
        } else {
            // Kode yang dijalankan jika kondisi_2 salah
        }
    } else {
        // Kode yang dijalankan jika kondisi_1 salah
    }

**Code :** 

.. code:: java

    int usia = 18;
    boolean memilikiKartu = true;

    if (usia >= 18) {
        if (memilikiKartu) {
            System.out.println("Selamat, Anda memenuhi syarat dan memiliki kartu anggota!");
        } else {
            System.out.println("Maaf, Anda memenuhi syarat namun tidak memiliki kartu anggota.");
        }
    } else {
        System.out.println("Maaf, Anda belum mencapai usia minimum.");
    }

**Output:** 
