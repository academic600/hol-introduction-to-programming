*ArrayList*
===========

.. note::

    Semua codingan yang ada disini jika di copy paste sama persis akan dianggap sebagai kecurangan


Sama seperti ``ArrayList``, ``ArrayList`` merupakan salah satu class dari ``java.util``.  Method yang terdapat pada ``ArrayList`` juga dimiliki oleh ``ArrayList`` Berikut adalah *syntax* yang dapat digunakan untuk mendeklarasikan sebuah ``ArrayList``.

.. code:: console

    import java.util.ArrayList;

    ArrayList<tipe_data> nama_arraylist = new ArrayList<>();

Menambahkan Data *ArrayList*
----------------------------

Berikut adalah contoh implementasi menambahkan data pada ``ArrayList`` menggunakan *method* ``add(data)`` dan ``add(index, data)``.

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            // Membuat object ArrayList yang menyimpan tipe data String
            ArrayList<String> language = new ArrayList<>();

            // Menambahkan data ke dalam ArrayList
            language.add("Java");
            language.add("C");
            language.add("Python");

            // Menampilkan data yang ada di dalam ArrayList
            System.out.println(language);

            // Menambahkan data berdasarkan index ke dalam ArrayList
            language.add(1, "Rust");

            // Menampilkan data yang ada di dalam ArrayList
            System.out.println(language);
        }
    }

.. code:: console

    [Java, C, Python]
    [Java, Rust, C, Python]

Menghilangkan Data *ArrayList*
------------------------------

Berikut adalah contoh implementasi menghilangkan data pada ``ArrayList`` menggunakan *method* ``remove(index)``.

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> language = new ArrayList<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            System.out.println(language);

            // Menghilangkan data berdasarkan index dari dalam ArrayList
            language.remove(2);

            // Menampilkan data yang ada di dalam ArrayList
            System.out.println(language);
        }
    }

.. code:: console

    [Java, Rust, C, Python]
    [Java, Rust, Python]

Mendapatkan Data *ArrayList*
----------------------------

Berikut adalah contoh implementasi mendapatkan data pada ``ArrayList`` menggunakan *method* ``get(index)``.

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> language = new ArrayList<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            // Mendapatkan data berdasarkan index dari dalam ArrayList
            System.out.println(language.get(0));
            System.out.println(language.get(1));
            System.out.println(language.get(2));
            System.out.println(language.get(3));
        }
    }

.. code:: console

    Java
    Rust
    C
    Python

Mengubah Data *ArrayList*
-------------------------

Berikut adalah contoh implementasi mengubah data pada ``ArrayList`` menggunakan *method* ``set(index, data)``.

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> language = new ArrayList<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            System.out.println(language);

            // Mengubah data berdasarkan index dari dalam ArrayList
            language.set(0, "Javascript");
            language.set(1, "C++");

            // Menampilkan data yang ada di dalam ArrayList
            System.out.println(language);
        }
    }


.. code:: console

    [Java, Rust, C, Python]
    [Javascript, C++, C, Python]

Mengecek Data *ArrayList*
-------------------------

Berikut adalah contoh implementasi mengecek data pada ``ArrayList`` menggunakan *method* ``size()`` dan ``isEmpty()``.

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> language = new ArrayList<>();

            if (language.isEmpty()) {
                System.out.println("Tidak ada bahasa yang disimpan");
            } else {
                System.out.println("Terdapat " + language.size() + " yang disimpan");
            }

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            if (language.isEmpty()) {
                System.out.println("Tidak ada bahasa yang disimpan");
            } else {
                System.out.println("Terdapat " + language.size() + " bahasa yang disimpan");
            }
        }
    }


.. code:: console

    Tidak ada bahasa yang disimpan
    Terdapat 4 bahasa yang disimpan
