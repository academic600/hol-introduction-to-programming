Validation
==========

Dengan mempelajari seleksi dan repetisi, pembuat program akan melakukan sebuah validasi. Validasi merupakan proses memeriksa apakah suatu data atau *input* memenuhi suatu kriteria tertentu. Hal ini bertujuan agar data atau *input* yang diberikan sesuai dengan kriteria sehingga dapat digunakan pada proses selanjutnya. Biasanya validasi *input* dibuat dengan menggunakan repetisi *do-while*, agar program dimulai dengan meminta *input* terlebih dahulu yang kemudian di validasikan.

Berikut adalah contoh validasi panjang sebuah kata dari *input* yang dimasukan pengguna program.

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