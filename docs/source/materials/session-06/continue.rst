*Continue*
------------

Pernyataan `continue` menghentikan satu iterasi (di dalam perulangan) jika suatu kondisi tertentu terjadi, dan melanjutkan dengan iterasi berikutnya dalam perulangan tersebut.



.. code:: java

    public class Main {
    
        public static void main(String[] args) {


            for (int i = 0; i < 10; i++) {
                if (i == 4) {
                    continue;
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
    5
    6
    7
    8
    9

Pada code diatas terdapat kondisi setelah for loop diman, jika ``i==4`` maka `continue`, 
Hal ini di artikan jika sudah sampai di iterasi ke-4 maka lanjutkan saja, sampai jumlah iterasi for loop terpenuhi.

