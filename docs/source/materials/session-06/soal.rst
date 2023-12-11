Latihan Soal
================
Buatlah sebuah program yang menghitung rata-rata dari sejumlah bilangan yang dimasukkan oleh pengguna. Program harus dapat mengabaikan angka negatif, dan jika pengguna memasukkan angka 0 sebagai input, program harus menampilkan pesan kesalahan.

**Answer**

.. code:: java

    import java.util.Scanner;

    public class AverageCalculator {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
            int count = 0;
            double total = 0;

            while (true) {
                System.out.print("Masukkan sebuah bilangan (0 untuk berhenti): ");
                int number = scanner.nextInt();

                if (number == 0) {
                    System.out.println("Input selesai.");
                    break;
                }

                try {
                    if (number < 0) {
                        System.out.println("Angka negatif diabaikan.");
                        continue;
                    }

                    total += number;
                    count++;
                } catch (Exception e) {
                    System.out.println("Terjadi kesalahan: " + e.getMessage());
                }
            }

            scanner.close();

            if (count > 0) {
                double average = total / count;
                System.out.println("Rata-rata dari bilangan yang dimasukkan adalah: " + average);
            } else {
                System.out.println("Tidak ada bilangan yang dimasukkan untuk dihitung rata-ratanya.");
            }
        }
    }

.. note:: 

    Program di atas meminta pengguna untuk memasukkan sejumlah bilangan. Jika pengguna memasukkan 0, input akan berhenti. Program mengabaikan angka negatif dan menghitung rata-rata dari bilangan positif yang dimasukkan. Jika terjadi kesalahan dalam input, program menangani exception dan menampilkan pesan kesalahan yang sesuai.
