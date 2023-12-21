Variable Scope
===================
*Variabel scope* (lingkup variabel) di Java mengacu pada bagian program di mana variabel tertentu dapat diakses atau digunakan. Lingkup variabel ditentukan oleh di mana variabel tersebut dideklarasikan, dan ada beberapa jenis lingkup variabel dalam Java:

**Lingkup Blok** 

Variabel yang dideklarasikan di dalam sebuah blok kode (misalnya, blok if, for, atau while) hanya dapat diakses di dalam blok tersebut.

.. code:: java

    public class Main {
        // Metode dengan satu parameter

        public void exampleMethod() {
            int x = 10; // Variabel x memiliki lingkup di dalam method exampleMethod()
            if (x > 5) {
                int y = 20; // Variabel y memiliki lingkup di dalam blok if
                System.out.println(x); // x dapat diakses di sini
                System.out.println(y); // y dapat diakses di sini
            }
            System.out.println(x); // x dapat diakses di sini
            // System.out.println(y); // Ini akan menyebabkan error karena y tidak dapat diakses di luar blok if
        }
        
        public Main() {
            exampleMethod();
        }
        
        public static void main(String[] args) {
            new Main();
            
        }
    }



.. code:: console 

        10
        20
        10

**Lingkup Metode (Method Scope)**

Variabel yang dideklarasikan di dalam sebuah metode dapat diakses di seluruh metode itu.


.. code:: java

    public void exampleMethod() {
        int a = 5; // Variabel a memiliki lingkup di dalam method exampleMethod()
        System.out.println(a); // a dapat diakses di sini
    }


**Lingkup Kelas (Class Scope)**

Variabel yang dideklarasikan sebagai variabel kelas (di luar metode) dapat diakses oleh semua metode dalam kelas yang sama.

.. code:: 

    public class MyClass {
        int b = 15; // Variabel b memiliki lingkup di dalam kelas MyClass
        public void displayB() {
            System.out.println(b); // b dapat diakses di sini
        }
    }

Variabel Global
~~~~~~~~~~~~~~~~~~~~~
Variabel global adalah variabel yang dideklarasikan di luar dari semua metode, biasanya di dalam sebuah kelas. Mereka dapat diakses oleh semua metode dalam kelas tersebut.


.. code:: java

    public class Main {
    
	
        // Variabel global yang digunakan di dalam kelas
        static int globalVar = 10;

        public static void main(String[] args) {
            // Mengakses variabel global pada method main
            System.out.println("Nilai globalVar pada method main: " + globalVar);

            // Memanggil metode lain yang menggunakan variabel global
            anotherMethod();
        }

        public static void anotherMethod() {
            // Mengakses variabel global dari metode lain
            System.out.println("Nilai globalVar pada anotherMethod: " + globalVar);
        }
    }


.. code:: console


    Nilai globalVar pada method main: 10
    Nilai globalVar pada anotherMethod: 10

Variabel Local
~~~~~~~~~~~~~~~~~~
Variabel lokal adalah variabel yang dideklarasikan di dalam suatu blok kode, seperti di dalam metode atau blok if/for/while. Mereka hanya dapat diakses di dalam blok kode di mana mereka dideklarasikan.

.. code:: java

    public class LocalVariableSimple {

        public static void main(String[] args) {
            // Variabel lokal di dalam method main
            int number = 5;
            System.out.println("Nilai number: " + number);
            
            // Variabel lokal di dalam blok kode if
            if (number > 3) {
                String message = "Angka lebih besar dari 3";
                System.out.println(message);
            }
            
            // System.out.println(message); // Ini akan menyebabkan error karena message hanya bisa diakses di dalam blok if
        }
    }

.. code:: console 

    Nilai number: 5
    Angka lebih besar dari 3



