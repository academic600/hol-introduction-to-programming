Validation
==========

Dengan mempelajari seleksi dan repetisi, pembuat program akan melakukan sebuah validasi. Validasi merupakan proses memeriksa apakah suatu data atau *input* memenuhi suatu kriteria tertentu. Hal ini bertujuan agar data atau *input* yang diberikan sesuai dengan kriteria sehingga dapat digunakan pada proses selanjutnya. Biasanya validasi *input* dibuat dengan menggunakan repetisi *do-while*, agar program dimulai dengan meminta *input* terlebih dahulu yang kemudian di validasikan.

Berikut adalah contoh validasi panjang sebuah kata dari *input* yang dimasukan pengguna program.

- **contoh 1:**

.. code:: java

    import java.util.Scanner;

    public class Main {
        public static void main(String args[]) {
            Scanner scan = new Scanner(System.in);
            String name;
            
            do {
                System.out.print("Input your name [5-20 characters]: ");
                name = scan.nextLine();	
            } while (name.length() < 5 || name.length() > 20 );
            
            System.out.println("Your name is " + name);
        }
    }

.. code:: console

    Input your name [5-20 characters]: Hey
    Input your name [5-20 characters]: HelloHelloHelloHelloHello
    Input your name [5-20 characters]: Hello
    Your name is Hello

Pada kode di atas, terdapat sebuah repetisi *do-while* yang bertujuan untuk memastikan sebuah nama yang dimasukan harus memiliki panjang 5 - 20 karakter. Apabila nama yang dimasukan tersebut kurang dari 5 karakter atau lebih dari 20 karakter, maka pengguna program harus memasukan nama kembali, sampai kondisi tersebut terpenuhi.


Berikut adalah contoh validasi dengan menggunakan *Wrapper Class* String dengan ``method()`` dari *Wrapper Class* tersebut.

- **contoh 2:**

Method yang akan digunakan adalah ``startWidth()``


.. code:: java 

    import java.util.*;
    
    public class Main
    {
        Scanner scan = new Scanner(System.in);
        
        public Main(){
            String fullname;
            do{
                System.out.print("Input full name must started with [Mr./Ms.]?");
                fullname = scan.nextLine();
                
            }while(!(fullname.startsWith("Mr.") || fullname.startsWith("Ms.")));
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    mInput full name must started with [Mr./Ms.]?mbudi
    Input full name must started with [Mr./Ms.]?Ms.Budi


Selanjutnya kita akan mencoba membuat validasi **string** yang diperuntukkan untuk 

- **contoh 3:**

melakukan validasi **nomor handphone** pada java. 

.. code:: java

    import java.util.Scanner;

    public class PhoneNumberValidation {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            String phoneNumber = "";
            int flag = 0;

            // Loop sampai input valid
            while (flag == 2) {
                System.out.print("Masukkan nomor handphone (harus diawali dengan '08' dan memiliki 10 karakter): ");
                phoneNumber = scanner.nextLine();

                if(phoneNumber.length == 10){
                    flag++;                    
                }

            }

            boolean isDigit = true;
            for(char a : phoneNumber){
                if(!Character.isDigit(a)){
                    isDigit = false;
                    break;
                }
            }

            if(flag == 2 && isDigit){
                System.out.println("Anda memasukkan nomor handphone yang valid: " + phoneNumber);
                scanner.close();       
            }
            else{
                System.out.println("Nomor handphone tidak valid. Coba lagi.");
            }

        }
    }

Berikut adalah hasil output dari program diatas.

.. code:: console 

   01121
   Nomor handphone tidak valid. Coba lagi.
   0812345678
   Anda memasukkan nomor handphone yang valid: 0812345678

Berikut adalah validasi dari data **nomor handphone** yang diimplementasi dengan penggunaan **string** dan **character** pada java. 

dari kode diatas, kita melakukan validasi bahwa data **nomor handphone** yang dimasukkan harus berisi **10 karakter** dan data yang dimasukkan harus berupa karakter **angka**. 

- **contoh 4:**

Selanjutnya adalah validasi input **string** yang digunakan untuk melakukan validasi 

nama yang harus memiliki **karakter spasi** pada implementasi program yang diberikan. 

Berikut adalah contoh dari input tersebut. 

.. code-block:: java 

    import java.util.Scanner;

    public class NameValidation {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            String name = "";
            boolean isValid = false;

            // Loop sampai input valid
            while (!isValid) {
                System.out.print("Masukkan nama lengkap (dua kata): ");
                name = scanner.nextLine();

                // Split the input by spaces
                String[] nameParts = name.split(" ");

                // Check if the input contains exactly two words
                if (nameParts.length == 2) {
                    isValid = true;
                } else {
                    System.out.println("Nama tidak valid. Harus terdiri dari dua kata. Coba lagi.");
                }
            }

            System.out.println("Anda memasukkan nama yang valid: " + name);
            scanner.close();
        }
    }


Berikut adalah contoh input yang **valid** untuk diimplementasikan di program diatas. 

.. code-block:: console 
    Masukkan nama lengkap (dua kata): Budi Andi
    Anda memasukkan nama yang valid: Budi Andi

Dibawah ini merupakan contoh input **tidak valid** untuk diimplementasikan di program diatas. 

.. code-block:: console
    Masukkan nama lengkap (dua kata): Budi
    Nama tidak valid. Harus terdiri dari dua kata. Coba lagi.
    Masukkan nama lengkap (dua kata): Budi Andi
    Anda memasukkan nama yang valid: Budi Andi

- **contoh 5:**

Selanjutnya kita akan membuat validasi input **string** untuk melakukan validasi input yang sesuai dengan **kondisi** tertentu. 

Kondisi yang akan kita buat adalah validasi **input** untuk melakukan validasi **lategori** yang sesuai dengan program yang ingin diimplementasi. 

.. code-block:: java 

    import java.util.Scanner;

    public class FoodCategoryValidation {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            String category = "";
            boolean isValid = false;

            // Daftar kategori makanan yang diizinkan
            String[] validCategories = {"Appetizer", "Main Course", "Dessert", "Beverage"};

            // Loop sampai input valid
            while (!isValid) {
                System.out.print("Masukkan kategori makanan (Appetizer, Main Course, Dessert, Beverage): ");
                category = scanner.nextLine();

                // Memeriksa apakah kategori yang dimasukkan ada dalam daftar kategori yang diizinkan
                for (String validCategory : validCategories) {
                    if (category.equalsIgnoreCase(validCategory)) {
                        isValid = true;
                        break;
                    }
                }

                if (!isValid) {
                    System.out.println("Kategori makanan tidak valid. Coba lagi.");
                }
            }

            System.out.println("Anda memasukkan kategori makanan yang valid: " + category);
            scanner.close();
        }
    }

Program diatas, kita akan melakukan validasi input untuk menentukan kategori makanan yang sesuai dengan data yang tersedia seperti **Appetizer**, **Main Course**, **Dessert**, dan **Beverage**. 

Berikut adalah **input** dan **output** yang valid dari program diatas. 

.. code-block:: console
    
    Masukkan kategori makanan (Appetizer, Main Course, Dessert, Beverage): Main Course
    Anda memasukkan kategori makanan yang valid: Main Course

