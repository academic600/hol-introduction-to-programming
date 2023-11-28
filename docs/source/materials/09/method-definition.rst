Method Definition
==================
Method adalah sebuah module blok code yang akan dijalankan ketika di panggil.
Fungsi dari method : agar bisa memecahkan program menjadi bagian-bagian yang lebih kecil dan kompleks agar bisa dipakai kembali. 

Method dapat mengembalikan nilai tertentu (memiliki return value), dan ada juga method yang tidak memiliki return value (void)

Struktur Method
---------------

.. image:: /images/01/method.webp


Penjelasan mengenai gambar diatas:
    * **Modifiers** 
    
      * Access Modifier: menentukan darimana method dapat di akses. terdapat beberapa jenis access Modifiers
     
         .. image:: /images/01/accessmodifier.webp

      *  Non-access Modifier: tidak berpengaruh pada sifat method, tapi memberikan sifat khusus pada method tersebut.Contohnya adalah static, final, dan abstract.
    
    * **Return type :** jika suatu method memiliki return type tertentu, maka tipe data yang ingin di return akan diletakan pada return type. jika suatu method tidak memiliki return type maka akan di sebut dengan ``void``
    * **Nama Method :** nama method biasanya dinamakan dengan camel case, diawali dengan huruf kecil. contoh diatas method nya bernama main.
    * **Parameter :** parameter atau argumen merupakan nilai masukkan yang perlu disertakan saat memanggil sebuah method. Parameter bersifat opsional, parameter juga dapat berjumlah  lebih dari satu.
  
Contoh Method
-------------
.. code:: java

    public class Main {
	
        public static int penjumlahanAngka(int a, int b) {
            int hasil = a + b;
            return hasil;
        }
        
        public static void main(String[] args) {
            //ditampung ke dalam variabel terlebih dahulu
            int hasil = penjumlahanAngka(2,3);
            System.out.println("Hasil yang di dapat: "  + hasil);

            //langsung diprint
            System.out.println("Hasil penjumlahan angka: " + penjumlahanAngka(10, 3));
        }


    }

Output:

.. code:: console

    Hasil yang di dapat: 5
    Hasil penjumlahan angka: 13

