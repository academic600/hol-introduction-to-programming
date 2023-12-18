*Continue*
==========

Kata kunci ``continue`` digunakan untuk mengabaikan kode yang ada di bawahnya dalam suatu iterasi, sehingga langsung dilanjutkan ke iterasi selanjutnya.

Berikut adalah contoh implementasi operasi lompat (*jump operation*) untuk ``continue``.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            for (int i = 0; i < 10; i++) {
                if (i == 4) {
                    continue;
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
    Iterasi ke-5
    Iterasi ke-6
    Iterasi ke-7
    Iterasi ke-8
    Iterasi ke-9

Pada kode di atas, terdapat sebuah repetisi *for* untuk mengeluarkan *output* dari interasi ke-0 sampai iterasi ke-9, karena memiliki validasi kurang dari 10. Namun, sebelum mengeluarkan *output*, terdapat sebuah validasi dengan seleksi *if*. Apabila variabel ``i`` bernilai 4, maka kata kunci ``continue`` dijalankan. Oleh karena itu, kode yang ada dibawahnya tidak akan dijalankan, dibuktikan dengan output "Iterasi ke-4" tidak keluar pada *console*.
