If-Else 
---------------
Digunakan untuk memberikan sebuah kondisi benar atau salah  beserta statement yang ingin dilakukan apabila suatu kondisinya benar atau salah.

**Syntax If-Else** 

.. code:: console

    if(kondisi1){
        statement1
    }else{
        statement2
    }


.. code:: java

    public class Main {

        public static void main(String[] args) {
            int a = 5;
            int b = 10;
            //IF - ELSE
            if(a < 10) {
                System.out.println("5 lebih kecil dari 10");
            }else {
                System.out.println("5 lebih besar dari 10");
            }
        }

    }


.. code:: console
    
    5 lebih kecil dari 10


If - else if
~~~~~~~~~~~~~
Digunakan untuk memeriksa beberapa kondisi secara berurutan dan melakukan tindakan sesuai jika memenuhi kondisi yang diberikan.

Syntax **If-elseif**

.. code:: console
    
    if( kondisi1){
        statement1
    }else if(kondisi2){
        statement2
    }else if(kondisi3){
        statement3
    }else{
        statment4
    }



.. code:: java

    
    public class Main {
            
            //IF - ELSE IF 
            if (a == 0) {
                System.out.println("5 sama dengan 0");
            }else if(a == 5 ) {
                System.out.println("Variable a = 5");
            }else {
                System.out.println("Variabel a bukan 5");
            } 

        }

    }


.. code:: console

    Variable a = 5
