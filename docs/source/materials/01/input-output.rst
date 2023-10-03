Input-Ouput
============
**Output** pada java kita bisa menggunakan perintah ``System.out.println();`` untuk mencetak hasil code. Contoh :

.. code-block:: java

    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello, World!");
            //output print (tanpa enter )
            System.out.print("Hello");
        }
    }

Output:

.. code-block:: console

    Hello, World!
    Hello

**Input** pada java bisa menggunakan ``Scanner`` dari ``java.utils.scanner``

.. code-block:: java

    import java.util.Scanner;

    public class Main {
        public static void main(String[] args) {
            //Scanner
            Scanner scan = new Scanner(System.in);
            //Variabel
            int a ;

            System.out.print("Input Angka : ");
            a = scan.nextInt();
            scan.nextLine();
            System.out.printf("Angka yang di Input: %d", a);
        }

    }

Output:

.. code-block:: console

    Input Angka : 5
    Angka yang di Input: 5

Dari kode diatas dapat dilihat bahwa saat kita ingin memakai ``Scanner``, kita wajib **mengimport** Scanner dari ``java.util.scanner`` terlebih dahulu.
Hal ini dapat dilakukan dengan secara otomatis dengan menekan tombol ``ctrl + space`` pada keyboard.

.. note:: 
    biasanya saat ingin menginput selain string kita wajib menggunakan     ``nextLine()`` untuk menangkap sisa enter



Special Characters
------------------
.. note:: 
    - Comment ``//`` : adalah kata-kata / kalimat yang tidak ingin di compile 
    - Automatic ``ctrl + space`` : untuk menampilkan saran otomatis dari IDE 
    - Brackects ``{}``: untuk memulai dan mengakhiri scope
    - Paranthesis ``()``: digunakan pada methods
    - ``""``: untuk string 
    - 

.. .. list-table:: Special Characters
..     :width: 25 25 50 
..     :header-rows: 1
..     * - Heading row 1, column1
..       - Heading row 1, column 2
..       - Heading rom 3, column 3
..     * - Row1, Column 1






