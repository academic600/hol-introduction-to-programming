*Exception Handling*
====================

Pada bahasa pemrograman *Java*, *exception handling* adalah proses untuk menangani kesalahan pada saat program dijalankan (*exception*). Ketika terjadi kesalahan tersebut, biasanya akan terjadi *crash* atau program yang berhenti secara tiba-tiba. Contoh kesalahan yang sering ditemui adalah pembagian oleh nol, akses ke data yang tidak tersedia, dan masalah koneksi jaringan. Oleh karena itu, kesalahan tersebut dapat dan perlu di validasikan agar program dapat berjalan dengan baik.

Salah satu cara untuk melakukan *exception handling* adalah menggunakan ``try-catch``. Berikut adalah *syntax* yang dapat digunakan dalam membuat ``try-catch``.

Macam-macam exception handling
-------------------------------

- Checked Exceptions 
- Unchecked Exceptions 
- Custom exceptions 

**Penjelasan**

1. **Checked Exceptions**
        
   Checked exceptions adalah exception yang diperiksa saat proses kompilasi sedang berjalan. Program harus mendeklarasikan checked exceptions 
   dengan menggunakan ``try-catch`` atau ``throws``.

   Jenis-jenis dari **checked exceptions** adalah sebagai berikut: 
     
     - **IOException**
      IOException digunakan untuk menangani kesalahan input dan output yang terjadi pada proses input output. 
      Seperti kesalahan membaca pada file data dan socket. 

      berikut adalah contoh dari ``IOException``.

      .. code-block:: java 

        // Contoh 1: Membaca dari file yang tidak ada
        try {
            FileReader fileReader = new FileReader("nonexistentfile.txt");
            BufferedReader bufferedReader = new BufferedReader(fileReader);
            String line = bufferedReader.readLine();
            System.out.println(line);
            bufferedReader.close();
        } catch (IOException e) {
            System.err.println("Caught IOException: " + e.getMessage());
        }
    
     - **SQLException**
       ``SQLException`` adalah exception yang digunakan untuk menangani kesalahan yang terjadi saat program 
       sedang berinteraksi dengan database JDBC (Java Database Connectivity). Kesalahan yang biasa terjadi seperti 
       kesalahan koneksi dengan database dan kesalahan syntax SQL yang digunakan. 

       berikut adalah contoh dari ``SQLException``. 

       .. code-block:: java

            import java.sql.Connection;
            import java.sql.DriverManager;
            import java.sql.SQLException;
            import java.sql.Statement;

            public class SQLExceptionExample {
                public static void main(String[] args) {
                    Connection connection = null;
                    Statement statement = null;

                    try {
                        // Koneksi ke database
                        String url = "jdbc:mysql://localhost:3306/testdb";
                        String user = "root";
                        String password = "password";
                        connection = DriverManager.getConnection(url, user, password);

                        // Membuat statement
                        statement = connection.createStatement();

                        // Menjalankan pernyataan SQL yang salah
                        String sql = "INSERT INTO users (id, name) VALUES (1, 'John Doe', 123)";
                        statement.executeUpdate(sql);

                    } catch (SQLException e) {
                        // Menangani SQLException
                        System.err.println("Caught SQLException: " + e.getMessage());
                        System.err.println("SQLState: " + e.getSQLState());
                        System.err.println("ErrorCode: " + e.getErrorCode());
                    } finally {
                        // Menutup sumber daya
                        try {
                            if (statement != null) statement.close();
                            if (connection != null) connection.close();
                        } catch (SQLException e) {
                            e.printStackTrace();
                        }
                    }
                }
            }

