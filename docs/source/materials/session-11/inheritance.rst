Inheritance
============
Di Java, memungkinkan untuk mewarisi atribut dan metode dari satu kelas ke kelas lainnya. Kita mengelompokkan konsep "*inherit*" ke dalam dua kategori:

*subclass* (anak) - kelas yang mewarisi dari kelas lain
*superclass* (induk) - kelas yang diwarisi
Untuk mewarisi dari sebuah kelas, gunakan kata kunci extends.

Pada contoh di bawah ini, kelas *Car* (subclass) mewarisi atribut dan metode dari kelas *Vehicle* (superclass):


.. image:: /images/session-11/Inheritance.png


.. code:: java

    class Vehicle {
        protected String brand = "Ford"; // Atribut Vehicle
        public void honk() { // Metode Vehicle
            System.out.println("Tuut, tuut!");
        }
    }

    class Car extends Vehicle {
        private String modelName = "Mustang"; // Atribut Car

        public static void main(String[] args) {
            // Membuat objek myCar
            Car myCar = new Car();

            // Memanggil metode honk() (dari kelas Vehicle) pada objek myCar
            myCar.honk();

            // Menampilkan nilai atribut brand (dari kelas Vehicle) dan nilai modelName dari kelas Car
            System.out.println(myCar.brand + " " + myCar.modelName);
        }
    }


.. code:: console


    Tuut, tuut!
    Ford Mustang
  
