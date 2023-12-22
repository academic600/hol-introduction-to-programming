Selection Sort
===================

*Selection sort* adalah salah satu algoritma pengurutan sederhana yang bekerja dengan cara mencari elemen terkecil dari bagian yang belum diurutkan dan menukarnya dengan elemen pertama dari bagian yang belum diurutkan. Proses ini terus berulang, memilih elemen terkecil berikutnya dan menukarnya dengan elemen pertama dari bagian yang belum diurutkan.

1. Pilih elemen pertama sebagai ``minimum``
   
.. image:: /images/session-10/selectionSort/Selection-sort-0-initial-array.png

2. Bandingkan ``minimum`` kita dengan elemen kedua dalam array , jika elemen kedua dalam array kita lebih kecil dibandingkan dengan ``minimumm``, pilih elemen kedua sebagai nilai ``minimum`` yang baru. Bandingkan ``minimum`` dengan elemen ketiga dalam array, jika elemen ketiga lebih kecil, maka pilih elemen ketiga sebagai nilai ``minimum`` yang baru, jika tidak, kita akan biarkan saja. kita akan melakukan proses ini secara repetitif, hingga elemen indeks terakhir.
   
.. image:: /images/session-10/selectionSort/Selection-sort-0-comparision.png

3. Seletah setiap iterasi, ``minimum`` diletakan di depan ``list`` yang belum di urutkan , kita bisa mentukar saja value mereka, ``indeks ke-0`` dengan ``indeks ke-4``
   
.. image:: /images/session-10/selectionSort/Selection-sort-0-swapping.png

4. Untuk setiap iterasi, pengindeksan dimulai dari elemen pertama yang belum diurutkan. Langkah 1 hingga 3 diulang sampai semua elemen ditempatkan pada posisi mereka yang benar. Pada tahao ini kita mencari nilai yang paling ``minimum`` atau nilai yang paling kecil dan mengurutkan nya di urutan yang benar. 



.. image:: /images/session-10/selectionSort/Selection-sort-0.png


.. image:: /images/session-10/selectionSort/Selection-sort-1.png


.. image:: /images/session-10/selectionSort/Selection-sort-2.png


.. image:: /images/session-10/selectionSort/Selection-sort-3_1.png

Pada itersi ke tiga sudah array sudah terdapat di urutan yang benar. 

Implementasi Selection Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java


    public class Main {
        public static void selectionSort(int[] arr) {
            int n = arr.length;
            for (int i = 0; i < n - 1; i++) {
                // Temukan indeks elemen terkecil yang belum diurutkan
                int min_idx = i;
                for (int j = i + 1; j < n; j++) {
                    if (arr[j] < arr[min_idx]) {
                        min_idx = j;
                    }
                }
                
                // Tukar elemen terkecil dengan elemen pertama yang belum diurutkan
                int temp = arr[min_idx];
                arr[min_idx] = arr[i];
                arr[i] = temp;
            }
        }

        public static void main(String[] args) {
            int[] myArray = {20, 12, 10, 15, 2};
            selectionSort(myArray);
            System.out.print("Array yang diurutkan: ");
            for (int num : myArray) {
                System.out.print(num + " ");
            }
        }
    }



.. code:: console


    Array yang diurutkan: 2 10 12 15 20 

Time Complexity Selection Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. **Kompleksitas Waktu:**
   **Kompleksitas Kasus Terburuk:** ``O(n^2)`` Jika ingin mengurutkan dalam urutan menaik dan array berada dalam urutan menurun, maka kasus terburuk terjadi.

   **Kompleksitas Kasus Terbaik**: ``O(n^2)`` Terjadi ketika array sudah terurut.

   **Kompleksitas Kasus Rata-rata:** ``O(n^2)`` Terjadi ketika elemen-elemen dalam array tidak berada dalam urutan yang teratur (tidak naik maupun turun).

1. **Kompleksitas Ruang:**

Kompleksitas ruang adalah ``O(1)`` karena hanya menggunakan satu variabel tambahan, yaitu variabel temp.


Aplikasi Selection Sort 
~~~~~~~~~~~~~~~~~~~~~~~~~~

Penggunaan Selection Sort:
Selection sort digunakan ketika: 

1. Daftar yang akan diurutkan memiliki jumlah elemen yang sedikit.
2. Biaya pertukaran tidak menjadi masalah.
3. Pengecekan semua elemen merupakan keharusan.
4. Biaya penulisan ke memori menjadi pertimbangan, seperti pada memori flash (jumlah tulisan/pertukaran adalah O(n) dibandingkan dengan O(n^2) pada bubble sort).





