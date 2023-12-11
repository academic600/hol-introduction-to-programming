*String Function*
--------------------
*String* dalam java adalah suatu tipe data untuk memuat suatu kalimat. 
penggunaan string biasanya di sertai dengan tanda petik dua ``""``.

Terdapat beberapa method-method dalam java untuk memanipulasi sebuah string. 

Simpel String
~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1

   * - Mehtod
     - Penjelasan
   * - length()
     - Mengembalikan banyak karakter dalam suatu *string*
   * - charAt(index)
     - Mengembalikan karakter sesuai index dari suatu *string*
   * - concat(s1)
     - Mengembalikan sebuah string baru yang menggabungkan string ini dengan string s1.
   * - toUpperCase()
     - Mengembalikan karakter dengan huruf kapital
   * - toLowerCase()
     - Mengembalikan karakter dengan huruf kecil 
   * - trim()
     - Mengembalikan sebuah string baru dengan karakter spasi di kedua sisinya.


**CharAt** 
~~~~~~~~~~~

Char at digunakan untuk mengambil karakter dari sebuah string pada posisi tertentu (berdasarkan indeks karakter)

.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan charAt
            String text = "Hello";
            char character = text.charAt(0); // Mengambil karakter pertama (index 0)
            System.out.println("Karakter pertama: " + character);
            
        }

    }
	
.. code:: 

    Karakter pertama: H


*toUpperCase*
~~~~~~~~~~~~~~
Digunakan untuk mengubah *string* menjadi huruf kapital. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
           String textToLowerCase = "HURUF KECIL";
           System.out.println("Uppercase: " + textToUpperCase.toUpperCase());
        }

   }

.. code:: console

    Uppercase: HURUF BESAR


*toLowerCase*
~~~~~~~~~~~~~~~
Digunakan untuk mengubah *string* menjadi huruf kecil.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan toUpperCase dan toLowerCase
            String textToUpperCase = "huruf besar";     
            System.out.println("Lowercase: " + textToLowerCase.toLowerCase());
        }

   }

.. code:: console

   Lowercase: huruf kecil




Comparing String
~~~~~~~~~~~~~~~~~
.. list-table::
   :header-rows: 1

   * - Mehtod
     - Penjelasan
   * - equals(s1)
     - Mengembalikan banyak karakter dalam suatu *string*
   * - equalIgnoreCase(s1)
     - Mengembalikan karakter sesuai index dari suatu *string*
   * - compareTo(s1)
     - Mengembalikan sebuah string baru yang menggabungkan string ini dengan string s1.
   * - compareToIgnoreCase(s1)
     - Mengembalikan karakter dengan huruf kapital
   * - startsWith(prefix)
     - Mengembalikan karakter dengan huruf kecil 
   * - endsWith(suffix)
     - Mengembalikan true jika akhir dari *string* sesuai dengan sufix yang di spesifikasi
   * - contains(s1)
     - Mengembalikan true jika akhir dari *string* sesuai dengan sufix yang di spesifikasi





*Contains* 
~~~~~~~~~~~~~
Digunakan untuk mengechek apakah suatu string mengandung kalimat atau kata yang diinginkan sesuai kondisi. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan contains
            String sentence = "Ini adalah contoh kalimat.";
            boolean containsWord = sentence.contains("contoh");
            System.out.println("Mengandung kata 'contoh': " + containsWord);
            
        }

   }

.. code:: console

    Mengandung kata 'contoh': true



*StartWith* 
~~~~~~~~~~~~
Digunakan untuk mengechek apakah awalan suatu *string* sudah  benar memenuhi kondisi yang di inginkan. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan startsWith
            String prefixCheck = "Nama saya adalah";
            boolean startsWithCheck = prefixCheck.startsWith("Nama");
            System.out.println("Dimulai dengan 'Nama': " + startsWithCheck);
        }

   }

.. code:: console

    Dimulai dengan 'Nama': true



*EndsWith* 
~~~~~~~~~~
Digunakan untuk mengechek pada akhiran *string* apakah sudah sesuai dengan kondisi yang diinginkan. 

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan endsWith
            String suffixCheck = "Saya suka programming.";
            boolean endsWithCheck = suffixCheck.endsWith("programming.");
            System.out.println("Berakhir dengan 'programming.': " + endsWithCheck);
        }

   }

.. code:: console

    Berakhir dengan 'programming.': true


*Equals* 
~~~~~~~~~
Digunakan untuk mengechek apakah *string* yang di input sudah sama sesuai dengan kondisi yang di inginkan, 
mengechek kesamaan string.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan equals
            String str1 = "Hello";
            String str2 = "hello";
            boolean isEqual = str1.equals(str2);
            System.out.println("String str1 sama dengan str2: " + isEqual);
        }

   }

.. code:: console

    String str1 sama dengan str2: false

*isEmpty* 
~~~~~~~~~~~
Digunakan untuk mengechek suatu string apakah *string* tersebut memiliki isi atau kosong. jika kosong maka akan mereturn true, jika tidak maka akan mereturn false.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            // Contoh penggunaan isEmpty
            String emptyString = "";
            boolean isEmpty = emptyString.isEmpty();
            System.out.println("String kosong: " + isEmpty);
        }

   }

.. code:: console

   String kosong: true





