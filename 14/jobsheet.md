# Fungsi 1

## Tujuan
1. Mahasiswa mampu memahami penggunaan fungsi *static* pada Java dengan
   parameter dan mengembalikan nilai.
2. Mahasiswa mampu membuat program dengan menggunakan fungsi *static* dan
   mengeksekusi fungsi tersebut.

## Alat dan Bahan

1. PC atau Laptop
2. JDK
3. IDE

## Uraian Teori
### Pengertian Fungsi

Dalam pemrograman terdapat istilah fungsi, prosedur, dan method, yang ketiganya
pada dasarnya adalah sama, di mana kita dapat menyebut ketiganya sebagai fungsi.
Prosedur adalah sebutan untuk fungsi yang tidak mengembalikan nilai. Fungsi ini
biasanya ditandai dengan kata kunci void. Fungsi adalah sebutan untuk fungsi
yang mengembalikan nilai. Method adalah fungsi yang berada di dalam sebuah
Class. Sebutan ini, biasanya digunakan pada OOP.

Ada 2 jenis fungsi di Java, yaitu fungsi static dan non-static. Fungsi static
adalah fungsi yang dapat dieksekusi langsung tanpa harus melakukan instansiasi
objek. Sedangkan funsi non-static adalah fungsi yang harus dieksekusi dari objek
yang sudah diinstansiasi, di mana ini berkaitan dengan OOP. Sehingga pada modul
praktikum kali ini kita hanya membahas tentang fungsi static di Java. Cara
mendeklarasikan fungsi static di Java adalah dengan menambahkan keyword static.

### Sintaks Fungsi di Java

Fungsi harus dibuat atau ditulis di dalam class. Sintaks dasar penulisan fungsi
adalah sebagai berikut:

```java
static TypeDataKembalian namaFungsi(){
  // statement
}
```

Kata kunci `static`, artinya kita akan membuat fungsi static.
`TypeDataKembalian` adalah tipe data dari nilai yang dikembalikan (output)
setelah fungsi dieksekusi. Jika fungsi tersebut tidak mengembalikan output, maka
`TypeDataKembalian` adalah `void`. Sedangkan, `namaFungsi()` adalah nama fungsi
yang kita buat, ditulis dengan cara camel case. Contoh:

```java
static void beriSalam(){
  System.out.println("Halo! Selamat Pagi");
}
```
### Cara Menjalankan/Eksekusi Fungsi

Setelah kita membuat fungsi, selanjutnya kita bisa mengeksekusi fungsinya.
Fungsi dapat dipanggil dari fungsi main atau dari fungsi yang lainnya. Contoh
pemanggilan fungsi dalam fungsi main:

```java
public static void main(String[] args){
  beriSalam();
}
```

> Kode selengkapnya, silahkan dicoba pada bagian Praktikum.

### Fungsi dengan Parameter

Parameter adalah variabel yang menampung nilai untuk diproses di dalam fungsi.
Parameter berperan sebagai input untuk fungsi. Struktur dasarnya seperti berikut
ini:


```java
static TypeDataKembalian namaFungsi(TipeData namaParameter, TipeData namaParameterLain){
  // statement
}
```

Parameter ditulis di antara parenthesis `(...)` setelah nama fungsi. Bila
terdapat lebih dari satu parameter, maka dipisah dengan tanda koma `,` dan
masing-masing parameter harus dideskripsikan tipe datanya.

Misalkan, dibuat parameter bernama ucapan dengan tipe String. Sehingga kita bisa
menggunakan variabel ucapan di dalam fungsi berikut ini:

```java
static void beriUcapan(String ucapan){
  System.out.println(ucapan);
}
```

Cara eksekusi fungsinya adalah dengan memberikan nilai yang akan diinputkan
sebagai parameter, bisa berupa variabel atau langsung nilainya. Contohnya:

```java
String halo = "Hallo!";
beriUcapan(halo);
beriUcapan("Selamat datang di pemrograman Java");
```

### Fungsi yang Mengembalikan Nilai

Pada kasus tertentu dibutuhkan sebuah fungsi yang dapat mengembalikan nilai
output sehingga bisa diolah pada proses berikutnya. Pengembalian nilai pada
fungsi menggunakan keyword return.

```java
static TypeDataKembalian namaFungsi(TipeData namaParameter){
  // statement
  return variabelOutput;
}

```

Contoh:

```java
static int luasPersegi(int sisi){
  int luas = sisi * sisi;
  return luas;
}
```

Pada contoh tersebut, dibuat sebuah parameter bernama sisi. Kemudian fungsi akan
mengembalikan output dengan tipe int (integer) dari variabel luas. Cara
pemanggilan fungsi tersebut adalah seperti berikut:

```java
System.out.println("Luas Persegi dengan sisi 5 = " + luasPersegi(5));
int luasan = luasPersegi(6);
```

###	Langkah Praktikum
#### Praktikum 1

