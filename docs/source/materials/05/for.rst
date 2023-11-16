For Loop
==========
For loop merupakan salah satu bentuk code pengulangan yang dapat dipakai dalam java. 
kenapa kita memakai iterasi? 
Misal jika kita ingin mengeprint "Hello World" sebanyak 5 kali kita bisa membuat kode seperti ini: 

.. code:: console

    System.out.println("Hello World");
    System.out.println("Hello World");
    System.out.println("Hello World");
    System.out.println("Hello World");
    System.out.println("Hello World");

Akan tetapi bagaimana jika kita ingin mengeprint sebanyak 100 kali?
kita bisa menggunakan iterasi untuk membuatnya.

For loop dapat digunakan untuk iterasi dan mengulang sebanyak variabel yang telah di inisialisasi. 

syntax for loop: 

.. code:: console

    for(inisialisasi ; condition ; increment){


    }

**Code**

.. code:: java

    public class Main {
        
        public static void main(String[] args) {
            for(int i=0; i<10; i++) {
                System.out.printf("Hello world %d\n", i);
            }
            
        }

    }

**Output**

.. code:: console

    Hello world 0
    Hello world 1
    Hello world 2
    Hello world 3
    Hello world 4
    Hello world 5
    Hello world 6
    Hello world 7
    Hello world 8
    Hello world 9

Pada code diatas, saya ingin mengeprint Hello world sebanyak 10 kali disertai angka iterasinya.
Iterasi di java selalu di mulai dari 0

    





