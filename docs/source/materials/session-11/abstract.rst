Abstract
==================
**Abstraksi data** adalah proses menyembunyikan detail tertentu dan hanya menampilkan informasi penting kepada pengguna. Abstraksi dapat dicapai dengan menggunakan kelas abstrak atau antarmuka.
Abstraksi pada kelas memisahkan implementasi kelas dari cara kelas tersebut digunakan. 

**Abstract Class** : adalah kelas yang terbatas yang tidak dapat digunakan untuk membuat objek (untuk mengaksesnya, kelas tersebut harus diwarisi dari kelas lain

Sintaks asbtract class: 


**Abstract Method** : 
hanya dapat digunakan dalam sebuah kelas abstrak, dan tidak memiliki tubuh (body). Tubuhnya disediakan oleh subclass (diwarisi dari kelas tersebut).




.. code:: java

    // Abstract class
    abstract class Shape {
        // Abstract method (tanpa implementasi)
        public abstract void draw();
    }

    // Subclass dari kelas abstrak Shape
    class Circle extends Shape {
        // Implementasi dari metode abstrak draw()
        public void draw() {
            System.out.println("Drawing a circle");
        }
    }

    class Rectangle extends Shape {
        // Implementasi dari metode abstrak draw()
        public void draw() {
            System.out.println("Drawing a rectangle");
        }
    }

    public class Main {
        public static void main(String[] args) {
            // Membuat objek dari subclass Circle dan memanggil metode draw()
            Shape circle = new Circle();
            circle.draw(); // Output: Drawing a circle

            // Membuat objek dari subclass Rectangle dan memanggil metode draw()
            Shape rectangle = new Rectangle();
            rectangle.draw(); // Output: Drawing a rectangle
        }
    }

.. code:: console

    Drawing a circle
<<<<<<< Updated upstream
    Drawing a rectangle
=======
    Drawing a rectangle
>>>>>>> Stashed changes
