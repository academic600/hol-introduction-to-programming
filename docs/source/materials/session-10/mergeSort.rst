Merge Sort
==================
*Merge sort* adalah algoritma pengurutan yang menggunakan pendekatan *divide and conquer* (bagi dan taklukkan). Algoritma ini membagi array menjadi bagian-bagian yang lebih kecil, secara rekursif mengurutkan setiap bagian tersebut, dan kemudian menggabungkan bagian-bagian yang sudah diurutkan tersebut untuk mendapatkan array yang utuh terurut.

.. image:: /images/session-10/merge-sort-example_0.png


Divide and Conquer 
~~~~~~~~~~~~~~~~~~~~~~~
Dengan menggunakan teknik Divide and Conquer, kita membagi sebuah masalah menjadi submasalah. Ketika solusi untuk setiap submasalah sudah siap, kita 'menggabungkan' hasil dari submasalah tersebut untuk memecahkan masalah utama.

Misalkan kita harus mengurutkan sebuah array ``A``. Sebuah submasalah adalah untuk mengurutkan sub-bagian dari array ini yang dimulai dari ``indeks p`` dan berakhir pada ``indeks r``, yang ditunjukkan sebagai ``A[p..r]``.

**Divide**

Jika ``q`` merupakan titik di tengah antara ``p`` dan ``r``, maka kita dapat membagi subarray ``A[p..r]`` menjadi dua array yaitu ``A[p..q]`` dan ``A[q+1, r]``.

**Conquer**

Pada langkah *conquer*, kita mencoba mengurutkan kedua subarray ``A[p..q]`` dan ``A[q+1, r]``. Jika kita belum mencapai kasus dasar, kita kembali membagi kedua subarray ini dan mencoba mengurutkannya.

**Combine**

Ketika langkah conquer mencapai langkah dasar dan kita mendapatkan dua subarray yang terurut ``A[p..q]`` dan ``A[q+1, r]`` untuk array ``A[p..r]``, kita menggabungkan hasilnya dengan membuat array terurut ``A[p..r]`` dari dua subarray terurut ``A[p..q]`` dan ``A[q+1, r]``.

Algoritma Merge Sort 
~~~~~~~~~~~~~~~~~~~~~~~

.. code:: console

    MergeSort(A, p, r):
    if p > r 
        return
    q = (p+r)/2
    mergeSort(A, p, q)
    mergeSort(A, q+1, r)
    merge(A, p, q, r)

Untuk mengurutkan seluruh array, kita perlu memanggil ``MergeSort(A, 0, length(A)-1)``.

Seperti yang ditunjukkan pada gambar di bawah, algoritma ``merge sort`` secara rekursif membagi array menjadi setengahnya sampai kita mencapai kasus dasar dari array dengan 1 elemen. Setelah itu, fungsi merge mengambil subarray yang sudah diurutkan dan menggabungkannya untuk secara bertahap mengurutkan seluruh array.

.. image:: /images/session-10/merge-sort-in-action---merge-step-simple.png

Tahap Penggabungan dari Merge Sort 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Setiap algoritma rekursif bergantung pada sebuah kasus dasar dan kemampuan untuk menggabungkan hasil dari kasus dasar tersebut. ``Merge sort`` tidak berbeda. Bagian paling penting dari algoritma ``merge sort`` adalah, seperti yang Anda duga, langkah penggabungan.

Langkah penggabungan adalah solusi untuk masalah sederhana penggabungan dua daftar (array) yang terurut untuk membangun satu daftar (array) besar yang terurut.

Algoritma ini mempertahankan tiga penunjuk, satu untuk masing-masing dari dua array dan satu untuk mempertahankan indeks saat ini dari array terurut akhir.

.. code:: console

    Apakah kita telah mencapai akhir dari salah satu array?
    Tidak:
        Bandingkan elemen saat ini dari kedua array
        Salin elemen yang lebih kecil ke dalam array yang sudah diurutkan
        Pindahkan penunjuk dari elemen yang mengandung elemen yang lebih kecil
    Ya:
        Salin semua elemen yang tersisa dari array yang tidak kosong

.. image:: /images/session-10/merge-two-sorted-arrays.png

Pada gambar diatas karena tidak ada elemen lagi yang tersisa pada array kedua, kita tahu bahwa kedua array telah di urutkan, kita bisa menyalin sisa elemen dari aray yang pertama secara langsung.

