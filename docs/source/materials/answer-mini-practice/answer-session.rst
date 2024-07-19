Answer Mini Practice All 
-------------------------------------

Berikut adalah jawaban dari mini practice untuk **session 1**. 

Answer mini practice session 1
-------------------------------------

.. code-block:: java 

    import java.util.Scanner;

    public class UserInfo {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Input nama
            System.out.print("Masukkan nama: ");
            String name = scanner.nextLine();

            // Input umur
            System.out.print("Masukkan umur: ");
            int age = scanner.nextInt();

            // Output informasi pengguna
            System.out.println("\nNama: " + name);
            System.out.println("Umur: " + age);
            
            scanner.close();
        }
    }

Program diatas adalah **answer** program dari **mini-practice** pada **session 1**.

Answer mini practice session 2
-------------------------------------

Dibawah ini merupakan **answer** untuk mini-practice **session 2**. 

.. code-block:: java 

    import java.util.Random;

    public class RandomIDGenerator {
        public static void main(String[] args) {
            Random random = new Random();
            
            // Menghasilkan angka acak antara 0 dan 999 (inklusif)
            int randomNumber = random.nextInt(1000);
            
            // Format ID dengan awalan "ID-" diikuti angka acak
            String randomID = String.format("ID-%03d", randomNumber);
            
            // Output ID acak
            System.out.println("Hasil random: " + randomID);
        }
    }


Answer mini practice session 3
-------------------------------------

Dibawah ini, merupakan **answer mini-practice** untuk **session 3**. 

.. code-block:: java

    import java.util.Scanner;

    public class SumCalculator {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Meminta pengguna untuk memasukkan dua angka
            System.out.print("Masukkan angka ke-1: ");
            int number1 = scanner.nextInt();

            System.out.print("Masukkan angka ke-2: ");
            int number2 = scanner.nextInt();

            // Menghitung penjumlahan
            int sum = number1 + number2;

            // Menampilkan hasil penjumlahan
            System.out.println("Hasil penjumlahan adalah: " + sum);

            // Menutup scanner
            scanner.close();
        }
    }

Answer mini practice session 4
-------------------------------------

Dibawah ini merupakan **answer mini-practice** untuk **session 4**.

.. code-block:: java 

    import java.util.Scanner;

    public class AgeCategory {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Meminta pengguna untuk memasukkan umur
            System.out.print("Masukkan umur: ");
            int age = scanner.nextInt();

            // Menentukan kategori berdasarkan umur
            if (age >= 18) {
                System.out.println("Anda adalah dewasa.");
            } else {
                System.out.println("Anda adalah anak-anak.");
            }

            // Menutup scanner
            scanner.close();
        }
    }

Answer mini practice session 5
-------------------------------------

Selanjutnya,dibawah ini merupakan **answer mini-practice** untuk **session 5**.

.. code-block:: java 

    import java.util.Scanner;

    public class EmailValidation {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            String email = "";
            boolean isValid = false;

            // Loop sampai input valid
            while (!isValid) {
                System.out.print("Masukkan email anda: ");
                email = scanner.nextLine();

                // Memeriksa apakah email diakhiri dengan "@gmail.com"
                if (email.endsWith("@gmail.com")) {
                    isValid = true;
                    System.out.println("Email anda sudah berhasil disimpan.");
                } else {
                    System.out.println("Email tidak valid. Harus diakhiri dengan '@gmail.com'. Coba lagi.");
                }
            }

            // Menutup scanner
            scanner.close();
        }
    }

Diatas ini merupakan **answer mini-practice** dari **session 5**. 

Answer mini practice session 6
-------------------------------------


Berikut adalah **answer mini-practice** untuk materi **session 6**.

.. code-block:: java 

    import java.util.Scanner;

    public class SimpleMenu {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            boolean exit = false;

            while (!exit) {
                // Menampilkan menu
                System.out.println("Selamat datang di ZYResto");
                System.out.println("==========================");
                System.out.println("1. Beli Barang");
                System.out.println("2. Retur Barang");
                System.out.println("3. Exit");
                System.out.print("Pilih menu (1-3): ");

                try {
                    // Membaca input pengguna
                    int choice = Integer.parseInt(scanner.nextLine());

                    // Menangani pilihan menu
                    switch (choice) {
                        case 1:
                            System.out.println("Anda memilih untuk Beli Barang.");
                            break;
                        case 2:
                            System.out.println("Anda memilih untuk Retur Barang.");
                            break;
                        case 3:
                            System.out.println("Anda memilih untuk Exit.");
                            exit = true;
                            break;
                        default:
                            System.out.println("Pilihan tidak valid. Silakan pilih antara 1-3.");
                            break;
                    }
                } catch (NumberFormatException e) {
                    System.out.println("Input tidak valid. Silakan masukkan angka antara 1-3.");
                }
            }

            // Menutup scanner
            scanner.close();
        }
    }

