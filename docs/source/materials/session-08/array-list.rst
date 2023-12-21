Array List 
----------------

Kelas ``ArrayList`` adalah ``array`` yang dapat diubah ukurannya, yang dapat ditemukan dalam paket ``java.util``.  merepresentasikan sebuah daftar (list) yang dapat diubah ukurannya secara dinamis. Ini memungkinkan penyimpanan koleksi elemen dalam urutan tertentu dan memungkinkan penambahan, penghapusan, dan akses elemen dengan menggunakan indeks. ``ArrayList`` memungkinkan penyimpanan objek dari berbagai tipe data. Perbedaan dengan ``built-in array`` adalah ``array list`` dapat di tambahkan, hapus, data sedangkan ``array`` biasa tidak dapat diubah, kita harus membuat ``array`` baru.



Berikut simtaks array list : 

.. code:: console

    import java.util.ArrayList; // import  ArrayList class

    ArrayList<TipeData> namaList = new ArrayList<TipeData>(); // Buat array list object


.. code:: console

    import java.util.ArrayList; 

    ArrayList<String> cars = new ArrayList<String>(); 


Add Data ArrayList
~~~~~~~~~~~~~~~~~~~~~~~
Jika kita ingin menambagkan suatu data ke dalam ``array list`` kita , terdapat method ``.add()``, untuk menambahkan data kepada ``array list`` yang kita punya. 

.. code:: java

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
                ArrayList<String> cars = new ArrayList<String>();
                //menambahkan data ke dalam array list
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                System.out.println(cars);
        }
    }


.. code:: console

    [Volvo, BMW, Ford, Mazda]


Akses ArrayList
~~~~~~~~~~~~~~~~~~~~~~~~
Untuk mengkases array list kita bisa memakai method ``.get()``, method ini menerima parameter ``index``, jadi kita bisa memasukan index dari array list yang ingin di ambil. 

.. code:: java 

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
                ArrayList<String> cars = new ArrayList<String>();
                //menambahkan data ke dalam array list
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");

                System.out.println(cars);

                // Mengakses elemen dengan indeks menggunakan method get
                String car = cars.get(0);
                System.out.println("Mobil di indeks ke-0: " + car);


        }
    }


.. code:: console

    [Volvo, BMW, Ford, Mazda]
    Mobil di indeks ke-0: Volvo


*Remove Data Array List*
=========================
Untuk menhapus data dalam array list kita dapat menggunakan method ``.remove()``, method ini menerima parameter ``index``, jadi jika kita ingin menghapus data kita tinggal masukan saja ``index`` data yang ingin kita hapus.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> cars = new ArrayList<String>();
            
            // Menambahkan data ke dalam array list
            cars.add("Volvo");
            cars.add("BMW");
            cars.add("Ford");
            cars.add("Mazda");

            System.out.println("Data awal: " + cars);

            // Mengakses elemen dengan indeks menggunakan method get
            String car = cars.get(0);
            System.out.println("Mobil di indeks ke-0: " + car);

            // Menghapus elemen dengan method remove
            cars.remove(2);
            System.out.println("Setelah menghapus indeks ke-2: " + cars);
        }
    }

.. code:: console

    Data awal: [Volvo, BMW, Ford, Mazda]
    Mobil di indeks ke-0: Volvo
    Setelah menghapus indeks ke-2: [Volvo, BMW, Mazda]

Mengakses ukuran array list
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Kita bis mengetahui ukuran dari suatu ``array list`` yang kita punya dengan menggunakan method ``.size()``,method ini berfungsi untuk mengambil jumlah data yang ada di dalam ``array list kita``. 
Biasanya kita juga bisa memakai .size() saat validasi untuk mengechek apakah ada data atau tidak pada ``array list``

.. code:: java

    import java.util.ArrayList;

    public class Main {
        public static void main(String[] args) {
            ArrayList<String> fruits = new ArrayList<String>();

            // Menambahkan elemen ke dalam ArrayList
            fruits.add("Apple");
            fruits.add("Banana");
            fruits.add("Orange");
            fruits.add("Mango");

            // Mendapatkan ukuran atau panjang ArrayList menggunakan method size
            int size = fruits.size();
            System.out.println("Ukuran ArrayList: " + size);
        }
    }


.. code:: console


    Ukuran ArrayList: 4
