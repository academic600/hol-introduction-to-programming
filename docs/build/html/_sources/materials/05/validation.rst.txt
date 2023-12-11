Validation
------------
Validasi adalah proses memeriksa apakah data atau input memenuhi syarat atau kriteria tertentu yang ditetapkan sebelumnya.

**Tujuan :**
untuk memastikan bahwa data atau input tersebut sesuai dengan format yang diharapkan atau memenuhi kondisi yang diperlukan untuk penggunaan selanjutnya dalam sistem atau aplikasi.

Validasi di java bisa kita lakukan dengan do-while loop, if-else, dan while loop. 

Contoh Validasi
~~~~~~~~~~~~~~~
Validasi panjang kata 

**Code**

.. code:: java

     public static void main(String[] args) {
    	Scanner scan = new Scanner(System.in);
    	String name;
    	
    	do {
    		
    		System.out.print("Input name [5-20 character]: ");
    		name = scan.nextLine();
			
		} while (name.length() < 5 || name.length() > 20 );
    	
    	System.out.println("Success input your name " + name);
    }


**Input/Output**

.. code:: console

    Input name [5-20 character]: er
    Input name [5-20 character]: erik
    Input name [5-20 character]: erika
    Success input your name erika

Pada kode diatas terdapat validasi nama yang dimana hanya di perbolehkan terdapat 5 - 20 huruf saja dalam suatu kata, jika kondisi tersebut tidak terpenuhi
maka, do-while loop akan meminta input kembali. 

Masih banyak jenis-jenis validasi lainnya yang bisa kita lakukan. Kita hanya perlu menyesuaikan apa kondisi yang dibutuhkan. 



