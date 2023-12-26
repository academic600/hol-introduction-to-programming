*Abstract Class* dan *Method*
=============================

*Abstract class* merupakan *class* yang tidak dapat dibuat sebagai *object* dari *class* tersebut. *Class* ini digunakan sebagai kerangka dasar untuk *sub-class* yang akan diwarisi. Untuk membuat *class* menjadi *abstract class* dapat menggunakan kata kunci ``abstract``.

Selain *abstract class*, bahasa pemrograman Java juga menyediakan *abstract method*, yaitu sebuah *method* yang dideklarasikan tanpa implementasi pada *abtract class*. Sehingga, implementasi dari method akan dibuat pada *sub-class*. Untuk membuat *method* menjadi *abstract method* dapat menggunakan kata kunci ``abstract``.

.. code:: java

    public class Main {
        // Deklarasi abstract class Kendaraan
        public abstract class Kendaraan {
            
            // Deklarasi abstract method suara
            protected abstract void suara();
        }
        
        // Deklarasi class Mobil dari abstract class Kendaraan
        public class Mobil extends Kendaraan {
            
            // Deklarasi method suara dari abstract method suara
            @Override
            public void suara() {
                System.out.println("Poom, poom!");
            }
        }
        
        // Deklarasi class Bus dari abstract class Kendaraan
        public class Bus extends Kendaraan {
            
            // Deklarasi method suara dari abstract method suara
            @Override
            public void suara() {
                System.out.println("Honk, honk!");
            }
        }
        
        public Main() {
            // Membuat object dari class Mobil
            Kendaraan kendaraan1 = new Mobil();
            kendaraan1.suara();

            // Membuat object dari class Bus
            Kendaraan kendaraan2 = new Bus();
            kendaraan2.suara();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    Poom, poom!
    Honk, honk!