Penulisan Kode Merge Sort 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perbedaan yang mencolok antara langkah penggabungan yang kita jelaskan di atas dan yang kita gunakan untuk ``merge sort`` adalah bahwa kita hanya melakukan fungsi penggabungan pada *subarray* yang berurutan.

Ini sebabnya kita hanya membutuhkan *array*, posisi pertama, indeks terakhir dari *subarray* pertama (kita dapat menghitung indeks pertama dari subarray kedua) dan indeks terakhir dari subarray kedua.

Tugas kita adalah menggabungkan dua subarray ``A[p..q]`` dan ``A[q+1..r]`` untuk membuat array terurut ``A[p..r]``. Jadi input ke fungsi adalah ``A``, ``p``, ``q``, dan ``r``.

Fungsi merge bekerja sebagai berikut:

Buat salinan dari subarray ``L <- A[p..q]`` dan ``M <- A[q+1..r]``.
Buat tiga penunjuk ``i``, ``j``, dan ``k``.
i mempertahankan indeks saat ini dari ``L``, dimulai dari ``1``.
j mempertahankan indeks saat ini dari ``M``, dimulai dari ``1``.
k mempertahankan indeks saat ini dari ``A[p..q]``, dimulai dari ``p``.
Sampai kita mencapai akhir dari ``L`` atau ``M``, pilih elemen yang lebih besar di antara elemen dari ``L`` dan ``M``, dan letakkan mereka pada posisi yang benar di ``A[p..q]``.
Ketika kita kehabisan elemen baik dari ``L`` atau ``M``, ambil elemen-elemen yang tersisa dan letakkan di ``A[p..q]``.

.. code:: java

    // Menggabungkan dua subarray L dan M ke dalam arr
    void merge(int arr[], int p, int q, int r) {

        // Buat L ← A[p..q] dan M ← A[q+1..r]
        int n1 = q - p + 1;
        int n2 = r - q;

        int L[n1], M[n2];

        for (int i = 0; i < n1; i++)
            L[i] = arr[p + i];
        for (int j = 0; j < n2; j++)
            M[j] = arr[q + 1 + j];

        // Memelihara indeks saat ini dari subarray dan array utama
        int i, j, k;
        i = 0;
        j = 0;
        k = p;

        // Sampai kita mencapai akhir dari L atau M, pilih yang lebih besar di antara
        // elemen-elemen L dan M dan letakkan di posisi yang benar di A[p..r]
        while (i < n1 && j < n2) {
            if (L[i] <= M[j]) {
                arr[k] = L[i];
                i++;
            } else {
                arr[k] = M[j];
                j++;
            }
            k++;
        }

        // Ketika kita kehabisan elemen baik dari L atau M,
        // ambil elemen-elemen yang tersisa dan letakkan di A[p..r]
        while (i < n1) {
            arr[k] = L[i];
            i++;
            k++;
        }

        while (j < n2) {
            arr[k] = M[j];
            j++;
            k++;
        }
    }

Penjelasan Merge Function
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Berikut penjelasan bagaimana cara fungsi merge() bekerja dengan contoh dataset dibawah ini: 

.. image:: /images/session-10/merge-sort-demo-step-1.png

Pada gambar diatas array ``A[0..5]`` berisi dua subarray terurut, yaitu ``A[0..3]`` dan ``A[4..5]``. 

Mari kita lihat bagaimana cara fungsi merge akan menggabungkan dua array. 