2. **Unchecked Exception**
   Unchecked exception adalah exception yang digunakan untuk mengatasi kesalahan logika dalam program. 

   Jenis-jenis dari **unchecked exceptions** adalah sebagai berikut:
      - **NullPointerException** 
        ``NullPointerException`` adalah jenis exception yang bisa digunakan untuk membantu dalam memvalidasi apakah 
        suatu data bernilai null atau tidak. 

        berikut adalah contoh dari ``NullPointerException``. 

        .. code-block:: java 

            try {
                obj.method();
            } catch (NullPointerException e) {
                System.out.println("Caught NullPointerException");
            }
    
      - **ArithmeticException** 
      ``ArithmeticException`` adalah jenis exception yang terjadi ketika operasi aritmatika tidak sesuai. 
      contoh dari ``ArithmeticException`` adalah ketika suatu bilangan bulat dibagi dengan angka nol. 

      berikut adalah contoh dari ``ArithmeticException``: 

       .. code-block:: java 

        public class Main {
            public static void main(String[] args) {
                try {
                    int result = 10 / 0; // ini merupakan arithmetic exception 
                } catch (ArithmeticException e) {
                    System.out.println("Perhitungan aritmetika tidak sesuai");
                }
            }
        }

    
     - **Custom Exceptions**
       Custom exception adalah suatu exception yang dibuat secara manual yang dimana exception ini 
       tidak ada di bahasa pemrograman java, sehingga kita harus membuat exception sendiri untuk suatu 
       kondisi tertentu. 

       Berikut adalah contoh dari ``Custom exception``:

       .. code-block:: java 

            // Membuat class custom exception yang inherit dari class Exception
            public class InvalidKarnivoraException extends Exception {
                public InvalidKarnivoraException(String message) {
                    super(message);
                }
            }

      disini kita membuat suatu custom exception dengan nama ``InvalidKarnivoraException`` yang diperuntukkan untuk 
      melakukan validasi hewan yang dikategorikan sebagai karnivora atau bukan. 


      .. code-block:: java 

        public class Main {
            // Method yang memeriksa hewan karnivora atau tidak 
            public static void checkIsKarnivora(String animal) throws InvalidKarnivoraException {
                if (animal != "Lion" || animal != "Tiger") {
                    throw new InvalidKarnivoraException("Hewan ini bukan karnivora");
                }
            }

            public static void main(String[] args) {
                try {
                    checkIsCarnivora("Dog"); // memanggil function checkIsCarnivora 
                } catch (InvalidAgeException e) {
                    System.out.println(e.getMessage());
                }
            }
        
      Maka hasil output dari exception diatas sebagai berikut.

      .. code-block:: console 
        
        Hewan ini bukan karnivora 
        


      

     
        

Penggunaan block ``try-catch``
------------------------------

**Syntax**

.. code:: console

    try {
        <kode yang ingin di validasikan>
    }
    catch(Exception e) {
        <kode yang dijalankan ketika error>
    }

Berikut adalah contoh implementasi ``try-catch`` ketika mengakses data dalam bentuk *array* yang tidak tersedia.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            try {
                int[] myNumbers = {1, 2, 3};
                System.out.println(myNumbers[10]);
            } catch (Exception e) {
                System.out.println("Data tidak ditemukan");
            }
        }   
    }


.. code:: console

    Data tidak ditemukan

Apabila tidak menggunakan ``try-catch``, pada *console* akan muncul *error* sebagai berikut.

.. code:: console

    Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 10 out of bounds for length 3
        at Main.main(Main.java:5)

Berdasarkan kode di atas, terdapat sebuah *array* dengan nama ``myNumbers`` yang hanya memiliki 3 buah data. Karena hanya ada 3 buah data saja, artinya *index* yang dapat diakses hanya sampai *index* ke-2 (karena *index* dimulai dari 0). Pada kode ingin dilakukan *output* untuk *index* ke-10 yang tidak didefinisikan, sehingga muncul *error*. Karena kode sudah di validasikan dengan ``try-catch``, maka ketika kode yang berada di dalam *scope* ``try`` *error*, yang dijalankan adalah kode yang ada di dalam *scope* ``catch``.


``try-catch`` bisa ditambahkan keyword ``finally``. keyword ``finally`` berfungsi untuk menampilkan output setelah proses ``try-catch`` telah selesai dijalankan. Cara menggunakan ``finally`` akan dijelaskan dibawah berikut. 

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            try {
                int[] myNumbers = {1, 2, 3};
                System.out.println(myNumbers[1]);
            } catch (Exception e) {
                System.out.println("Data tidak ditemukan");
            } finally {
                System.out.println("'try catch' finished !");
            }
        }
    }

.. code:: console

    2
    'try catch' finished !


Selanjutnya pada ``try-catch`` kita dapat melakukan custom error handling. Custom error handling bisa dilakukan dengan keyword ``throw()``. ketika menggunakan ``throw()`` harus diikutsertakan dengan *exception type*. 

.. code:: java 

    public class Main {

        public void checkAge(int age) {
            if (age < 18) {
                throw new ArithmeticException("Access denied - You must be at least 18 years old.");
            }
            else {
                System.out.println("Access granted - You are old enough!");
            }
        }

        public static void main(String[] args) {
            checkAge(15); 
        }
    }

.. code:: console

    Exception in thread "main" java.lang.ArithmeticException: Access denied - You must be at least 18 years old.





