Class & object
====================
Pemrograman berorientasi objek (OOP) melibatkan penggunaan objek. Sebuah objek mewakili entitas dalam dunia nyata yang dapat diidentifikasi secara unik. Sebagai contoh, seorang siswa, sebuah meja, sebuah lingkaran, sebuah tombol, dan bahkan sebuah pinjaman semuanya dapat dianggap sebagai objek. Sebuah objek memiliki identitas, keadaan, dan perilaku yang unik.


**Kelas** adalah sebuah template, cetakan, atau ``blue print`` yang menentukan data dan metode-metode apa yang akan dimiliki oleh sebuah objek. 


**Objek** adalah sebuah instansi dari sebuah kelas.

Contoh : Mobil adalah class, lalu atribut atribut mobil seperti pintu mobil, warna mobil, roda mobil adalah objek. 


Membuat Class
<<<<<<< Updated upstream
~~~~~~~~~~~~~~~~~~~~~~~~~~
=======
~~~~~~~~~~~~~~~~~~~~~~~~~~``
>>>>>>> Stashed changes
Untuk membuat class  pada java kita bisa menamai class kita di java dengan diwali huruf besar. 
Contoh di bawah membuat class Main 


.. code:: java

    public class Main {
     int x = 5;
    }

Membuat object
~~~~~~~~~~~~~~~~~~~~~~~
Contoh membuat object adalah memanggil nama class tersebut lalu memberi nama pada objek kita. 

.. code:: java

    public class Main {
        int x = 5;

        public static void main(String[] args) {
            Main myObj = new Main();
            System.out.println(myObj.x);
        }
    }

.. code:: console

    5
