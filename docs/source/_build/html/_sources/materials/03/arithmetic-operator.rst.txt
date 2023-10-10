Arithmetic Operator
=====================
Merupakan salah satu jenis operator untuk melakukan pemrosesan dua buah operand yang akan menghasilkan suatu nilai tertentu.

Contoh Arithmetic Operator: 

.. list-table:: Arithmetic operator
   :widths: 50 50
   :header-rows: 1

   * - Operator
     - Result
   * - ``+``
     - Addition
   * - ``-`` 
     - Subtraction
   * - ``*`` 
     - Multiplication 
   * - ``/`` 
     - Division
   * - ``%`` 
     - Modulus
   * - ``++`` 
     - Increment
   * - ``--`` 
     - Decrement
  
Berikut contoh penerapan Arithmetic operator

.. code:: java 

    public class Main {
        
        public static void main(String[] args) {

            int a = 10;
            int b = 5;
            
            System.out.printf("Hasil Penjumlahan a + b = %d \n",a+b );
            System.out.printf("Hasil Pengurangan a - b = %d \n",a-b );
            System.out.printf("Hasil Perkalian a * b = %d \n",a*b );
            System.out.printf("Hasil Pembagian a / b = %d \n",a/b );
            System.out.printf("Hasil Modulo a % b = %d \n",a%b );
            
        }


    }
