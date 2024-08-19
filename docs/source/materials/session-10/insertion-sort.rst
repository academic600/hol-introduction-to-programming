*Insertion Sort*
================

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


*Insertion sort* merupakan algoritma *sorting* yang menempatkan sebuah data yang belum diurutkan pada tempat yang sesuai di setiap iterasi. Proses tersebut sama ketika mengurutkan kartu di tangan pada permainan kartu.

Berikut adalah simulasi kerja *sorting* data secara *ascending* (kecil ke besar) menggunakan *insertion sort* dengan data awal di bawah ini.

.. image:: /images/session-10/insertion-sort/initial.png
    :width: 250
    :align: center
.. centered:: Simulasi *Insertion Sort* Tahap ke-1

Secara umum, program akan melakukan tahapan sebagai berikut.

1. Data pertama diasumsukan sudah terurut.
2. Memilih data selanjutnya yang belum teurut.
3. Bandingkan data terpilih dengan data sebelumnya yang sudah terurut. Data akan digeser ke kanan selama lebih besar dari data terpilih.
4. Mengubah data pada posisi tersebut dengan data terpilih. 

**Tahap ke-1**

Data paling pertama, yaitu ``9``, dianggap sudah terurut. Oleh karena itu, proses dimulai dari data kedua, yaitu ``5``. Data ini disebut sebagai data terpilih (``key``). Program akan membandingkan angka data terpilih dengan data terurut ``9``. Hasilnya lebih kecil, maka data ``9`` akan digeser ke kanan. Kemudian, karena data terurut sudah habis, data terpilih akan dimasukan ke posisi terakhir data bergeser.

.. image:: /images/session-10/insertion-sort/step-1.png
    :width: 300
    :align: center
.. centered:: Simulasi *Insertion Sort* Tahap ke-1

**Tahap ke-2**

Pada tahap ini, data terpilih selanjutnya adalah ``1``. Kemudian, data terpilih dibandingkan dengan data terurut terakhir, yaitu ``9``. Hasilnya lebih kecil, sehinga digeser. Kemudian, data terakhir dibandingkan kembali dengan data terurut selanjutnya, yaitu ``5``. Hasilnya lebih kecil, sehingga digeser. Karan data terurut sudah habis. data terpilih akan dimasukan ke posisi terakhir data bergeser.

.. image:: /images/session-10/insertion-sort/step-2.png
    :width: 300
    :align: center
.. centered:: Simulasi *Insertion Sort* Tahap ke-2

**Tahap ke-3**

.. image:: /images/session-10/insertion-sort/step-3.png
    :width: 300
    :align: center
.. centered:: Simulasi *Insertion Sort* Tahap ke-3

**Tahap ke-4**

Pada tahap ini, data yang ada di dalam kumpulan data (*array*) sudah terurut dari kecil ke besar, sehingga simulasi *insertion sort* sudah selesai.

.. image:: /images/session-10/insertion-sort/step-4.png
    :width: 300
    :align: center
.. centered:: Simulasi *Insertion Sort* Tahap ke-4

Implementasi *Insertion Sort* 
-----------------------------

.. code:: java

    public class Main {
        
        // Deklarasi method insertionSort dengan parameter sebuah array tipe data int
        public void insertionSort(int[] numbers) {
            
            // Deklarasi variabel x bernilai panjang dari sebuah array
            int x = numbers.length;
            
            // Iterasi untuk menandakan jumlah iterasi yang perlu dilakukan
            for (int i = 0; i < x; i++) {
                
                // Deklarasi variabel key bernilai variabel numbers index ke-i
                int key = numbers[i];
                
                // Deklarasi variabel j bernilai i-1, untuk mendapatkan nilai sebelumnya
                int j = i - 1;

                // Iterasi untuk mengecek dengan data yang sudah terurut lebih besar dari variabel key
                while (j >= 0 && numbers[j] > key) {
                    
                    // Memindahkan data ke sebelahnya
                    numbers[j + 1] = numbers[j];
                    j--;
                }
                
                // Memindahkan data posisi terakhir dengan data terpilih
                numbers[j + 1] = key;
            }
        }
        
        public void print(int[] numbers) {
            for (int number : numbers) {
                System.out.print(number + " ");
            }
        }
        
        public Main() {
            int[] numbers = {9, 5, 1, 4, 3};
            insertionSort(numbers);
            print(numbers);
        }

        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    1 3 4 5 9

Kompleksitas Waktu *Insertion Sort*
-----------------------------------

Pada algortima *insertion sort*, kasus terbaik memiliki kompleksitas ``O(n)``. Hal ini terjadi ketika data sudah terurut sesuai dengan kriteria, sehingga tidak perlu ada pergeseran data.

Pada algoritma *insertion sort*, kasus terburuk dan rata-rata memiliki kompleksitas ``O(n^2)``. Hal ini terjadi ketika data terurut secara terbalik atau tanpa pola, sehingga perlu adanya pergeseran data.

Kompleksitas Ruang *Insertion Sort*
-----------------------------------

Pada algortima *insertion sort*, ketiga kasus memiliki kompleksitas ruang yang sama, yaitu ``O(1)``. Hal ini disebabkan karena algoritma *insertion sort* hanya menggunakan satu buah variabel pembantu untuk menyimpan nilai sementara saat pertukaran data.
