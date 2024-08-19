Seleksi *If* Bersarang (*Nested*)
=================================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Ketika membuat sebuah program yang kompleks, terkadang dibutuhkan penggunaan *if* yang bersarang (*nested if*), artinya seleksi *if* di dalam seleksi *if*. Tidak ada batasan dalam menggunakan *nested if*.

Berikut adalah contoh implementasi seleksi *if* yang bersarang (*nested if*).

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int usia = 18;
            boolean memilikiKTP = true;

            if (usia >= 18) {
                if (memilikiKTP) {
                    System.out.println("Anda memenuhi syarat usia dan sudah memiliki KTP.");
                } else {
                    System.out.println("Anda memenuhi syarat usia, namun belum memiliki KTP.");
                }
            } else {
                System.out.println("Anda belum mencapai usia minimum.");
            }
        }
    }


.. code:: console

    Anda memenuhi syarat usia dan sudah memiliki KTP.

Pada seleksi *if* yang bersarang (*nested if*) di atas, pertama akan dilakukan pengecekan pada seleksi *if* yang berada di luar, yaitu apakah variabel usia lebih besar atau sama dengan 18. Karena variabel usia bernilai 18, maka pengecek tersebut menghasilkan benar (*true*), sehingga akan dijalankan perintah-perintah (*statements*) yang ada pada *scope* tersebut (baris 6 sampai 12).

Setelah itu, akan dilakukan pengecekan pada seleksi *if* yang berada di dalam, yaitu apakah variabel memilikiKTP bernilai benar (*true*). Karena kondisi tersebut terpenuhi, maka akan dijalankan perintah *output*, seperti yang terlihat pada *console*.