Answer mini practice session 7
-------------------------------------

Dibawah ini merupakan **answer mini-practice** untuk materi **session 7**.

.. code-block:: java 

    import java.util.Scanner;

    public class ArrayUpdate {
        public static void main(String[] args) {
            // Membuat array statis
            int[] array = {1, 2, 3, 4, 5};
            Scanner scanner = new Scanner(System.in);
            
            // Menampilkan array awal
            System.out.println("Array awal:");
            for (int i = 0; i < array.length; i++) {
                System.out.print(array[i] + " ");
            }
            System.out.println();
            
            // Meminta pengguna untuk memasukkan indeks yang ingin di-update
            int index = -1;
            boolean validIndex = false;
            while (!validIndex) {
                System.out.print("index array yang ingin diubah [0-4]: ");
                try {
                    index = Integer.parseInt(scanner.nextLine());
                    if (index >= 0 && index < array.length) {
                        validIndex = true;
                    } else {
                        System.out.println("Indeks di luar jangkauan. Silakan masukkan indeks antara 0 dan 4.");
                    }
                } catch (NumberFormatException e) {
                    System.out.println("Input tidak valid. Silakan masukkan angka.");
                }
            }
            
            // Meminta pengguna untuk memasukkan angka baru
            int newValue = 0;
            boolean validNumber = false;
            while (!validNumber) {
                System.out.print("Masukkan angka baru: ");
                try {
                    newValue = Integer.parseInt(scanner.nextLine());
                    validNumber = true;
                } catch (NumberFormatException e) {
                    System.out.println("Input tidak valid. Silakan masukkan angka.");
                }
            }
            
            // Meng-update array dengan nilai baru
            array[index] = newValue;
            
            // Menampilkan array yang sudah di-update
            
            for (int i = 0; i < array.length; i++) {
                System.out.print(array[i] + " ");
            }
            System.out.println();
            
            // Menutup scanner
            scanner.close();
        }
    }

Answer mini practice session 8
-------------------------------------

Selanjutnya, dibawah ini merupakan **answer mini-practice** untuk **session 8**.

.. code-block:: java 

    import java.util.ArrayList;
    import java.util.Scanner;

    public class VehicleSearch {
        public static void main(String[] args) {
            // Membuat ArrayList dan menambahkan data kendaraan
            ArrayList<String> vehicles = new ArrayList<>();
            vehicles.add("Mobil");
            vehicles.add("Kereta");
            vehicles.add("Motor");

            Scanner scanner = new Scanner(System.in);

            // Meminta pengguna untuk memasukkan data yang akan dicari
            System.out.print("Masukkan nama kendaraan yang ingin dicari: ");
            String searchQuery = scanner.nextLine();

            // Mencari data di dalam ArrayList
            if (vehicles.contains(searchQuery)) {
                System.out.println("Data berhasil ditemukan.");
            } else {
                System.out.println("Data tidak dapat ditemukan.");
            }

            // Menutup scanner
            scanner.close();
        }
    }

Answer mini practice session 9
-------------------------------------

Selanjutnya, dibawah ini merupakan **answer mini-practice** dari materi **session 9**.

.. code-block:: java 

    import java.util.Scanner;

    public class NameGender {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Menerima input untuk name dan gender
            System.out.print("Masukkan nama anda: ");
            String name = scanner.nextLine();

            System.out.print("Masukkan gender anda (Male/Female): ");
            String gender = scanner.nextLine();

            // Memanggil fungsi getName dan menampilkan hasilnya
            String result = getName(name, gender);
            System.out.println(result);

            // Menutup scanner
            scanner.close();
        }

        // Fungsi getName
        public static String getName(String name, String gender) {
            if (gender.equalsIgnoreCase("Male")) {
                return "Mr. " + name;
            } else if (gender.equalsIgnoreCase("Female")) {
                return "Ms. " + name;
            } else {
                return name; // Jika gender tidak valid, kembalikan nama tanpa perubahan
            }
        }
    }

