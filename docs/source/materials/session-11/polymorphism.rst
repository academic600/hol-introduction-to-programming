Polymorphism
======================
Polymorphism berasal dari bahasa Yunani, yaitu ``poly`` yang berarti banyak, ``morph`` yang berarti bentuk, jadi Polymorphism adalah banyak bentuk dan terjadi ketika kita memiliki banyak kelas yang saling terkait melalui pewarisan.

Pewarisan memungkinkan kita mewarisi atribut dan metode dari kelas lain. Polimorfisme menggunakan metode-metode tersebut untuk melakukan tugas-tugas yang berbeda. Ini memungkinkan kita untuk melakukan satu tindakan dengan cara yang berbeda.

Sebagai contoh, bayangkan sebuah superclass yang disebut Animal yang memiliki metode bernama ``animalSound()``. Subclass dari Animal bisa menjadi *Pigs*, *Cats*, *Dogs*, *Birds* - Dan mereka juga memiliki implementasi suara hewan mereka sendiri (babi menguik, kucing mengeong, dan sebagainya):

.. code:: java

    class Animal {
        public void animalSound() {
            System.out.println("The animal makes a sound");
        }
    }

    class Pig extends Animal {
        public void animalSound() {
            System.out.println("The pig says: wee wee");
        }
    }

    class Dog extends Animal {
        public void animalSound() {
            System.out.println("The dog says: bow wow");
        }
    }

        class Main {
        public static void main(String[] args) {
            Animal myAnimal = new Animal();  // Membuat Animal objek
            Animal myPig = new Pig();  // Membuat objek pig
            Animal myDog = new Dog();  // Membuat objek dog
            myAnimal.animalSound();
            myPig.animalSound();
            myDog.animalSound();
        }
    }

.. code:: console


    The animal makes a sound
    The pig says: wee wee
    The dog says: bow wow






Overloading Method 
=======================
Overloading terjadi saat ada beberapa metode dengan nama yang sama di sebuah kelas, tetapi dengan parameter yang berbeda. Metode-metode tersebut bisa memiliki jumlah atau tipe parameter yang berbeda. Saat memanggil metode, Java akan menentukan metode mana yang sesuai berdasarkan jumlah atau tipe parameter yang digunakan dalam pemanggilan.

.. code:: java

    class Calculator {
        // Overloading method add dengan dua parameter int
        public int add(int x, int y) {
            return x + y;
        }

        // Overloading method add dengan tiga parameter int
        public int add(int x, int y, int z) {
            return x + y + z;
        }
    }



Overriding 
======================
Overriding, di sisi lain, terjadi saat sebuah subclass memiliki metode dengan nama dan parameter yang sama seperti metode dalam superclassnya. Subclass dapat mengganti implementasi dari metode yang diwarisi dari superclassnya.

.. code:: java

    class Animal {
        public void makeSound() {
            System.out.println("Some sound");
        }
    }


    class Dog extends Animal {
        @Override
        public void makeSound() {
            System.out.println("Bark!");
        }
    }

Dalam contoh ini, method ``makeSound()`` pada kelas *Dog* meng-override metode ``makeSound()`` yang diwarisi dari kelas *Animal*. Ketika memanggil ``makeSound()`` pada objek Dog, versi yang didefinisikan dalam kelas *Dog* akan dieksekusi.