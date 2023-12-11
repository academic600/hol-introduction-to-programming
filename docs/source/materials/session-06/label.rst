*Label* 
==============
*Label* digunakan bersama dengan pernyataan *break* dan *continue* untuk memberikan kemampuan untuk melompat ke blok tertentu atau mengulangi iterasi dari luar loop.

**Syntax :** 

.. code:: console

    break label;


.. code:: java

    public class Main {
    
        public static void main(String[] args) {
            
            outerLoop: // Label untuk loop luar
                for (int i = 0; i < 5; i++) {
                    innerLoop: // Label untuk loop dalam
                    for (int j = 0; j < 3; j++) {
                        if (i == 2 && j == 1) {
                            break outerLoop; // Melompat keluar dari outerLoop
                            
                            // Atau bisa juga dengan continue outerLoop untuk melanjutkan iterasi
                        }
                        System.out.println("i = " + i + ", j = " + j);
                    }

                }

        }
    }

.. code:: console

    i = 0, j = 0
    i = 0, j = 1
    i = 0, j = 2
    i = 1, j = 0
    i = 1, j = 1
    i = 1, j = 2
    i = 2, j = 0


.. note:: 

    Dalam contoh ini, terdapat dua loop bersarang (outerLoop dan innerLoop). Label outerLoop ditempatkan sebelum loop luar, sementara innerLoop ditempatkan sebelum loop dalam. Ketika kondisi tertentu terpenuhi (contoh di atas: i == 2 && j == 1), break outerLoop digunakan untuk melompat keluar dari loop luar.