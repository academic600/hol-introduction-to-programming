*Break*
-----------
Kata kunci `break` kita sudah pernah melihat di switch case yang berfungsi untuk berpindah ke case yang lain.
Kita juga bisa memakai kata *break* dalam suatu loop
untuk segera menghentikan loop tersebut.


`break` juga digunakan untuk memberhentikan suatu loop. 

.. code:: java

    public class Main {
    
        public static void main(String[] args) {
            
            for (int i = 0; i < 10; i++) {
                if (i == 4) {
                    break;
                }
                System.out.println(i);
            }

        }


    }



   

.. code:: console

    0
    1
    2
    3


Pada code diatas dapat terlihat suatu for loop ingin melakukan iterasi dari 0 sampai 9,
lalu di dalam for loop terdapat kondisi, jika ``i==4`` maka akan melakukan `break`. Hal ini apabila melakukan iterasi sebanyak 4 kali maka i akan keluar dari loop dan loop akan berhenti. 