1.	Buat class baru dengan nama `Greeting`.

  ```java
  public class Greeting {

  }
  ```

2.	Buat fungsi `beriSalam()` di dalam class tersebut.

  ```java
  public class Greeting {

      static void beriSalam() {
          System.out.println("Halo! Selamat Pagi");
      }

  }
  ```

3.	Buat fungsi main di dalam class tersebut, dan eksekusi fungsi `beriSalam()`
    dari dalam fungsi `main()`.

  ```java
  public class Greeting {

      static void beriSalam() {
          System.out.println("Halo! Selamat Pagi");
      }

      public static void main(String[] args) {
          beriSalam();
      }

  }
  ```

#### Praktikum 2

1.	Buat fungsi `beriUcapan` dengan sebuah parameter bertipe `String` di dalam class
    `Greeting`.

  ```java
  public class Greeting {

      static void beriSalam() {
          System.out.println("Halo! Selamat Pagi");
      }

      static void beriUcapan(String ucapan) {
          System.out.println(ucapan);
      }

      public static void main(String[] args) {
          beriSalam();
      }

  }
  ```

2.  Eksekusi fungsi beriUcapan dari dalam fungsi main.

  ```java
  public class Greeting {

      static void beriSalam() {
          System.out.println("Halo! Selamat Pagi");
      }

      static void beriUcapan(String ucapan) {
          System.out.println(ucapan);
      }

      public static void main(String[] args) {
          beriSalam();
          String salam = "Selamat datang di pemrograman Java";
          beriUcapan(salam);
      }

  }
  ```

### Praktikum 3

1.	Buat class baru dengan nama `Persegi`.

  ```java
  public class Persegi {

  }
  ```

2.	Buat fungsi `luasPersegi` di dalam class tersebut yang mengembalikan nilai
    luas (int) dan parameter masukan sisi (int).

  ```java
  public class Persegi {

      static int luasPersegi(int sisi) {
          int luas = sisi * sisi;
          return luas;
      }

  }
  ```

3.	Buat fungsi main di dalam class tersebut, dan eksekusi fungsi `luasPersegi`
    dari dalam fungsi main.

  ```java
  public class Persegi {

      static int luasPersegi(int sisi) {
          int luas = sisi * sisi;
          return luas;
      }

      public static void main(String[] args) {
          int luasan = luasPersegi(5);
          System.out.println("Luas Persegi dengan sisi 5 = " + luasan);
      }

  }
  ```
#### Praktikum 4

1.	Buat class baru dengan nama `Hitung`.
  ```java
  public class Hitung {

  }
  ```

2.	Buatlah fungsi `kali` di dalam class tersebut yang mengembalikan nilai
    `hasil` (int) dan parameter masukan `angka1` dan `angka2` (int).

  ```java
  static int kali(int angka1, int angka2)  {
      int hasil = (angka1 + 10) % (angka2 + 19);
      return hasil;
  }
  ```

3.	Buatlah fungsi `kurang` di dalam class tersebut yang mengembalikan nilai
    `hasil` (int) dan parameter masukan `angka1` dan `angka2` (int) dan
    memanggil fungsi `kali`.

  ```java
  static int kurang(int angka1, int angka2) {
      angka1 = angka1 + 7;
      angka2 = angka2 + 4;
      int hasil = kali(angka1, angka2);
      return hasil;
  }
  ```

4.	Buat fungsi main di dalam class tersebut, dan eksekusi fungsi `kurang` dari
    dalam fungsi main.

  ```java
  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      System.out.print("Masukkan nilai 1: ");
      int nilai1 = input.nextInt();
      System.out.print("Masukkan nilai 2: ");
      int nilai2 = input.nextInt();
      int hasil = kurang(nilai1, nilai2);
      System.out.println("Hasil akhir adalah " + hasil);
  }
  ```

#### Praktikum 5

1.	Buat class baru dengan nama `Varargs`.

  ```java
  public class Varargs {

  }
  ```

2.	Buatlah fungsi Tampil (bertipe void) di dalam class tersebut dengan
    menggunakan dua jenis tipe data parameter yaitu string dan int

  ```java
  static void tampil(String pesan, int... angka) {
      System.out.println("String: " + pesan);
      System.out.println("Jumlah argumen/parameter: " + angka.length);

      for (int i = 0; i < angka.length; i++) {
          System.out.print(angka[i] + " ");
      }
      System.out.println();
  }
  ```

3.	Buat fungsi main di dalam class tersebut, dan eksekusi fungsi Tampil dari
    dalam fungsi main.

  ```java
  public static void main(String[] args) {
    tampil("Daspro 2019", 100, 200);
    tampil("Teknologi Informasi", 1, 2, 3, 4, 5);
    tampil("Polinema");
    int[] angka = { 1, 2, 3, 4 };
    tampil("Malang", angka);
  }
  ```

#### Praktikum 6

1.	Buat class baru dengan nama `Balok`.

  ```java
  public class Balok {

  }
  ```

