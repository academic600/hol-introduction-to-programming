*Inheritance*
=============

Konsep *object oriented programming* (OOP) lainnya adalah *inheritance* (pewarisan). Hal ini memungkinkan sebuah *class* dapat mewarisi atribut dan *method* dari *class* lainnya. Terdapat dua buah istilah yang berkaitan dengan *inheritance* (pewarisan), yaitu *sub-class* dan *super-class*. *Sub-class* adalah *class* yang diwarisi atribut dan *method* dari *super-class*. Sedangkan, *super-class* adalah *class* yang mewarasi atribut dan *method* ke *sub-class*

Untuk dapat mewarisi atribut atau *method*, dapat digunakan *access modifier* ``protected``. *Access modifier* ini memungkinkan *sub-class* memiliki atribut atau *method* dari *super-class*. Selain itu, untuk menunjukan bahwa sebuah class menjadi *sub-class* dapat menggunakan kata kunci ``extends``.

.. image:: /images/session-11/inheritance.png
    :width: 400
    :align: center
.. centered:: Contoh *Inheritance*

Berikut adalah contoh implementasi *inheritance* (pewarisan) pada sebuah *class*. Atribut dan method yang dimiliki oleh *class* ``Kendaraan`` juga dimiliki oleh *class* ``Mobil`` dan *class* ``Bus``.

.. code:: java

    public class Main {
        public class Kendaraan {
            // Atribut yang dimiliki oleh class Kendaraan
            protected String jenis;
            protected String warna;
            protected int tahun;
            
            // Constructor yang dimiliki oleh class Kendaraan
            protected Kendaraan(String jenis, String warna, int tahun) {
                this.jenis = jenis;
                this.warna = warna;
                this.tahun = tahun;
            }
            
            // Method yang dimiliki oleh class Kendaraan
            protected void suara() {
                System.out.println("Tuut, tuut!");
            }
        }
        
        public class Mobil extends Kendaraan {
            // Atribut yang dimiliki oleh class Mobil (ditambah dengan Kendaraan)
            private int jumlahPintu;
            
            // Constructor yang dimiliki oleh class Mobil
            public Mobil(String jenis, String warna, int tahun, int jumlahPintu) {
                super(jenis, warna, tahun);
                this.jumlahPintu = jumlahPintu;
            }
        }
        
        public class Bus extends Kendaraan {
            // Atribut yang dimiliki oleh class Bus (ditambah dengan Kendaraan)
            private int jumlahRoda;
            
            // Constructor yang dimiliki oleh class Bus
            public Bus(String jenis, String warna, int tahun, int jumlahRoda) {
                super(jenis, warna, tahun);
                this.jumlahRoda = jumlahRoda;
            }
        }
        
        public Main() {
            // Membuat object dari class Mobil
            Kendaraan kendaraan1 = new Mobil("SUV", "Hitam", 2023, 4);
            kendaraan1.suara();

            // Membuat object dari class Bus
            Kendaraan kendaraan2 = new Bus("Bus", "Putih", 2023, 12);
            kendaraan2.suara();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    Tuut, tuut!
    Tuut, tuut!
