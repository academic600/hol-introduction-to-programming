Seleksi *Switch-Case*
=====================

Selain dapat menggunakan seleksi *if*, pembuat program juga dapat menggunakan seleksi *switch-case* untuk membuat percabangan. Seleksi *switch-case* digunakan untuk memilih salah satu kasus atau kondisi yang sesuai berdasarkan nilai dari sebuah variabel. 

Berikut adalah *syntax* dari seleksi *switch-case*.

.. code:: console

    switch (variable) {
        case value_1:
            <statement-1>
            break;

        case value_2:
            <statement-2>
            break;

        default:
            <statement-n>
    }

Untuk dapat membuat seleksi *switch-case* tentukan variabel yang ingin dijadikan percabangan terlebih dahulu. Kasus atau validasi yang dipilih berdasarkan nilai dari variabel tersebut. Pengecekan dilakukan dari atas sesuai urutan baris kode. Apabila variabel tersebut sesuai dengan nilai yang ditentukan, maka perintah (*statement*) yang ada di dalamnya akan dijalankan. Bagian ``default`` digunakan apabila nilai dari variabel di atas tidak sesuai dengan kasus atau kondisi apapun. Hal ini bersifat opsional, artinya tidak wajib digunakan sesuai dengan kebutuhan.

.. note:: 

    Pada seleksi *switch-case*, setiap kasus atau kondisi harus diakhiri dengan kata kunci ``break``. Hal ini bertujuan agar program tidak menjalankan perintah (*statement*) dari kasus lainnya.

.. code:: java

    public class Main {
        
        public static void main(String[] args) {
            int hari = 3;

            switch (hari) {
                case 1:
                    System.out.println("Senin");
                    break;

                case 2:
                    System.out.println("Selasa");
                    break;

                case 3:
                    System.out.println("Rabu");
                    break;

                case 4:
                    System.out.println("Kamis");
                    break;

                case 5:
                    System.out.println("Jumat");
                    break;

                case 6:
                    System.out.println("Sabtu");
                    break;

                case 7:
                    System.out.println("Minggu");
                    break;

                default:
                    System.out.println("Tidak sesuai");
            }
        }
    }

.. code:: console

    Rabu

Pada seleksi *switch-case* di atas, kasus atau kondisi didasarkan pada variabel hari yang bernilai 3. Pertama, dilakukan pengecekan apakah variabel tersebut bernilai 1 dan hasilnya tidak sesuai. Kedua, dilakukan pengecekan apakah variabel tersebut bernilai 2 dan hasilnya tidak sesuai. Ketiga, dilakukan pengecekan apakah variabel tersebut bernilai 3 dan hasilnya sesuai. Oleh karena itu, perintah yang ada di dalam akan dijalankan, yaitu perintah *output* dan ``break``. Karena kata kunci ``break`` dipanggil, seleksi *switch-case* sudah berakhir, pengecekan kasus atau kondisi selanjutnya tidak dilakukan.
