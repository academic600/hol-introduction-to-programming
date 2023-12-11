While Loop 
==============
While Loop melakukan eksekusi pernyataan secara berulang selama kondisi yang diberikan benar (True). 
Perbedaannya dengan for loop adalah bahwa dalam while loop, kondisi pengecekan terjadi sebelum eksekusi pernyataan.

Syntax While Loop

.. code:: console

    while (kondisi) {
    // Statement(s) yang akan dieksekusi selama kondisi terpenuhi (true)
    // Pernyataan ini akan diulang selama kondisi masih benar
    }
    
.. code:: java

    public class Main {
    
        public static void main(String[] args) {
            int j =0; 
            while(j < 5) {
                System.out.println("Iterasi ke- " + j );
                j++;
            }       
        }
    }


.. code:: console

    Iterasi ke- 0
    Iterasi ke- 1
    Iterasi ke- 2
    Iterasi ke- 3
    Iterasi ke- 4  


