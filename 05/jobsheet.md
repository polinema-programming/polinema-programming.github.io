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
