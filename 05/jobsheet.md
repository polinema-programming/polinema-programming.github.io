# Sintaks Pemilihan 1

## Tujuan

Mahasiswa mampu menyelesaikan permasalahan/studi kasus menggunakan sintaks
pemilihan 1 dan mengimplementasikannya dalam bahasa pemrograman Java.

## Alat dan Bahan

1. PC/Laptop
2. Netbeans IDE

## Uraian Teori

Pada kehidupan sehari-hari kita selalu mengambil keputusan dengan
mempertimbangkan berbagai hal/kondisi-kondisi. Sintaks pemilihan adalah
statement pemilihan yang digunakan untuk mengatur kapan suatu perintah akan
dijalankan. Dengan statement ini kita bisa mengatur kapan suatu perintah akan
dijalankan, yaitu ketika telah dipenuhinya suatu syarat tertentu. Misalnya:

> Jika **nilai lebih dari 70** maka **Diterima**

Pernyataan di atas mengandung sebab akibat. Bila dilihat, keterangan **nilai
lebih dari 70** adalah merupakan suatu syarat, sedangkan **DITERIMA** ini akan
dilakukan apabila syaratnya terpenuhi atau **nilai lebih dari 70**. Dalam dunia
logika, istilah **terpenuhinya syarat** dapat dikatakan **syarat tersebut
bernilai benar atau TRUE**. Selanjutnya pernyataan **jika...maka...** dapat
diadopsi dalam *programming*. Untuk pernyataan tersebut dalam programming, maka
dapat digunakan statement sintaks pemilihan. Pada pembahasan di materi sintaks
pemilihan 1 ini akan dipelajari tiga macam sintaks pemilihan yaitu `if`,
`if else`, `if else if else` dan `switch case`.

## Sintaks Pemilihan `if`

Bentuk umum:

```java
if (kondisi)  {
  pernyataan;
  pernyataan;
  ...
}
```

Bentuk flowchart:

{% flowchart %}
start=>start: Mulai
end=>end: Selesai
op1=>operation: operasi...
cond=>condition: Ya atau Tidak?
op2=>operation: operasi...

start->op1->cond
cond(yes, right)->op2->end
cond(no)->end
{% endflowchart %}

> - Apabila kondisi bernilai benar, maka pernyataan akan dilaksanakan.
> - Apabila kondisi bernilai salah, maka pernyataan tidak akan dilaksanakan.

Pada sintaks pemilihan 1 ini, kita akan menggunakan operator hubungan
(*relational operator*). Berikut ini operator hubungan dalam bahasa pemrograman
Java:

| Simbol Operator | Keterangan                               |
| ---             | ---                                      |
| `==`            | Sama dengan (*Equal to*)                 |
| `>`             | Sama dengan (*Greater than*)             |
| `<`             | Sama dengan (*Less than*)                |
| `>=`            | Sama dengan (*Greater than or Equal to*) |
| `<=`            | Sama dengan (*Less than or Equal to*)    |
| `!=`            | Tidak sama dengan (*Not Equal to*)       |

Implementasi atau penggunaan operator hubungan pada sintaks pemilihan adalah
sebagai berikut:

![Operator Hubungan If](./images/operator-hubungan-if.png)

Contoh program:

```java
import java.util.Scanner;

public class Contoh {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    int angka;

    System.out.print("Masukkan angka: ");
    angka = input.nextInt();

    if (angka > 70) {
      System.out.println("Selamat anda dinyatakan diterima");
    }

  }
}
```

Ketika program di atas dijalankan kemudian dimasukkan angka 80 maka akan keluar
tampilan **Selamat anda dinyatakan diterima**. Hal ini disebabkan karena
terdapat sebuah kondisi yang menyatakan bahwa jika nilai lebih dari 70 (`angka > 70`) maka akan tampil **Selamat anda dinyatakan diterima**, sedangkan jika dimasukkan angka 70 atau kurang dari 70 maka tidak akan terdapat tampilan apapun.

## Sintaks Pemilihan `if else`

Bentuk umum:

```java
if (kondisi) {
  pernyataan1;
} else {
  pernyataan2;
}
```

Bentuk flowchart:

{% flowchart %}
start=>start: Mulai
end=>end: Selesai
cond=>condition: Ya atau Tidak?
op1=>operation: pernyataan 1
op2=>operation: pernyataan 2

start->cond
cond(yes, left)->op1->end
cond(no, right)->op2->end
{% endflowchart %}

Struktur ini minimal memiliki 2 pernyataan. Jika kondisi yang diperiksa bernilai
benar atau terpenuhi maka pernyataan pertama yang akan dilaksanakan dan jika
kondisi yang diperiksa bernilai salah maka pernyataan kedua yang akan
dilaksanakan.

