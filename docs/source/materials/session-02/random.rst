Math, Random
----------------
Random adalah cara untuk mengahasilkan suatu angka yang acak. 
Untuk membuat angka random kita bisa menggunakan library ``Math.Random`` yang di miliki Java 
kita dapat melakuakn import dari ``java.util.Random``

.. code-block:: java

    import java.util.Random;

    public class Main {
        
        public static void main(String[] args) {
            Random random = new Random();
            int randomNumber = random.nextInt(100) + 1; //random antara 1 - 100 
            System.out.println("Angka random : " + randomNumber);
            
        }

    }


.. code-block:: console

    Angka random : 49 

jika kita ingin menghasilkan kombinasi dari huruf dan angka random : 
Contoh misal 





