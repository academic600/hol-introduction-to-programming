*Vector* 
========

``Vector`` dalam bahasa pemrograman *Java* merupakan salah satu class dari ``java.util``. Berikut adalah *syntax* yang dapat digunakan untuk mendeklarasikan sebuah ``Vector``.

.. code:: console

    import java.util.Vector;

    Vector<tipe_data> nama_vector = new Vector<>();

Terdapat beberapa *method* pada ``Vector`` yang sering digunakan. Berikut adalah nama dan kegunaan dari *method* tersebut.

.. list-table::
   :widths: 40 60
   :header-rows: 1

   * - *Method*
     - Penjelasan
   * - ``add(data)``
     - Menambahkan sebuah ``data`` ke dalam ``Vector``.
   * - ``add(index, data)``
     - Menambahkan sebuah ``data`` ke dalam ``Vector`` pada ``index`` yang diberikan.
   * - ``remove(index)``
     - Menghapus sebuah data pada ``index`` yang diberikan dari ``Vector``.
   * - ``get(index)``
     - Mendapatkan sebuah data pada ``index`` yang diberikan dari ``Vector``.
   * - ``set(index, newData)``
     - Mengubah sebuah data menjadi ``newData`` pada ``index`` yang diberikan dari ``Vector``.
   * - ``size()``
     - Mendapatkan jumlah data dari sebuah ``Vector``.
   * - ``isEmpty()``
     - Mengecek apakah sebuah ``Vector`` kosong atau tidak.

Menambahkan Data *Vector*
-------------------------

Berikut adalah contoh implementasi menambahkan data pada ``Vector`` menggunakan *method* ``add(data)`` dan ``add(index, data)``.

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            // Membuat object Vector yang menyimpan tipe data String
            Vector<String> language = new Vector<>();

            // Menambahkan data ke dalam Vector
            language.add("Java");
            language.add("C");
            language.add("Python");

            // Menampilkan data yang ada di dalam Vector
            System.out.println(language);

            // Menambahkan data berdasarkan index ke dalam Vector
            language.add(1, "Rust");

            // Menampilkan data yang ada di dalam Vector
            System.out.println(language);
        }
    }

.. code:: console

    [Java, C, Python]
    [Java, Rust, C, Python]

Berdasarkan kode di atas, *method* ``add(data)`` akan menambahkan data ke paling belakang, sehingga data ditampilkan pada *console* berurutan sesuai dengan ketika data dimasukan. Sedangkan, *method* ``add(index, data)`` akan menambahkan data sesuai dengan index yang diberikan.

Menghilangkan Data *Vector*
---------------------------

Berikut adalah contoh implementasi menghilangkan data pada ``Vector`` menggunakan *method* ``remove(index)``.

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            Vector<String> language = new Vector<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            System.out.println(language);

            // Menghilangkan data berdasarkan index dari dalam Vector
            language.remove(2);

            // Menampilkan data yang ada di dalam Vector
            System.out.println(language);
        }
    }

.. code:: console

    [Java, Rust, C, Python]
    [Java, Rust, Python]

Mendapatkan Data *Vector*
-------------------------

Berikut adalah contoh implementasi mendapatkan data pada ``Vector`` menggunakan *method* ``get(index)``.

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            Vector<String> language = new Vector<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            // Mendapatkan data berdasarkan index dari dalam Vector
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

.. note:: 

    Pastikan *index* yang diakses dari sebuah ``Vector`` itu memiliki data. Apabila tidak, akan muncul *error* ``java.lang.ArrayIndexOutOfBoundsException`` karena program akan membaca data di luar batas yang dimiliki.

Mengubah Data *Vector*
----------------------

Berikut adalah contoh implementasi mengubah data pada ``Vector`` menggunakan *method* ``set(index, data)``.

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            Vector<String> language = new Vector<>();

            language.add("Java");
            language.add("C");
            language.add("Python");
            language.add(1, "Rust");

            System.out.println(language);

            // Mengubah data berdasarkan index dari dalam Vector
            language.set(0, "Javascript");
            language.set(1, "C++");

            // Menampilkan data yang ada di dalam Vector
            System.out.println(language);
        }
    }

.. code:: console

    [Java, Rust, C, Python]
    [Javascript, C++, C, Python]

Mengecek Data *Vector*
----------------------

Berikut adalah contoh implementasi mengecek data pada ``Vector`` menggunakan *method* ``size()`` dan ``isEmpty()``.

.. code:: java 

    import java.util.Vector;

    public class Main {
        public static void main(String[] args) {
            Vector<String> language = new Vector<>();

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

Pada kode diatas, dilakukan deklarasi sebuah ``Vector`` yang masih kosong, belum memiliki data. Setelah itu, terdapat sebuah seleksi yang mengecek apakah ``Vector`` kosong atau tidak. Karena ``Vector`` tersebut masih kosong, maka akan masuk ke bagian ``if``, sehingga muncul "Tidak ada bahasa yang disimpan" pada *console* baris ke-1. Kemudian, dilakukan penambahan sebanyak 4 data. Terakhir, dilakukan selesi yang sama. Karena ``Vector`` sudah tidak kosong, maka akan masuk ke bagian ``else``, sehingga muncul "Terdapat 4 bahasa yang disimpan" pada *console* baris ke-2.