Contoh program:

```java
import java.util.Scanner;

public class Contoh {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    int angka;

    System.out.print("Masukkan angka: ");
    angka = input.nextInt();

    if (angka > 70) {
      System.out.println("Selamat anda dinyatakan diterima");
    } else {
      System.out.println("Silahkan coba tes lagi tahun depan");
    }

  }
}
```

Pada contoh program `if else` di atas ditambahkan kode program.

```java
else {
  System.out.println("Silahkan coba tes lagi tahun depan");
}
```

Sehingga ketika angka yang dimasukkan nilainya 70 atau kurang dari 70 maka akan
muncul tampilan **Silahkan coba tes lagi tahun depan**.

## Sintaks Pemilihan `if else if else`

Bentuk Umum:

```java
if (kondisi1) {
  pernyataan-1;
} else if (kondisi2) {
  pernyataan-2;
} else if (kondisix) {
  pernyataan-x;
} else {
  pernyataan-else;
}
```

Bentuk Flowchart:

{% flowchart %}
start=>start: Mulai
end=>end: Selesai
cond1=>condition: Ya atau Tidak?
cond2=>condition: Ya atau Tidak?
condx=>condition: Ya atau Tidak?
op1=>operation: pernyataan 1
op2=>operation: pernyataan 2
opx=>operation: pernyataan x
op=>operation: pernyataan else

start->cond1
cond1(no, right)->cond2
cond2(no, right)->condx
condx(no, right)->op->end

cond1(yes)->op1->end
cond2(yes)->op2->end
condx(yes)->opx->end
{% endflowchart %}

Pada bentuk `if else if else` di atas, pernyataan 1 akan dijalankan apabila
`kondisi1` bernilai benar. Jika `kondisi1` bernilai salah, maka akan dicek
`kondisi2`. Jika `kondisi2` benar maka akan dijalankan pernyataan2, begitu
seterusnya. Dan apabila tidak ada satupun syarat yang terpenuhi, barulah
pernyataan-else akan dikerjakan.

Contoh program:

```java
import java.util.Scanner;

public class Contoh {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    int bayar;

    System.out.print("Masukkan total belanja anda: ");
    bayar = input.nextInt();

    if (bayar >= 2000000) {
      System.out.println("Selamat anda mendapatkan hadiah kompor gas");
    } else if (bayar >= 1000000) {
      System.out.println("Selamat anda mendapatkan hadiah teflon");
    } else if (bayar >= 500000) {
      System.out.println("Selamat anda mendapatkan hadiah piring");
    } else {
      System.out.println("Maaf anda belum beruntung, tingkatkan belanja anda!");
    }

  }
}
```

## Sintaks pemilihan `switch case`

Sintaks pemilihan ini digunakan untuk penyelesaian kondisi dengan kemungkinan
yang terjadi cukup banyak. Struktur ini akan melaksanakan salah satu dari
beberapa pernyataan `case` tergantung nilai kondisi yang ada di dalam `switch`.
Selanjutnya proses diteruskan hingga ditemukan pernyataan `break`. Jika tidak
ada nilai pada case yang sesuai dengan nilai kondisi, maka proses akan
diteruskan kepada pernyataan yang ada di bawah `default`. Bentuk `switch case`
pada umumnya digunakan untuk menggantikan pernyataan `if else if else` yang
berdasarkan nilai konstanta.

Bentuk umum:

```java
switch (kondisi) {
case konstanta-1:
  pernyataan-1;
  break;
case konstanta-2:
  pernyataan-2;
  break;
  ...
  ...
case konstanta-x:
  pernyataan-x;
  break;
default:
  pernyataan;
}
```

Contoh program:

```java
import java.util.Scanner;

public class Contoh {
  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);

    int angka;

    System.out.print("Masukkan kode kelas anda: ");
    angka = input.nextInt();

    switch(angka) {
      case 1:
        System.out.println("Kelas 1");
        break;
      case 2:
        System.out.println("Kelas 2");
        break;
      case 3:
        System.out.println("Kelas 3");
        break;
      case 4:
        System.out.println("Kelas 4");
        break;
      default:
        System.out.println("Kode yang anda masukkan salah");
    }

  }
}
```

Pada contoh program `switch case` di atas jika dimasukkan angka `1` maka
outputnya **Kelas 1** dan seterusnya sampai angka `4`. Jika inputan selain angka
`1` s/d `4` maka outputnya adalah **Kode yang anda masukkan salah**.

## Langkah Praktikum

Ikuti langkah-langkah praktikum berikut ini.

### Praktikum 1

