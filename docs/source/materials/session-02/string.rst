*String Method*
===============

*String* merupakan tipe data untuk menyimpan sebuah kalimat. Kalimat tersebut diapit dengan menggunakan tanda petik dua (``""``). Karena *string* merupakan sebuah *class* yang sudah dibuat oleh bahasa pemrograman *Java*, maka sudah tersedia beberapa *method* yang pembuat program dapat langsung gunakan.

Berikut adalah beberapa *string method* umum yang sering digunakan.

length()
--------

*Method* ``length()`` digunakan untuk menghitung jumlah karakter dalam sebuah *string*.

.. code:: java
    
    public class Main {
        public static void main(String[] args) {
            String city = "Jakarta";
            int cityLength = city.length();
            System.out.println(cityLength); // Output: 7

            String region = "Indonesia";
            int regionLength = region.length();
            System.out.println(regionLength); // Output: 9
        }
    }

charAt(index)
-------------

*Method* ``charAt(index)`` digunakan untuk mendapatkan karakter sesuai dengan ``index`` yang diberikan dalam sebuah *string*.

.. note:: 

    *Index* pada bahasa pemrograman *Java* dimulai dari 0. Artinya huruf ke-1 memiliki *index* ke-0, huruf ke-2 memiliki *index* ke-1, dan seterusnya.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String city = "Jakarta";

            char character1 = city.charAt(0);
            System.out.println(character1); // Output: J

            char character3 = city.charAt(2);
            System.out.println(character3); // Output: k
        }
    }

toUpperCase()
-------------

*Method* ``toUpperCase()`` digunakan untuk mengubah semua karakter dalam *string* menjadi huruf kapital.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String city = "Jakarta";
            String upperCity = city.toUpperCase();
            System.out.println(upperCity); // Output: JAKARTA
            
            String region = "Indonesia";
            String upperRegion = region.toUpperCase();
            System.out.println(upperRegion); // Output: INDONESIA
        }
    }

toLowerCase()
-------------

*Method* ``toLowerCase()`` digunakan untuk mengubah semua karakter dalam *string* menjadi huruf kecil.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String city = "Jakarta";
            String lowerCity = city.toLowerCase();
            System.out.println(lowerCity); // Output: jakarta
            
            String region = "Indonesia";
            String lowerRegion = region.toLowerCase(); 
            System.out.println(lowerRegion); // Output: indonesia
        }
    }

contains(str)
-------------

*Method* ``contains(str)`` digunakan untuk mengecek apakah sebuah *string* mengandung kata atau kalimat dari *parameter* ``str``, secara *case sensitive*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence = "The quick brown fox jumps over the lazy dog";

            String find1 = "fox";
            boolean isContains1 = sentence.contains(find1);
            System.out.println(isContains1); // Output: true

            String find2 = "DOG";
            boolean isContains2 = sentence.contains(find2);
            System.out.println(isContains2); // Output: false
        } 
    }

startsWith(str)
---------------

*Method* ``startsWith(str)`` digunakan untuk mengecek apakah sebuah *string* dimulai dengan kata atau kalimat dari *parameter* ``str``, secara *case sensitive*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence = "The quick brown fox jumps over the lazy dog";
            
            String find1 = "The quick";
            boolean isStartsWith1 = sentence.startsWith(find1);
            System.out.println(isStartsWith1); // Output: true

            String find2 = "the quick";
            boolean isStartsWith2 = sentence.startsWith(find2);
            System.out.println(isStartsWith2); // Output: false

            String find3 = "lazy dog";
            boolean isStartsWith3 = sentence.startsWith(find3);
            System.out.println(isStartsWith3); // Output: false
        }
    }

endsWith(str)
-------------

