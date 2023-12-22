Insertion Sort
====================
*Insertion sort* adalah algoritma pengurutan yang bekerja dengan cara membagi array menjadi dua bagian: bagian yang sudah diurutkan dan bagian yang belum diurutkan. Ia menempatkan elemen dari bagian yang belum diurutkan ke dalam bagian yang sudah diurutkan satu per satu, pada posisi yang tepat.

Inisialisasi Array:

    .. image:: /images/session-10/insertionSort/array-initial.jpg

1. Elemen pertama dalam array diasumsikan sudah terurut. Ambil elemen kedua dan simpan secara terpisah di dalam ``key``. Bandingkan ``key`` dengan elemen pertama, jika elemen pertama lebih  besar daripada ``key``, maka ``key`` diletakan  di depan elemen pertama. 

.. image:: /images/session-10/insertionSort/Insertion-sort-0_1.png

2. Sekarang, dua elemen pertama sudah terurut. Ambil elemen ketiga dan bandingkan dengan elemen-elemen di sebelah kirinya. Letakkan di belakang elemen yang lebih kecil darinya. Jika tidak ada elemen yang lebih kecil, maka letakkan di awal array.

.. image:: /images/session-10/insertionSort/Insertion-sort-1_1.png

3. Demikian pula, letakkan setiap elemen yang belum diurutkan pada posisi yang tepat.

.. image:: /images/session-10/insertionSort/Insertion-sort-2_2.png

.. image:: /images/session-10/insertionSort/Insertion-sort-3_2.png


Implementasi Insertion Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java

    public class Main {
        public static void insertionSort(int[] arr) {
            int n = arr.length;
            for (int i = 1; i < n; i++) {
                int key = arr[i];
                int j = i - 1;

                // Memindahkan elemen yang lebih besar dari key ke posisi yang lebih kanan
                while (j >= 0 && arr[j] > key) {
                    arr[j + 1] = arr[j];
                    j = j - 1;
                }
                arr[j + 1] = key;
            }
        }

        public static void main(String[] args) {
            int[] myArray = {9, 5, 1, 4, 3};
            insertionSort(myArray);
            System.out.print("Array yang diurutkan: ");
            for (int num : myArray) {
                System.out.print(num + " ");
            }
        }
    }

.. code:: console

    Array yang diurutkan: 1 3 4 5 9 

Time Complexity Insertion Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
**Kompleksitas Kasus Terburuk:** ``O(n^2)``
Misalkan, sebuah array dalam keadaan urutan menaik, dan Anda ingin mengurutkannya dalam urutan menurun. Dalam kasus ini, kompleksitas terburuk terjadi.

Setiap elemen harus dibandingkan dengan setiap elemen lainnya sehingga, untuk setiap elemen ke-n, dilakukan ``(n-1)`` jumlah perbandingan.

Maka dari itu, total jumlah perbandingan = ``n*(n-1) ~ n^2``

**Kompleksitas Kasus Terbaik:** ``O(n)``
Ketika array sudah terurut, loop luar berjalan sebanyak n kali sementara loop dalam tidak berjalan sama sekali. Jadi, hanya ada n jumlah perbandingan. Dengan demikian, kompleksitasnya adalah linear.

**Kompleksitas Kasus Rata-rata:** ``O(n^2)``
Terjadi ketika elemen-elemen dalam sebuah array berada dalam kekacauan (tidak dalam urutan naik maupun turun).

Aplikasi Insertion Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~
Insertion Sort digunakan saat:

1. Array memiliki jumlah elemen yang sedikit.
2. Hanya tersisa sedikit elemen yang perlu diurutkan.