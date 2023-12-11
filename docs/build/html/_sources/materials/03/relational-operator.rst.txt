Relational Operator
=====================
Relational operator merupakan operator yang dapat digunakan untuk membandingkan antara dua operand. 

Relational operator : 

.. image:: /images/03/relational-operator.png

Contoh Relational Operator dalam code : 

.. code:: java 

    public class Main {

        public static void main(String[] args) {
            int nilaiA = 12;
            int nilaiB = 4;
            boolean hasil;

            // apakah A lebih besar dari B?
            hasil = nilaiA > nilaiB;
            System.out.println(hasil);

            // apakah A lebih kecil dari B?
            hasil = nilaiA < nilaiB;
            System.out.println(hasil);

            // apakah A lebih besar sama dengan B?
            hasil = nilaiA >= nilaiB;
            System.out.println(hasil);

            // apakah A lebih kecil sama dengan B?
            hasil = nilaiA <= nilaiB;
            System.out.println(hasil);

            // apakah nilai A sama dengan B?
            hasil = nilaiA == nilaiB;
            System.out.println(hasil);

            // apakah nilai A tidak sama dengan B?
            hasil = nilaiA != nilaiB;
            System.out.println(hasil);

        }

    }

Output : 

.. code:: console

    false
    true
    false
    false
    true
