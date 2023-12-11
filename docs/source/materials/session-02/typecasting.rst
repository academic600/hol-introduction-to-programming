Type Casting
-----------------
Type casting merupakan cara mengubah tipe data ke tipe data lain.

Terdapat 2 macam type casting : 

*Widening casting (automatically)* 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 
mengubah tipe data yang lebih kecil menjadi tipe data yang besar 

``byte`` -> ``short`` -> ``char``-> ``int`` -> ``long`` -> ``float`` -> ``double``

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int bulat = 9;
            double desimal = bulat; // Automatic casting: int ke double

            System.out.println(bulat);     
            System.out.println(desimal);   
        }
    }

.. code:: console

    9
    9.0


*Narrowing casting (manually)*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
mengubah tipe data yang besar menjadi tipe data yang lebih kecil 

``double`` -> ``float`` -> ``long`` -> ``int`` -> ``char`` -> ``short`` -> ``byte``
  

.. code:: java

    public class Main {
        public static void main(String[] args) {
            double desimal = 9.78d;
            int bulat = (int) desimal; // Manual casting: double ke int

            System.out.println(desimal);   // Outputs 9.78
            System.out.println(bulat);      // Outputs 9
        }
    }


.. code:: console

    9.78
    9