2.	Buatlah program untuk menghitung luas permukaan dan volume balok tanpa
    menggunakan fungsi.

  ```java
  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      System.out.print("Masukkan panjang: ");
      int p = input.nextInt();
      System.out.print("Masukkan panjang: ");
      int l = input.nextInt();
      System.out.print("Masukkan panjang: ");
      int t = input.nextInt();

      int luasPermukaan = 2 * ((p * l) + (p * t) + (l * t));
      System.out.println("Luas permukaan Balok adalah: " + luasPermukaan);

      int volume = p * l * t;
      System.out.println("Volume Balok adalah: " + volume);
  }
  ```

3.	Program menghitung luas persegi dan volume balok di atas jika dibuatkan
    fungsi maka terdapat 3 fungsi yaitu hitungLuasPermukaan, hitungVolume dan fungsi
    main, seperti dibawah ini:

  ```java
  static int hitungLuasPermukaan(int p, int l, int t) {
      int hasil = 2 * ((p * l) + (p * t) + (l * t));
      return hasil;
  }
  ```

  ```java
  static int volume(int p, int l, int t) {
      int hasil = p * l * t;
      return hasil;
  }
  ```

  ```java
  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      System.out.print("Masukkan panjang: ");
      int p = input.nextInt();
      System.out.print("Masukkan panjang: ");
      int l = input.nextInt();
      System.out.print("Masukkan panjang: ");
      int t = input.nextInt();

      System.out.println("Luas permukaan Balok adalah: " + hitungLuasPermukaan(p, l, t));
      System.out.println("Volume Balok adalah: " + hitungVolume(p, l, t));
  }
  ```

4.	Jelaskan jalannya program menghitung luas persegi dan volume balok diatas
    yang menggunakan fungsi!

#### Pertanyaan!

1.	Berdasarkan praktikum 2 dan 3, jelaskan kapan suatu fungsi membutuhkan nilai
    kembalian (return)!
2.	Pada praktikum 4 tambahkan satu fungsi yang digunakan untuk mengecek inputan
    nilai 1 dan nilai 2 harus minimal 0, kemudian panggil fungsi tersebut di
    fungsi main!
3.	Jelaskan mengapa penulisan parameter di praktikum 5 di tulis dengan int...
    angka!
4.	Apakah output dari program dibawah ini kemudian jelaskan alur jalannya
    program tersebut!

  ```java
  public class Programku {
      public static void tampilHinggaKeI(int i) {
          for (int j = 1; j <= i; j++) {
            System.out.print(j);
          }
      }

      public static int jumlah(int bil1, int bil2) {
        return bil1 + bil2;
      }

      public static void tampilJumlah(int bil1, int bil2) {
        tampilHinggaKeI(jumlah(bil1, bil2));
      }

      public static void main(String[] args) {
        int temp = jumlah(1, 1);
        tampilJumlah(temp, 5);
      }
  }
  ```

### Tugas

1.	Buatlah sebuah static method yang bernama Max3(int bil1, int bil2, int bil3)
    yang menerima 3 buah parameter bilangan integer dan mengembalikan sebuah
    bilangan integer yang merupakan nilai maksimum diantara ketiga bilangan
    tersebut.

    > Catatan: Anda boleh membuat static method lain selain Max3.
    > Setelah itu, gunakanlah static method Max3 tersebut di method utama kalian
    > (penggunaannya bebas).

2.	Buatlah sebuah class `Lingkaran` yang di dalamnya terdapat fungsi untuk
    menghitung keliling lingkaran dan luas lingkaran.

3.	Buatlah program untuk mengisi array `nilai` sampai penuh dengan tipe data
    berupa int (nilai ujian 10 mahasiswa), dimana proses penginputan dan
    pengisiannya kedalam array dilakukan dalam sebuah fungsi. Selanjutnya
    buatlah lainya yaitu untuk menghitung nilai rata-rata array tersebut  (nilai
    rata-rata ujian mahasiswa). Dan cetak nilai rata-rata tersebut dimana
    intsruksi mencetaknya berada di fungsi main.

4.	Berdasarkan soal no 3, tambahkan sebuah fungsi lain untuk mencari nilai
    terbesar dan terkecil dari isi array tersebut. Dan cetak nilai terbesar dan
    terkecil tersebut, dimana intruksi mencetaknya berada pada fungsi main.

5.	Terdapat array A satu dimensi dengan ilustrasi seperti gambar dibawah ini
    yang dibuat didalam fungsi main (belum ada isinya)

| 0      | 1      | 2      | 3      | 4      | 5      | 6      | 7      | 8      | 9      | 10     |
| ---    | ---    | ---    | ---    | ---    | ---    | ---    | ---    | ---    | ---    | ---    |
| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |

  Buatlah sebuah fungsi untuk mengisi array tersebut, sehingga isinya menjadi
  seperti berikut:

| 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1   |     | 2   |     | 3   |     | 4   |     | 5   |     | 6   |





