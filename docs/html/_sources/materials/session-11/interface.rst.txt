Interface
================

Interface adalah penghubung antara function abstrak dengan suatu objek ketika melakukan suatu proses implementasi pada interface.

Interface akan berjalan jika suatu objek memanggil atau mengimplementasi suatu class *Interface*.

Pertama-tama, kita dapat membuat class interface ``Car`` untuk menyimpan function interface.

.. code:: java 
    public interface Car{
    void turnOn();
    void turnOff();
    void drive ();
    }

Setelah class *interface* berhasil dibuat, langkah selanjutnya adalah mengimplementasi object class terhadap class *interface* yang sudah kita buat. kita dapat melakukannya dengan memanggil keyword ``implements``.

.. code:: java 
    public class Volvo implements Car{
        public Volvo(){
            
        }
        
        public void drive(){
            System.out.println("Volvo is starting drive...");
        }
        
        public void turnOn(){
            System.out.println("Volvo is starting turn on...");
        }
        
        public void turnOff(){
            System.out.println("Volvo is starting turn off...");
        }
    }

Langkah selanjutnya adalah memanggil objek ``Volvo`` ke dalam class ``Main`` yang sudah dibuat. 

.. code:: java 
    public class Main
    {
        public Main(){
        Volvo v = new Volvo();
        v.turnOn();
        v.drive();
        v.turnOff();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

