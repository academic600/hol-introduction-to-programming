Assignment Operator
========================
Assignment operator merupkan operator yang digunakan untuk memberikan nilai ke variabel. 

Juga digunakan untuk menggabungkan operasi aritmatika dengan operasi pemberian nilai. 

Berikut contoh assignment operator : 

.. image:: /images/03/assignment-operator.png

Contoh assignment operator dalam code 

.. code:: java

    public class Main {
        
        public static void main(String[] args) {
            int a;
            int b;

            // inisialisasi nilai
            a = 5;
            b = 10;

            // penambahan
            b += a;
            // sekarang b = 15
            System.out.println("Penambahan : " + b);

            // pengurangan
            b -= a;
            // sekarang b = 10 (karena 15-5)
            System.out.println("Pengurangan : " + b);

            // perkalian
            b *= a;
            // sekarang b = 50 (karena 10*5)
            System.out.println("Perkalian : " + b);

            // Pembagian
            b /= a;
            // sekarang b=10
            System.out.println("Pembagian : " + b);

            // Sisa bagi
            b %= a;
            // sekarang b=0
            System.out.println("Sisa Bagi: " + b);
        }

    }

Output : 

.. code-block:: console

    Penambahan : 15
    Pengurangan : 10
    Perkalian : 50
    Pembagian : 10
    Sisa Bagi: 0

