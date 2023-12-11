Switch Case
---------------
digunakan untuk memilih dari sejumlah opsi berdasarkan nilai dari ekspresi tertentu.

**Syntax Switch-case**

.. code:: console

    switch (ekspresi) {
        case nilai_1:
            // Kode yang akan dieksekusi jika ekspresi sama dengan nilai_1
            break;

        case nilai_2:
            // Kode yang akan dieksekusi jika ekspresi sama dengan nilai_2
            break;

        // Tambahkan lebih banyak kasus jika diperlukan

        default:
            // Kode yang akan dieksekusi jika ekspresi tidak cocok dengan kasus manapun
    }

**Code**

.. code:: java

    int hari = 3;

    switch (hari) {
        case 1:
            System.out.println("Minggu");
            break;

        case 2:
            System.out.println("Senin");
            break;

        case 3:
            System.out.println("Selasa");
            break;

        case 4:
            System.out.println("Rabu");
            break;

        case 5:
            System.out.println("Kamis");
            break;

        case 6:
            System.out.println("Jumat");
            break;

        case 7:
            System.out.println("Sabtu");
            break;

        default:
            System.out.println("Hari tidak valid");
    }

**Output :**

.. code:: console

    Selasa