.. code:: console

    void merge(int arr[], int p, int q, int r) {
    // Here, p = 0, q = 4, r = 6 (size of array)

**LANGKAH 1 :**  Buat duplikat *copy* dari ``sub-array`` untuk di urutkan

.. code:: console

    // Create L ← A[p..q] and M ← A[q+1..r]
    int n1 = q - p + 1 = 3 - 0 + 1 = 4;
    int n2 = r - q = 5 - 3 = 2;

    int L[4], M[2];

    for (int i = 0; i < 4; i++)
        L[i] = arr[p + i];
        // L[0,1,2,3] = A[0,1,2,3] = [1,5,10,12]

    for (int j = 0; j < 2; j++)
        M[j] = arr[q + 1 + j];
        // M[0,1] = A[4,5] = [6,9]

.. image:: /images/session-10/merge-sort-demo-step-2.png    

Keterangan : 

- ``A`` = Array 
- ``L`` = sub-array pertama di bagian kiri 
- ``M`` = sub-array keua di bagaian kanan 

**Langkah 2**: Menjaga indeks saat ini dari subarray dan array utama

.. code:: console

        
    int i, j, k;
    i = 0; 
    j = 0; 
    k = p; 

.. image:: /images/session-10/merge-sort-demo-step-3.png


**Langkah 3**: Sampai kita mencapai akhir dari ``L`` atau ``M``, pilih yang lebih besar di antara elemen-elemen ``L`` dan ``M`` dan letakkan mereka pada posisi yang benar di ``A[p..r]``

.. code:: console

    while (i < n1 && j < n2) { 
        if (L[i] <= M[j]) { 
            arr[k] = L[i]; i++; 
        } 
        else { 
            arr[k] = M[j]; 
            j++; 
        } 
        k++; 
    }

.. image:: /images/session-10/merge-sort-demo-step-4.png


**Langkah 4**: Ketika kita kehabisan elemen dari salah satu di antara ``L`` atau ``M``, ambil elemen-elemen yang tersisa dan letakkan di ``A[p..r]``

.. code:: console

    // Kita keluar dari pengulangan sebelumnya karena j < n2 tidak memenuhi syarat
    while (i < n1){
        arr[k] = L[i];
        i++;
        k++;
    }

.. image:: /images/session-10/merge-sort-demo-step-5.png

.. code:: console

    // Kita keluar dari pengulangan sebelumnya karena i < n1 tidak memenuhi syarat
    while (j < n2){
        arr[k] = M[j];
        j++;
        k++;
    }

.. image:: /images/session-10/merge-sort-demo-step-6.png

Langkah ini diperlukan jika ukuran ``M`` lebih besar daripada ``L``.

Pada akhir fungsi merge, subarray ``A[p..r]`` sudah terurut.

Time Complexity
~~~~~~~~~~~~~~~~~~~~
**Time Complexity**
**Best Case Complexity**: ``O(n*log n)``

**Worst Case Complexity**: ``O(n*log n)``

**Average Case Complexity**: ``O(n*log n)``

**Space Complexity**
**The space complexity dari merge sort adalah :** ``O(n)``.

Aplikasi Merge Sort
~~~~~~~~~~~~~~~~~~~~~
Merge sort dapat dipakai dalam: 

1. Masalah perhitungan inversi
2. Pengurutan eksternal
3. Aplikasi e-commerce

Implementasi pada aplikasi
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java
    
    public class Main {
         // Method untuk menggabungkan dua subarray dari arr[]
        void merge(int arr[], int p, int q, int r) {
            int n1 = q - p + 1;
            int n2 = r - q;

            int L[] = new int[n1];
            int M[] = new int[n2];

            // Salin data ke array sementara L dan M
            for (int i = 0; i < n1; ++i)
                L[i] = arr[p + i];
            for (int j = 0; j < n2; ++j)
                M[j] = arr[q + 1 + j];

            int i = 0, j = 0;
            int k = p;

            // Gabungkan elemen-elemen dari L dan M ke dalam arr[]
            while (i < n1 && j < n2) {
                if (L[i] <= M[j]) {
                    arr[k] = L[i];
                    i++;
                } else {
                    arr[k] = M[j];
                    j++;
                }
                k++;
            }

            // Salin elemen yang tersisa dari L jika ada
            while (i < n1) {
                arr[k] = L[i];
                i++;
                k++;
            }

            // Salin elemen yang tersisa dari M jika ada
            while (j < n2) {
                arr[k] = M[j];
                j++;
                k++;
            }
        }

        // Method untuk melakukan merge sort pada arr[]
        void mergeSort(int arr[], int p, int r) {
            if (p < r) {
                int q = (p + r) / 2;

                // Urutkan dua bagian dari array
                mergeSort(arr, p, q);
                mergeSort(arr, q + 1, r);

                // Gabungkan hasil pengurutan
                merge(arr, p, q, r);
            }
        }
        
        // Konstruktor untuk melakukan merge sort pada array dan mencetak hasilnya
        public Main() {
            int arr[] = { 6, 5, 12, 10, 9, 1 };

            mergeSort(arr, 0, arr.length - 1);

            System.out.println("Array yang terurut:");
            for (int i = 0; i < arr.length; ++i) {
                System.out.print(arr[i] + " ");
            }
        }

        // Main method untuk menjalankan proses pengurutan
        public static void main(String args[]) {
        new Main();
        }
}


.. code:: console

    Array yang terurut:
    1 5 6 9 10 12 