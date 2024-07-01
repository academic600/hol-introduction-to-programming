*Type Casting*
==============

Dalam membuat sebuah program, terkadang dibutuhkan untuk mengubah sebuah tipe data ke tipe data yang lainnya. Proses ini disebut juga sebagai *type casting*. 

Terdapat dua macam tipe *type casting*, yaitu *implicit casting* dan *explicit casting*.

*Implicit Casting* 
------------------

*Implicit casting* yang biasanya disebut juga sebagai *widening casting*, merupakan *type casting* yang dilakukan secara otomatis oleh *compiler*. Hal ini dilakukan untuk mengubah tipe data yang ukurannya lebih kecil ke lebih besar, tanpa kehilangan informasi. 
    
.. image:: /images/session-02/implicit-casting.png
    :width: 500
    :align: center
.. centered:: *Implicit Casting*

Gambar diatas merupakan *type casting* yang dapat dilakukan secara otomatis. Contohnya adalah tipe data ``byte`` hanya dapat diubah menjadi ``short``, ``int``, ``long``, ``float``, ``double``, dan ``boolean``. Contoh lainnya adalah tipe data ``long`` hanya dapat diubah menjadi ``float``, ``double``, dan ``boolean``.

Berikut adalah contoh penggunaan *implict casting*.

.. code:: java

    public class Main {
        public static void main(String[] args) {
            int bilangan_bulat = 9;
            double bilangan_desimal = bilangan_bulat; // implicit casting dari int ke double

            System.out.println(bilangan_bulat);     
            System.out.println(bilangan_desimal);   
        }
    }

.. code:: console

    9
    9.0

*Explicit Casting*
------------------

*Explicit casting* yang biasanya disebut juga sebagai *narrowing casting*, merupakan *type casting* yang dilakukan secara manual oleh pembuat program. Hal ini dilakukan untuk mengubah tipe data yang ukurannya lebih besar ke lebih kecil, sehingga berpotensi kehilangan informasi. 

Untuk dapat melakukan explicit casting dapat menggunakan format sebagai berikut.

.. code:: console

    <tipedata_setelah> <nama_variabel> = (<tipedata_setelah>) <nama_variabel_sebelum>

.. code:: java

    public class Main {
        public static void main(String[] args) {
            double bilangan_desimal = 9.78;
            int bilangan_bulat = (int) bilangan_desimal; // explicit casting dari double ke int

            System.out.println(bilangan_desimal);
            System.out.println(bilangan_bulat);
        }
    }


.. code:: console

    9.78
    9

Pada kode di atas, nilai yang disimpan pada variabel ``bilangan_desimal`` adalah 9.78. Namun, setelah dilakukan *explicit casting* nilai pada variabel ``bilangan_bulat`` hanya 9 saja. Dari hasil tersebut, terlihat bahwa terdapat informasi yang hilang, yaitu digit desimal. Oleh karena itu, pembuat program perlu memperhatikan hal tersebut agar tidak ada informasi penting hilang saat dilakukan *type casting*.  