1. Perhatikan flowchart di bawah ini!

   <figure style="text-align: center">
        <img src="images/05-19.png" alt="Flowchart If"/>
    </figure>

   Flowchart diatas digunakan untuk menentukan bilangan ganjil/genap,
   selanjutnya kita akan membuat programnya berdasarkan flowchart di atas!

2.	Buka Netbeans yang sudah anda install
3.	Buat project baru dengan nama “Pemilihan1” dengan cara `File -> New Project
    -> Java Application ->Next ->Pemilihan1 ->Finish`

   <figure style="text-align: center">
        <img src="images/05-20.png" alt="Flowchart If"/>
        <figcaption style="text-align: center; font-weight: bold">New Project</figcaption>
    </figure>

   <figure style="text-align: center">
        <img src="images/05-21.png" alt="Flowchart If"/>
        <figcaption style="text-align: center; font-weight: bold">Java Application</figcaption>
    </figure>

   <figure style="text-align: center">
        <img src="images/05-22.png" alt="Flowchart If"/>
        <figcaption style="text-align: center; font-weight: bold">Project Name</figcaption>
    </figure>

4.	Maka akan terdapat 1 buat project dengan nama Pemilihan 1 dan didalamnya
    terdapat 1 file dengan nama `Pemilihan1.java`

   <figure style="text-align: center">
        <img src="images/05-23.png" alt="Flowchart If"/>
    </figure>

5.	Tambahkan import library Scanner.
6.	Deklarasikan Scanner:

   <figure style="text-align: center">
        <img src="images/05-24.png" alt="Flowchart If"/>
    </figure>

7.	Buatlah variabel bertipe int dengan nama bil

   <figure style="text-align: center">
        <img src="images/05-25.png" alt="Flowchart If"/>
    </figure>

8.	Tambahkan kode berikut ini untuk menerima inputan dari keyboard:

   <figure style="text-align: center">
        <img src="images/05-26.png" alt="Flowchart If"/>
    </figure>

9.	Buatlah struktur kondisi untuk mengecek apakah bilangan tersebut merupakan bilangan genap atau ganjil

   <figure style="text-align: center">
        <img src="images/05-27.png" alt="Flowchart If"/>
    </figure>

10.	Jalankan program, maka outputnya adalah sebagai berikut:

   <figure style="text-align: center">
        <img src="images/05-28.png" alt="Flowchart If"/>
    </figure>

#### Pertanyaan!

1.	Modifikasi program diatas dibagian struktur pemilihannya sehingga menjadi sebagai berikut:

   <figure style="text-align: center">
        <img src="images/05-29.png" alt="Flowchart If"/>
    </figure>

2.	Jalankan dan amatilah hasilnya!
3.	Jelaskan mengapa output program yang dimodifikasi sama dengan output program sebelum dimodifikasi!

### Praktikum 2

1.	Buat file baru beri nama “Percobaan2.java” di project  “Pemilihan1”.

   <figure style="text-align: center">
        <img src="images/05-30.png" alt="Flowchart If"/>
    </figure>

   <figure style="text-align: center">
        <img src="images/05-31.png" alt="Flowchart If"/>
    </figure>

2.	Tambahakan library `Scanner`.
3.	Buatlah deklarasi `Scanner`.
4.	Buat variabel nilai bertipe int.

   <figure style="text-align: center">
        <img src="images/05-32.png" alt="Flowchart If"/>
    </figure>

5.	Tuliskan perintah untuk memasukkan inputan.

   <figure style="text-align: center">
        <img src="images/05-33.png" alt="Flowchart If"/>
    </figure>

6.	Tambahkan kode program kondisi dibawah ini

   <figure style="text-align: center">
        <img src="images/05-34.png" alt="Flowchart If"/>
    </figure>

7.	Jalankan program. Amati apa yang terjadi!

### Pertanyaan

1.	Jelaskan fungsi kode program berikut:
   ```java
    nilai += 10;
    nilai += 10;
   ```
2.	Modifikasilah program diatas dimana inputannya yang awalnya hanya satu
    kemudian diganti 2 inputan (misal : nilai1 dan nilai2), lakukan perhitungan
    rata-rata kedua nilai tersebut jika nilainya lebih dari sama dengan 100 maka
    dikurangi 5, sedangkan jika nilai rata-rata tersebut kurang dari 100 maka
    akan langsung dicetak!

### Praktikum 3

1.	Buat file baru beri nama “Percobaan3.java” di project  “Pemilihan1”.
2.	Tambahakan library Scanner.
3.	Buatlah deklarasi Scanner.
4.	Buat variabel umur bertipe int.

   ```java
    int umur;
   ```

5.	Tuliskan perintah untuk memasukkan inputan.

   ```java
    System.out.println("Masukkan umur Anda: ");
    umur = input.nextInt();
   ```

