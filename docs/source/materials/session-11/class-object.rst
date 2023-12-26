*Class* dan *Object*
====================

Pada materi sebelumnya, sudah dipelajari bagaimana cara menggunakan *class* dan membuat *object* yang sudah disediakan oleh bahasa pemrograman *Java*. Pada materi ini akan dibahas lebih dalam mengenai *class* dan *object*.

*Class*
-------

*Class* merupakan *blueprint* yang digunakan untuk membuat sebuah *object*. Di dalam sebuah *class*, digambarkan karakteristik sebuah *object*, seperti atribut (variabel) dan perilaku (*method*). Misalkan ingin dibuat *class* mahasiswa. Atribut yang dimiliki oleh *class* tersebut adalah NIM, nama, semester, GPA, dan lainnya. Sedangkan, perilaku yang dimiliki oleh *class* tersebut adalah absen(), belajar(), dan lainnya. 

Berikut adalah implementasi kode dalam membuat *class* berdasarkan contoh di atas.

.. code:: java

    // Deklarasi class Mahasiswa
    public class Mahasiswa {

        // Atribut yang dimiliki oleh class Mahasiswa
        public String NIM;
        public String nama;
        public int semester;
        public double GPA;

        // Perilaku yang dimiliki oleh class Mahasiswa
        public void absen() {
            System.out.println("Mhasiswa berhasil absen.");
        }
        public void belajar() {
            System.out.println("Mahasiswa sedang belajar.");
        }
    }

*Object*
--------

Seperti yang sudah dijelaskan sebelumnya, *object* merupakan hasil *instance* dari sebuah *class*. *Object* dapat dibuat dengan memanggil *constructor* dari *class* tersebut. Ketika sebuah *object* dibuat, semua atribut dan *method* yang sudah didefinisikan di dalam *class* dapat langsung digunakan. 

Berikut adalah implementasi kode dalam membuat *object* dari *class* yang sudah dibuat pada contoh di atas.

.. code:: java

    public class Main {

        // Deklarasi class Mahasiswa, yang sudah dibuat sebelumnya
        public class Mahasiswa {
            public String NIM;
            public String nama;
            public int semester;
            public double GPA;

            public void absen() {
                System.out.println("Mahasiswa berhasil absen.");
            }
            public void belajar() {
                System.out.println("Mahasiswa sedang belajar.");
            }
        }

        public Main() {

            // Membuat object dari class Mahasiswa
            Mahasiswa mahasiswa = new Mahasiswa();

            // Menampilkan isi atribut dari class Mahasiswa
            System.out.println("NIM = " + mahasiswa.NIM);
            System.out.println("Nama = " + mahasiswa.nama);
            System.out.println("semester = " + mahasiswa.semester);
            System.out.println("GPA = " + mahasiswa.GPA);

            // Memanggil perilaku dari class Mahasiswa
            mahasiswa.absen();
            mahasiswa.belajar();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console

    NIM = null
    Nama = null
    semester = 0
    GPA = 0.0
    Mahasiswa berhasil absen.
    Mahasiswa sedang belajar.

Pada kode di atas, atribut yang dimiliki pada *class* Mahasiswa masih bernilai *default*. Selain itu, *method* yang dimiliki juga melakukan *output* secara statis. Oleh karena itu, perlu dibuat *constructor* pada *class* Mahasiswa untuk menginisialisasikan atribut.

.. code:: java

    public class Main {

        public class Mahasiswa {
            public String NIM;
            public String nama;
            public int semester;
            public double GPA;

            // Membuat constructor untuk melakukan inisialisasi atribut
            public Mahasiswa(String NIM, String nama, int semester, double GPA) {
                this.NIM = NIM;
                this.nama = nama;
                this.semester = semester;
                this.GPA = GPA;
            }

            public void absen() {
                System.out.println("Mahasiswa dengan NIM " + this.NIM + " berhasil absen.");
            }
            public void belajar() {
                System.out.println("Mahasiswa dengan nama " + this.nama + " sedang belajar.");
            }
        }

        public Main() {

            // Membuat object dari class Mahasiswa dengan inisialisasi atribut
            Mahasiswa mahasiswa = new Mahasiswa("2200112233", "Java", 3, 3.95);

            System.out.println("NIM = " + mahasiswa.NIM);
            System.out.println("Nama = " + mahasiswa.nama);
            System.out.println("semester = " + mahasiswa.semester);
            System.out.println("GPA = " + mahasiswa.GPA);

            mahasiswa.absen();
            mahasiswa.belajar();
        }
        
        public static void main(String[] args) {
            new Main();
        }
    }

.. code:: console
    
    NIM = 2200112233
    Nama = Java
    semester = 3
    GPA = 3.95
    Mahasiswa dengan NIM 2200112233 berhasil absen.
    Mahasiswa dengan nama Java sedang belajar.

.. note:: 

    Pada saat melakukan inisialisasi atribut pada *class* Mahasiswa di dalam *constructor*, digunakan kata kunci ``this``. Kata kunci ``this`` merupakan refrensi ke *object* tersebut. Apabila tidak menggunakan kata kunci tersebut, kode akan berubah menjadi ``NIM = NIM``, yang dapat menimbulkan ambiguitas. Oleh karena itu, kode dibuat menjadi ``this.NIM = NIM``, artinya variabel NIM pada *class* Mahasiswa diubah berdasarkan nilai dari variabel NIM pada parameter *constructor*.
