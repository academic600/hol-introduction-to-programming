Logical Operator
=================
logical operator  digunakan untuk membuat operasi logika.

.. image:: /images/03/logical-operator.png

biasanya di pakai untuk memberikan suatu kondisi tertentu. 
Contoh : 

.. code:: java

    public class Main{
        public static void main ( String args[] ) {
                    int a = 5;
                    System.out.println ( a<5  &&  a<20 );
                    System.out.println ( a<5 || a<20 );
                    System.out.println ( ! ( a<5  &&  a<20 ));
        }  
    }

Output : 

.. code:: console

    false
    true
    true
