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

Inrement & Decrement
---------------------
Increment pada java di lambangkan dengan symbol ``++``

Decrement di lambangkan dengan symbol ``--``

Terdapat 2 macam jenis increment  
  - Pre Increment : merupakan cara menambahkan 1 terlebih dahulu baru digunakan
  - Post Increment: menggunakan angka tersebut, lalu ditambahkan 1 di akhir

.. code:: java

    public class Main {
    
      public static void main(String[] args) {
        int a = 10;
        int b = 10;
        ++a;
        b++;
        System.out.println("Hasil dari pre increment a: " +  a );
        System.out.println("Hasil dari post increment b: " +  b );
      } 
    }

Output : 

.. code:: console

  Hasil dari pre increment a: 11
  Hasil dari post increment b: 11

Terdapat 2 jenis juga decrement : 
   - Pre decrement : merupakan cara mengurangkan 1 terlebih dahulu baru digunakan
   - Post decrement: menggunakan angka tersebut, lalu mengurangkan 1 di akhir

.. code:: java

    public class Main {
    
      public static void main(String[] args) {
        int a = 10;
        int b = 10;
        --a;
        b--;
        System.out.println("Hasil dari pre decrement a: " +  a );
        System.out.println("Hasil dari post decrement b: " +  b );
      } 
    }

Output : 

.. code:: console

  Hasil dari pre decrement a: 9
  Hasil dari post decrement b: 9


.. note:: 

    Pada intinya post maupun pre memiliki tujuan yang sama yaitu increment atau decrement sebanyak 1.