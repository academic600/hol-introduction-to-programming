Bubble Sort
===============
*Bubble sort* mengurutkan array dengan menukar elemen-elemen tetangga jika tidak berurutan. Nilai-nilai yang lebih kecil 'membubuh' ``(bubble)`` ke atas sementara yang lebih besar 'terbenam'``
(singking)`` ke bawah. Proses ini dilakukan dalam beberapa langkah, di mana setiap langkah membandingkan pasangan tetangga untuk ditukar jika perlu. Hasilnya, elemen terakhir menjadi yang terbesar, dan proses ini terus berlanjut hingga seluruh elemen terurut."

Berikut adalah dataset array yang akan kita pakai: 

.. image:: /images/session-10/bubbleSort/inisialisasi-array.png


Iterasi pertama : 

.. image:: /images/session-10/bubbleSort/bubbleSort-1.png

Iterasi kedua : 

.. image:: /images/session-10/bubbleSort/bubbleSort-2.png


Implementasi *Bubble Sort* 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java 

    public class Main {
        public static void bubbleSort(int[] arr) {
            int n = arr.length;
            for (int i = 0; i < n; i++) {
                // Elemen terakhir sebanyak i sudah berada pada posisi yang benar,
                // sehingga tidak perlu diperiksa lagi.
                for (int j = 0; j < n - i - 1; j++) {
                    // Melintasi array dari 0 hingga n-i-1
                    // Tukar jika elemen yang ditemukan lebih besar dari elemen berikutnya
                    if (arr[j] > arr[j + 1]) {
                        int temp = arr[j];
                        arr[j] = arr[j + 1];
                        arr[j + 1] = temp;
                    }
                }
            }
        }

        public static void main(String[] args) {
            int[] myArray = {2, 9, 5, 4, 8, 1};
            bubbleSort(myArray);
            System.out.print("Array yang terurut: ");
            for (int num : myArray) {
                System.out.print(num + " ");
            }
        }
    }


.. code:: console

    Array yang terurut: 1 2 4 5 8 9 

Optimisasi *Bubble Sort* 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Perbedaan utama antara *Bubble Sort* biasa dan versi yang dioptimalkan terletak pada cara penggunaan variabel tambahan untuk mengurangi jumlah operasi yang tidak perlu.

*Bubble Sort* biasa melakukan pertukaran elemen pada setiap iterasi, bahkan jika array sudah terurut. Hal ini dapat mengakibatkan iterasi terus dilakukan meskipun tidak ada lagi pertukaran yang dibutuhkan.

Namun, dalam Bubble Sort yang dioptimalkan, biasanya ditambahkan ``variabel boolean`` seperti ``swapped`` yang menandai apakah ada pertukaran elemen yang terjadi dalam satu iterasi. Jika tidak ada pertukaran yang dilakukan, artinya array sudah terurut dan iterasi dapat dihentikan lebih awal. Ini membantu mengurangi jumlah operasi yang tidak perlu, terutama ketika array sudah dalam keadaan hampir terurut atau sudah terurut. Dengan begitu, *Bubble Sort* yang dioptimalkan bisa lebih cepat karena mengurangi jumlah iterasi yang tidak perlu.

.. code:: Java

    public class Main {
        public static void bubbleSort(int[] arr) {
            int n = arr.length;
            boolean swapped; //variable boolean 
            
            for (int i = 0; i < n - 1; i++) {
                swapped = false;
                for (int j = 0; j < n - i - 1; j++) {
                    if (arr[j] > arr[j + 1]) {
                        int temp = arr[j];
                        arr[j] = arr[j + 1];
                        arr[j + 1] = temp;
                        swapped = true;
                    }
                }
                
                // Jika tidak ada pertukaran pada iterasi ini, array sudah terurut
                if (!swapped) {
                    break;
                }
            }
        }

        public static void main(String[] args) {
            int[] myArray = {64, 34, 25, 12, 22, 11, 90};
            bubbleSort(myArray);
            System.out.print("Array yang diurutkan: ");
            for (int num : myArray) {
                System.out.print(num + " ");
            }
        }
    }

.. code:: console

    Array yang diurutkan: 11 12 22 25 34 64 90 


Time Complexity Bubble Sort
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. **Kompleksitas Waktu**
   **Kompleksitas Kasus Terburuk**: ``O(n^2)``
   Jika kita ingin mengurutkan dalam urutan menaik dan array berada dalam urutan menurun, maka kasus terburuk terjadi.
   
   **Kompleksitas Kasus Terbaik**: ``O(n)``
   Jika array sudah terurut, maka tidak perlu dilakukan pengurutan.
   
   **Kompleksitas Kasus Rata-rata**: ``O(n^2)``
   Terjadi ketika elemen-elemen dalam array tidak berada dalam urutan yang teratur (tidak naik maupun turun).
   
2. **Kompleksitas Ruang**
   Kompleksitas ruang adalah ``O(1)`` karena hanya menggunakan variabel tambahan untuk pertukaran.
   Pada algoritma bubble sort yang dioptimalkan, digunakan dua variabel tambahan. Oleh karena itu, kompleksitas ruangnya menjadi ``O(2)``.

Aplikasi *Bubble Sort* 
~~~~~~~~~~~~~~~~~~~~~~~
Bubble sort akan di pakai saat : 

1. bukan di pakai dalam sesuatu yang kompleks 
2. Lebih menyukai kode yang pendek dan sederhana