*Method* ``endsWith(str)`` digunakan untuk mengecek apakah sebuah *string* diakhiri dengan kata atau kalimat dari *parameter* ``str``, secara *case sensitive*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence = "The quick brown fox jumps over the lazy dog";
            
            String find1 = "The quick";
            boolean isEndsWith1 = sentence.endsWith(find1);
            System.out.println(isEndsWith1); // Output: false

            String find2 = "Lazy Dog";
            boolean isEndsWith2 = sentence.endsWith(find2);
            System.out.println(isEndsWith2); // Output: false

            String find3 = "lazy dog";
            boolean isEndsWith3 = sentence.endsWith(find3);
            System.out.println(isEndsWith3); // Output: true
        }
    }

equals(str)
-----------

*Method* ``equals(str)`` digunakan untuk mengecek apakah sebuah *string* sama seperti dengan kata atau kalimat dari *parameter* ``str``, secara *case sensitive*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence1 = "The Quick Brown Fox Jumps Over the Lazy Dog";
            String sentence2 = "The Quick Brown Fox Jumps Over the Lazy Dog";
            String sentence3 = "The quick brown fox jumps over the lazy dog";
            
            boolean isEquals1 = sentence1.equals(sentence2);
            System.out.println(isEquals1); // Output: true

            boolean isEquals2 = sentence1.equals(sentence3);
            System.out.println(isEquals2); // Output: false
        }
    }

equalsIgnoreCase(str)
---------------------

*Method* ``equalsIgnoreCase(str)`` digunakan untuk mengecek apakah sebuah *string* sama seperti dengan kata atau kalimat dari *parameter* ``str``, secara *case insensitive*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence1 = "The Quick Brown Fox Jumps Over the Lazy Dog";
            String sentence2 = "The Quick Brown Fox Jumps Over the Lazy Dog";
            String sentence3 = "The quick brown fox jumps over the lazy dog";
            
            boolean isEquals1 = sentence1.equalsIgnoreCase(sentence2);
            System.out.println(isEquals1); // Output: true

            boolean isEquals2 = sentence1.equalsIgnoreCase(sentence3);
            System.out.println(isEquals2); // Output: true
        }
    }

*isEmpty* 
-----------

*Method* ``isEmpty()`` digunakan untuk mengecek apakah *string* tersebut tidak memiliki isi (kosong).

.. code:: java

    public class Main {
        public static void main(String[] args) {
            String sentence1 = "The quick brown fox jumps over the lazy dog";
            String sentence2 = "";
            
            boolean isEmpty1 = sentence1.isEmpty();
            System.out.println(isEmpty1); // Output: false

            boolean isEmpty2 = sentence2.isEmpty();
            System.out.println(isEmpty2); // Output: true
        }
    }

*trim*
------------

*Method* ``trim()`` digunakan untuk menghapus whitespace yang berada di akhir *String*.

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            String name1 = "Gunawan ";
            System.out.println(name1); // Output: "Gunawan "

            String name2 = "Gunawan";
            System.out.println(name2); // Output: "Gunawan" 
        }
    }


*split*
------------

*Method* ``split()`` digunakan untuk memisahkan *String* menjadi suatu data yang bertipe array. Pada ``split()`` dibutuhkan parameter dalam penggunaannya. 
Parameter tersebut berfungsi untuk memisahkan string menjadi beberapa bagian dalam bentuk array. 

.. code:: java 

    public class Main {
        public static void main(String[] args){
            String text = "Budi Gunawan";
            String[] arr_text = text.split(" "); // ["Budi", "Gunawan"]
            System.out.println(arr_text[0]); // Output: "Budi"
            System.out.println(arr_text[1]); // Output: "Gunawan"
        }
    }


*substring*
--------------

*Method* ``substring()`` digunakan untuk menambilkan suatu data *String* berdasarkan index dari *String* tersebut.

.. code:: java 

    public class Main {
        public static void main(String[] args) {
            String text = "Budiman";
            System.out.println(text.substring(1)); // Output: "udiman"
        }
    }


*replace*
---------------

*Method* ``replace()`` digunakan untuk mengganti character dari *String* menjadi sebuah character yang baru.

.. code:: java 
    
    public class Main {
        public static void main(String[] args) {
            String text = "Budiman";
            System.out.println(text.replace("Bu", "Lu")); // Output: "Ludiman"
        }
    }


