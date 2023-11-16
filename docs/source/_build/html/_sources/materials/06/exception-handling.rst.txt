Exception Handling
===================
**Exception handling** adalah proses yang memungkinkan penanganan 
kesalahan atau kondisi yang tidak terduga saat program dijalankan.
Saat sebuah program berjalan, terdapat situasi-situasi yang bisa menyebabkan kesalahan, 
seperti pembagian oleh nol, akses ke data yang tidak tersedia, atau masalah koneksi jaringan.

Biasanya kita bisa menggunakan key-word ``try and catch``

**Syntax**

.. code:: console

    try {
        //kode yang ingin di test 
    }
    catch(Exception e) {
        //kode yang digunakan jika kode yang di test error
    }

**Contoh Code**

.. code:: console

    public class Main {
        public static void main(String[ ] args) {
            try {
                int[] myNumbers = {1, 2, 3};
                System.out.println(myNumbers[10]);
            } catch (Exception e) {
                System.out.println("Something went wrong.");
            }
        }   
    }

**Output**

.. code:: console

    Something went wrong.


