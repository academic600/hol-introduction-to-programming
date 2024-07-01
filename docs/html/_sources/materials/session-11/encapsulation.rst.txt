*Encapsulation*
===============

Setelah mempelajari tentang *class* dan *object*, selanjutnya akan dibahas mengenai *Object Oriented Programming* (OOP). Terdapat tiga prinsip dasar yang perlu dipelajari mengenai OOP sehingga program yang dibuat dapat lebih efektif. Ketiga prinsip dasar tersebut adalah *encapsulation* (enkapsulasi), *inheritance* (pewarisan), dan *polymorphism* (polimorfisme). Pada bagian ini akan dibahas mengenai *encapsulation* (enkapsulasi).

Sesuai dengan namanya, *encapsulation* (enkapsulasi) artinya membungkus sebuah *class* dengan tujuan membatasi *class* lain untuk mengakses atribut secara langsung. Caranya adalah dengan menggunakan *access modifier* yang sudah dipelajari pada materi sebelumnya. Umumnya *access modifierlain* yang akan digunakan adalah ``private``. *Access modifier* ini memungkinkan atribut hanya dapat diakses oleh *class* bersangkutan saja. Nantinya, *class* lain dapat mengakses atribut tersebut dengan menggunakan *method getter* atau *accessor*. Sedangkan, untuk mengubah atribut dari *class* lain dapat menggunakan method *setter* atau *mutator*.

.. note:: 

    Pada aplikasi Eclipse, terdapat *shortcut* untuk dapat membuat *method getter* dan *setter* secara otomatis. Tekan tombol ``ALT`` + ``SHIFT`` + ``S`` secara bersamaan, kemudian tekan tombol ``R``.

    .. image:: /images/session-11/setter-getter-shortcut.png
        :width: 300
        :align: center
    .. centered:: Tampilan shortcut *Method Getter* dan *Setter*
    
    Pada *window* konfigurasi yang muncul, pilih *method* yang ingin dibuat. Gunakan tombol "*Select All*" yang ada pada bagian kanan untuk memilih semua *method*. Apabila sudah, tekan tombol *Generate*.

    .. image:: /images/session-11/setter-getter-setting.png
        :width: 350
        :align: center
    .. centered:: Tampilan konfigurasi *Method Getter* dan *Setter*

Berikut adalah contoh implementasi *encapsulation* (enkapsulasi) pada sebuah *class*.

.. code:: java

    public class Main {
        
        public class Mobil {
            // Atribut yang dimiliki oleh class Mahasiswa
            private String jenis;
            private String warna;
            private int tahun;
            
            // Method getter untuk atribut jenis bernama getJenis()
            public String getJenis() {
                return jenis;
            }
            // Method setter untuk atribut jenis bernama setJenis()
            public void setJenis(String jenis) {
                this.jenis = jenis;
            }
			
            // Method getter untuk atribut warna bernama getWarna()
            public String getWarna() {
                return warna;
            }
            // Method setter untuk atribut warna bernama setWarna()
            public void setWarna(String warna) {
                this.warna = warna;
            }
            
            // Method getter untuk atribut tahun bernama getTahun()
            public int getTahun() {
                return tahun;
            }
            // Method setter untuk atribut tahun bernama setTahun()
            public void setTahun(int tahun) {
                this.tahun = tahun;
            }
        }
        
        public Main() {
            // Membuat object dari class Mobil
            Mobil mobil = new Mobil();

            // Mengubah atribut menggunakan setter
            mobil.setJenis("SUV");
            mobil.setWarna("Hitam");
            mobil.setTahun(2023);

            // Mengakses atribut menggunakan getter
            System.out.println("Jenis: " + mobil.getJenis());
            System.out.println("Warna: " + mobil.getWarna());
            System.out.println("Tahun: " + mobil.getTahun());
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    Jenis: SUV
    Warna: Hitam
    Tahun: 2023