6.	Tambahkan kode program kondisi dibawah ini

   ```java
    if(umur > 60) {
       System.out.println("Lansia");
    } else if(umur > 45) {
       System.out.println("Tua");
    } else if(umur > 17) {
       System.out.println("Dewasa");
    } else if(umur > 5) {
       System.out.println("Anak-anak");
    } else {
       System.out.println("Balita");
    }
   ```

7.	Jalankan program. Amati apa yang terjadi!

#### Pertanyaan

1.	Berapa jumlah kondisi yang ada pada program di percobaan 3? Jelaskan!
2.	Modifikasi program diatas sehingga jika umur yang dimasukkan 0 tahun atau
    kurang dari 0 akan tampil output “Maaf umur yang anda masukkan salah”!

### Praktikum 4
1.	Buat file baru beri nama “Percobaan4.java” di project  “Pemilihan1”.
2.	Tambahakan library Scanner.
3.	Buatlah deklarasi Scanner.
4.	Buat variabel-variabel berikut:

   ```java
   double angka1, angka2, hasil;
   char operator;
   ```

5.	Tuliskan perintah untuk memasukkan inputan.
   ```java
   System.out.println("Masukkan angka pertama: ");
   angka1 = sc.nextDouble();
   System.out.println("Masukkan angka kedua: ");
   angka2 = sc.nextDouble();
   System.out.println("Masukkan operator (+ - * /): ");
   operator = sc.next().chartAt(0);
   ```

6.	Tambahkan kode program kondisi dibawah ini

  ```java
  switch(operator){
    case '+':
      hasil = angka1 + angka2;
      System.out.println(angka1 + " + " + angka2 + "=" + hasil);
      break;
    case '-':
      hasil = angka1 - angka2;
      System.out.println(angka1 + " - " + angka2 + "=" + hasil);
      break;
    case '*':
      hasil = angka1 * angka2;
      System.out.println(angka1 + " * " + angka2 + "=" + hasil);
      break;
    case '/':
      hasil = angka1 / angka2;
      System.out.println(angka1 + " / " + angka2 + "=" + hasil);
      break;
  }
  ```

7.	Jalankan program. Amati apa yang terjadi!

#### Pertanyaan

1.	Jelaskan fungsi dari break dan default pada percobaan 4 diatas!
2.	Jelaskan fungsi perintah kode program dibawah ini pada percobaan 4!
   ```java
       operator = sc.next().chartAt(0);
   ```

#### Tugas

1. Buatlah program untuk menginputkan dua buah bilangan bulat, kemudian
   mencetak salah satu bilangan yang nilainya terbesar.
2. Perhatikan flowchart berikut ini:

   <figure style="text-align: center">
        <img src="images/05-37.png" alt="Flowchart If"/>
    </figure>

  Buatlah program sesuai dengan flowchart diatas!

3. Anda ingin membangun sebuah Restoran. Restoran anda setidaknya mempunyai 3
   menu yang dapat dipilih oleh pelanggan. Pelanggan dapat memilih menu dan
   jumlah pesanan yang diinginkan. Untuk memudahkan pelayanan restoran, buatlah program
   yang dapat menampilkan menu yang disediakan serta menghitung total harga yang
   dibayarkan (ditambah dengan pajak restoran 10%) dan uang kembalian!

   Ilustrasi menu restoran, dapat dilihat di bawah:

   ```
   Menu Restoran Besok Gratis
   1. Ayam Geprek  - Rp. 100.000
   2. Ayam Goreng  - Rp.  80.000
   3. Bebek Geprek - Rp. 150.000
   Masukkan pilihan anda (1 - 3):
   ```

4.	Sebuah toko menyediakan fasilitas member untuk memberikan diskon kepada
    pelanggannya. Terdapat 3 kategori member yaitu: Silver, Gold, dan Platinum.
    Setiap total belanja yang sesuai ketentuan katagori member akan mendapatkan
    diskon spesial sesuai dengan ketentuan berikut:

| Total belanja         | Jenis potongan member | Potongan  |
| ----------------------| --------------------- | --------  |
| >Rp. 200.000,00       | Silver                | 2%        |
| >Rp. 500.000,00       | Gold                  | 5%        |
| >Rp. 1.000.000,00     | Platinum              | 10%       |

   **Output:**

   <figure style="text-align: left">
        <img src="images/05-38.png" alt="Flowchart If"/>
    </figure>

   <figure style="text-align: left">
        <img src="images/05-39.png" alt="Flowchart If"/>
    </figure>

   <figure style="text-align: left">
        <img src="images/05-40.png" alt="Flowchart If"/>
   </figure>

   <figure style="text-align: left">
        <img src="images/05-41.png" alt="Flowchart If"/>
    </figure>
