Encapsulation
==================

Encapsulation adalah konsep dalam pemrograman yang mengizinkan pembatasan akses langsung ke bagian dalam suatu objek dan mendorong penggunaan metode (method) untuk mengakses atau mengubah data di dalam objek tersebut. Dengan menggunakan encapsulation, variabel-variabel di dalam suatu class disembunyikan atau dilindungi dari akses langsung oleh class lain, dan hanya dapat diakses melalui metode-metode yang telah ditentukan.

Sebuah bidang data private tidak dapat diakses oleh sebuah objek dari luar kelas yang menentukan bidang ``private`` tersebut. Namun, seringkali klien memerlukan untuk mengambil dan memodifikasi bidang data tersebut. Untuk membuat sebuah bidang data ``private`` dapat diakses, sediakan sebuah metode ``getter`` untuk mengembalikan nilainya. Untuk memungkinkan sebuah bidang data ``private`` diperbarui, sediakan sebuah metode ``setter`` untuk menetapkan nilai baru. Metode ``getter`` juga disebut sebagai ``accessor`` dan ``setter`` sebagai ``mutator``.

.. code:: java

    class Mobil {
        private String merek; // Variabel dienkapsulasi dengan akses private
        private String warna;
        private int tahunProduksi;

        // Metode untuk mengatur nilai merek
        public void setMerek(String merekBaru) {
            merek = merekBaru;
        }

        // Metode untuk mengambil nilai merek
        public String getMerek() {
            return merek;
        }

        // Metode untuk mengatur nilai warna
        public void setWarna(String warnaBaru) {
            warna = warnaBaru;
        }

        // Metode untuk mengambil nilai warna
        public String getWarna() {
            return warna;
        }

        // Metode untuk mengatur nilai tahunProduksi
        public void setTahunProduksi(int tahunBaru) {
            tahunProduksi = tahunBaru;
        }

        // Metode untuk mengambil nilai tahunProduksi
        public int getTahunProduksi() {
            return tahunProduksi;
        }
    }

    public class Main {
        public static void main(String[] args) {
            Mobil mobil = new Mobil();

            // Menggunakan metode setter untuk mengatur nilai atribut
            mobil.setMerek("Toyota");
            mobil.setWarna("Merah");
            mobil.setTahunProduksi(2020);

            // Menggunakan metode getter untuk mendapatkan nilai atribut
            System.out.println("Merek: " + mobil.getMerek());
            System.out.println("Warna: " + mobil.getWarna());
            System.out.println("Tahun Produksi: " + mobil.getTahunProduksi());
        }
    }

.. code:: console

    Merek: Toyota
    Warna: Merah
<<<<<<< Updated upstream
    Tahun Produksi: 2020
=======
    Tahun Produksi: 2020
>>>>>>> Stashed changes
