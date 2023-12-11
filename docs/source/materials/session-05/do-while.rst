Do-While Loop 
--------------
Do-while loop akan mengeksekusi blok pernyataan minimal satu kali tanpa memeriksa kondisi terlebih dahulu. 
Berbeda dengan while loop, dimana akan melakukan pengecekan terlebih dahulu benar atau tidak kondisinya baru dijalankan.

Syntax do-while loop 

.. code:: console

    do {
        // Statement(s) yang akan dieksekusi minimal satu kali
        // Pernyataan ini akan diulang selama kondisi masih benar (true)
    } while (kondisi);

**Code**

.. code:: java

    public static void main(String[] args) {
        //contoh kondisi benar
    	int k = 0;
    	do {
    	    System.out.println("Iterasi ke-" + k);
    	    k++;
    	} while (k < 5);
        
        //contoh kondisi salah
        int k = 5;
    	do {
    	    System.out.println("Iterasi ke-" + k);
    	    k++;
    	} while (k < 2);
        
    }

**Output**

.. code:: console

    //kondisi benar
    Iterasi ke-0
    Iterasi ke-1
    Iterasi ke-2
    Iterasi ke-3
    Iterasi ke-4

    //kondisi salah
    Iterari ke-5

Pada code diatas dengan kondisi yang salah, kita menginisialisasi nilai k = 5, tapi kondisi nya kita minta sampai ``k < 2``
hal ini yang membuat kondisi nya salah, lalu hanya mengeluarkan output sebanyak 1 kali yaitu "Iterasi ke-5".



