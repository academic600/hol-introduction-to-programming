*Polymorphism*
==============

*Polymorphism* berasal dari bahasa Yunani, yaitu *poly*, yang berarti banyak, dan *morph*, yang berarti bentuk. Sehingga, *polymorphism* berarti sebuah *object* dapat memiliki banyak bentuk. Terdapat dua konsep *polymorphism* yang dapat diterapkan, yaitu *overloading* dan *overriding*. 

*Overloading*
-------------

Konsep ini memungkinkan pembuat program dapat mendeklarasikan *method* dengan nama yang sama di dalam sebuah *class*, namun dengan *parameter* atau *return type* yang berbeda. Berikut adalah contoh implementasi *overloading*.

.. code:: java

    public class Main {
        class Calculator {
            // Overloading method add dengan return type int dan dua parameter int
            public int add(int x, int y) {
                return x + y;
            }

            // Overloading method add dengan return type double dan dua parameter double
            public double add (double x, double y) {
                return x + y;
            }

            // Overloading method add dengan return type int dan tiga parameter int
            public int add(int x, int y, int z) {
                return x + y + z;
            }
        }

        public Main() {
            Calculator calculator = new Calculator();

            // Memanggil method add dengan return type int dan dua parameter int 
            System.out.println("add(10, 5) = " + calculator.add(10, 5));

            // Memanggil method add dengan return type double dan dua parameter double
            System.out.println("add(3.5, 2.7) = " + calculator.add(3.5, 2.7));

            // Memanggil method add dengan return type int dan tiga parameter int
            System.out.println("add(10, 5, 9) = " + calculator.add(10, 5, 9));
        }

        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    add(10, 5) = 15
    add(3.5, 2.7) = 6.2
    add(10, 5, 9) = 24


*Overriding*
------------

Konsep ini terjadi ketika *child class* (*sub-class*) memiliki *method* dengan nama yang sama, tipe *parameter* yang sama, dan *return type* yang sama dengan method dari *parent class* (*super-class*). Program hanya akan menjalankan method yang berada pada *child class*. Berikut adalah contoh implementasi *overriding*.

.. code:: java

    public class Main {
        public class Kendaraan {
            protected void suara() {
                System.out.println("Tuut, tuut!");
            }
        }
        
        public class Mobil extends Kendaraan {
            @Override
            public void suara() {
                System.out.println("Poom, poom!");
            }
        }
        
        public class Bus extends Kendaraan {
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
