*Return*
================
`Return` digunakan untuk mengembalikan nilai dari suatu metode dan sekaligus mengakhiri eksekusi metode tersebut. Ketika suatu metode memiliki tipe pengembalian (return type) selain void, pernyataan return digunakan untuk mengirimkan nilai tersebut kembali ke tempat di mana metode tersebut dipanggil.


.. code:: java

        public class Main {
            
            public int calculateSum(int a, int b) {
                int sum = a + b;
                return sum; // Mengembalikan nilai sum
            }

            public void printMessage() {
                System.out.println("Hello!");
                return; // Mengakhiri eksekusi metode printMessage tanpa mengembalikan nilai
            }
            
            public Main() {
                //panggil  method
                System.out.println(calculateSum(2,3));
                printMessage();
            }
            
            public static void main(String[] args) {
                
                new Main();
            
            }
    }


.. code:: console

    5
    Hello!

