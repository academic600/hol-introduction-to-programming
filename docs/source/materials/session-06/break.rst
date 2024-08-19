*Break*
=======

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Pada bahasa pemrograman *Java*, pembuat program dapat menggabungkan repetisi dengan operasi lompat (*jump operation*). Tujuannya adalah untuk mengontrol perulangan dalam sebuah program. Terdapat tiga operasi lompat (*jump operation*) yang dapat digunakan yaitu *break*, *continue*, dan *label*.

Kata kunci ``break`` sudah pernah digunakan pada seleksi *switch-case*. Pada seleksi *switch-case*, kata kunci ini digunakan untuk mengakhiri perintah setiap kasus. Namun, pada repetisi, kata kunci ini digunakan untuk mengakhiri sebuah repetisi, walaupun kondisi repetisi masih terpenuhi.

Berikut adalah contoh implementasi operasi lompat (*jump operation*) untuk ``break``.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            for (int i = 0; i < 10; i++) {
                if (i == 4) {
                    break;
                }
                System.out.println("Iterasi ke-" + i);
            }
        }
    }

.. code:: console

    Iterasi ke-0
    Iterasi ke-1
    Iterasi ke-2
    Iterasi ke-3

Pada kode di atas, terdapat sebuah repetisi *for* untuk mengeluarkan *output* dari interasi ke-0 sampai iterasi ke-9, karena memiliki validasi kurang dari 10. Namun, sebelum mengeluarkan *output*, terdapat sebuah validasi dengan seleksi *if*. Apabila variabel ``i`` bernilai 4, maka kata kunci ``break`` dijalankan. Oleh karena itu, repetisi *for* dihentikan yang terbukti dengan *output* pada *console* hanya sampai iterasi ke-3 saja.