Answer mini practice session 10
-------------------------------------

Berikutnya adalah **answer mini-practice** dari **session 10**. 

.. code-block:: java 

    import java.util.ArrayList;
    import java.util.Collections;

    public class BubbleSortExample {
        public static void main(String[] args) {
            // Membuat ArrayList dan menambahkan data sampel
            ArrayList<String> array_id = new ArrayList<>();
            array_id.add("ID01");
            array_id.add("ID02");
            array_id.add("ID03");

            // Melakukan sorting menggunakan Bubble Sort
            bubbleSort(array_id);

            // Menampilkan data setelah sorting
            System.out.println("Data setelah sorting: " + array_id);
        }

        // Fungsi untuk melakukan Bubble Sort
        public static void bubbleSort(ArrayList<String> array) {
            int n = array.size();
            for (int i = 0; i < n - 1; i++) {
                for (int j = 0; j < n - 1 - i; j++) {
                    if (array.get(j).compareTo(array.get(j + 1)) > 0) {
                        // Swap elements
                        Collections.swap(array, j, j + 1);
                    }
                }
            }
        }
    }

Answer mini practice session 11
-------------------------------------

Selanjutnya, dibawah ini merupakan **answer mini-practice** dari materi **session 11**. 

Dalam pembuatan jawaban project nya, kita akan membuat 3 file **java** sebagai salah satu bentuk untuk mempermudah dan memahami konsep **Object Oriented Programming**. 

.. code-block:: console 

    VehicleProject/
    |-- src/
    |   |-- main/
    |       |-- java/
    |           |-- Vehicle.java
    |           |-- Car.java
    |           |-- Truck.java
    |           |-- Main.java
    |-- build/
    |-- out/
    |-- lib/
    |-- README.md


.. code-block:: java 
    :caption: Vehicle.java


    public class Vehicle {
        private String name;
        private String manufacturer;
        private double price;

        public Vehicle(String name, String manufacturer, double price) {
            this.name = name;
            this.manufacturer = manufacturer;
            this.price = price;
        }

        public String getName() {
            return name;
        }

        public String getManufacturer() {
            return manufacturer;
        }

        public double getPrice() {
            return price;
        }

        public void displayInfo() {
            System.out.println("Nama kendaraan: " + name);
            System.out.println("Nama pabrik: " + manufacturer);
            System.out.println("Harga kendaraan: " + price);
        }
    }

.. code-block:: java 
    :caption: Car.java 

    public class Car extends Vehicle {
        public Car(String name, String manufacturer, double price) {
            super(name, manufacturer, price);
        }

        @Override
        public void displayInfo() {
            super.displayInfo();
            System.out.println("Tipe kendaraan: Car");
            System.out.println("Status: Selesai");
        }
    }

.. code-block:: java 
    :caption: Truck.java 

    public class Truck extends Vehicle {
        public Truck(String name, String manufacturer, double price) {
            super(name, manufacturer, price);
        }

        @Override
        public void displayInfo() {
            super.displayInfo();
            System.out.println("Tipe kendaraan: Truck");
            System.out.println("Status: Selesai");
        }
    }

.. code-block:: java 
    :caption: Main.java 

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            System.out.println("Vehicle Generator");
            System.out.println("=================");
            System.out.println("1. Generate Truck");
            System.out.println("2. Generate Car");
            System.out.print(">> ");
            int choice = scanner.nextInt();
            scanner.nextLine();  // Consume newline

            System.out.print("Masukkan nama vehicle? ");
            String name = scanner.nextLine();

            System.out.print("Masukkan nama pabrik pembuat? ");
            String manufacturer = scanner.nextLine();

            System.out.print("Masukkan harga vehicle? ");
            double price = scanner.nextDouble();

            Vehicle vehicle;

            if (choice == 1) {
                vehicle = new Truck(name, manufacturer, price);
            } else if (choice == 2) {
                vehicle = new Car(name, manufacturer, price);
            } else {
                System.out.println("Invalid choice.");
                scanner.close();
                return;
            }

            vehicle.displayInfo();

            scanner.close();
        }
    }











