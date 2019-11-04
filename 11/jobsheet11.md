#  Array 1

## Tujuan
1.	Mahasiswa mampu memahami dan menjelaskan fungsi array satu dimensi.
2.	Mahasiswa mampu membuat program dengan menggunakan konsep array satu dimensi.


## Alat dan Bahan

1. PC atau Laptop
2. JDK
3. NetBeans IDE

## Uraian Teori
Array adalah sekumpulan tempat penyimpanan data yang bertipe sama dan memiliki index. Array dapat diibaratkan sebagai 
sekumpulan variabel yang bertipe sama dan bernama sama. Array biasanya digunakan untuk menyimpan deret angka. Kemudian 
untuk membedakan nilai/isi dari variabel tersebut, digunakan index.
Ada dua tipe array:
- Array satu dimensi
- Array multi dimensi

Pada jobsheet praktikum ini hanya akan dibahas array satu dimensi saja. Array multi dimensi akan dibahas di jobsheet 
selanjutnya.

### Array Satu Dimensi
Amati ilustrasi tentang variabel berikut ini.

<figure style="text-align: center">
          <img src="images/10-01.png" alt="Variabel"/>
          <figcaption style="text-align: center; font-weight: bold">Gambar 1 Variabel</figcaption>
      </figure>

Ilustrasi diatas adalah variabel bertipe integer yang bernama bilanganBulat dan berisi nilai 17. Satu buah variabel 
hanya dapat menyimpan satu buah nilai. Sekarang amati ilustrasi tentang array berikut ini:

<figure style="text-align: center">
          <img src="images/10-02.png" alt="Array satu dimensi"/>
          <figcaption style="text-align: center; font-weight: bold">Gambar 2 Array satu dimensi</figcaption>
      </figure>

Ilustrasi diatas adalah **array** bertipe **integer** bernama **arrayInteger** dan memiliki kapasitas 5 buah bilangan 
integer. Sebuah array dapat menyimpan lebih dari satu nilai (tergantung dari kapasitasnya). Meskipun begitu, nilai-nilai 
yang disimpan di sebuah array harus bertipe sama. Tiap elemen pada array dinomori dengan index array. **Index array** 
selalu dimulai dari 0 (nol).

### Cara Mendeklarasikan Array
Secara umum, cara mendeklarasikan array adalah sebagai berikut:
```java
tipe[] namaArray = new tipe[kapasitas];
```
- Tipe adalah tipe data dari array yang akan dibuat.
- namaArray adalah nama dari array yang akan dibuat.
- Kapasitas adalah banyaknya nilai yang dapat disimpan didalam array yang akan dibuat.

Untuk mengakses (mengisi/membaca) sebuah elemen dari array, kita hanya perlu menuliskan nama array tersebut, kemudian 
diikuti dengan index yang dituju didalam tanda kurung kotak [ ].

Contoh program berikut ini membuat array bernama bil, bertipe integer, jumlah elemen 4, kemudian mengisinya dengan 
beberapa nilai, kemudian menampilkan isi elemennya ke layar.

<figure style="text-align: left">
          <img src="images/10-03.png" alt="Array satu dimensi"/>
      </figure>
<figure style="text-align: left">
          <img src="images/10-04.png" alt="Hasil"/>
      </figure>

Ada beberapa alternatif cara untuk mendeklarasikan array.
1.	Deklarasi array tanpa mengalokasikan jumlah elemennya:

    `int[] myArray;`
    
2.	Deklarasi array dengan mengalokasikan 10 elemen:

    `int[] myArray = new int[10];`
    
3.  Mengubah jumlah elemen array dengan 50: 

    `myArray = new int[50];`
    
4.	Deklarasi array dan mengisinya secara langsung:
    ```java
    int[] myArray = {10, 20, 30, 40};
    String[] myArray2 = {"Malang", "Surabaya"};
    ```
5.	Mengetahui jumlah elemen array: 

    `myArray.length;`

### Menggunakan Perulangan Pada Array Satu Dimensi
Untuk mengakses (mengisi/membaca) nilai dari sebuah array, kita dapat menggunakan perulangan.

<figure style="text-align: left">
          <img src="images/10-05.png" alt="Mengakses array"/>
      </figure>
      Hasil
   <figure style="text-align: left">
                <img src="images/10-06.png" alt="Hasil"/>
            </figure>

Kita juga bisa menggunakan perulangan untuk menerima input dan menyimpannya kedalam array. Contoh, program yang meminta 
input sebanyak 5 bilangan kemudian menampilkan kembali 5 bilangan tersebut.

<figure style="text-align: left">
          <img src="images/10-07.png" alt="Input array"/>
      </figure>
      
   <figure style="text-align: left">
                <img src="images/10-08.png" alt="Hasil"/>
            </figure>

### Input Jumlah Elemen Array
Kita juga dapat membuat program yang meminta input berapa banyak jumlah elemen array.
Langkahnya secara umum adalah:

1. Deklarasikan array tanpa mengalokasikan jumlah elemennya.
2. Buat input yang menerima jumlah elemen array kemudian simpan di sebuah variabel.
3. Set jumlah elemen array menggunakan variabel yang diinputkan tadi.
Coba amati program berikut ini:

<figure style="text-align: left">
          <img src="images/10-09.png" alt="Input array"/>
      </figure>
      
   <figure style="text-align: left">
                <img src="images/10-10.png" alt="Hasil"/>
            </figure>

## Langkah Praktikum
Ikuti langkah-langkah praktikum berikut ini.
### Praktikum 1
1. Buat class baru dengan nama `MyArray.java`
2. Buat array bertipe integer dengan nama bil dengan kapasitas 4 elemen.

   `int[] bil = new int[4]`

3. Isi masing-masing elemen array bil tadi dengan angka 5, 12, 7, 20.
    ```java
    bil[0]=5;
    bil[1]=12;
    bil[2]=7;
    bil[3]=20;
    ```
4. Tampilkan ke layar semua isi elemennya:
    ```java
    System.out.println(bil[0]);
    System.out.println(bil[1]);
    System.out.println(bil[2]);
    System.out.println(bil[3]);
    ```
5. Cocokkan dan amati hasilnya dengan gambar berikut ini:
<figure style="text-align: left">
          <img src="images/10-11.png" alt="Output array"/>
      </figure>  
      
#### Pertanyaan
1. Dari percobaan 1 berapakah indeks array terbesar dan terkecil?
2. Jika Isi masing-masing elemen array bil diubah dengan angka 5.0, 12867, 7.5, 2000000. Apa yang terjadi? 
Mengapa bisa demikian?
3. Ubah statement pada langkah No 4 menjadi seperti berikut 
    ```java
    for(int i=0; i<4; i++){
        System.out.println(bil[i]);
    }
    ```
    Apa keluaran dari program? Mengapa bisa demikian?
    
### Praktikum 2
1. Buat file baru beri nama `ArrayInputLoop.java`
2. Import dan deklarasikan Scanner untuk keperluan input. 

    `Scanner sc = new Scanner(System.in)`

3. Buat array bertipe integer dengan nama `nilaiUAS`, dengan kapasitas 6 elemen. 

    `int nilaiUAS[] = new int[6]`

4. Menggunakan perulangan, buat input untuk mengisi elemen dari array `nilaiUAS`.
    ```java
        for(int i=0; i<6; i++){
            System.out.print("Masukan nilai UAS ke-"+i+": ");
            nilaiUAS[i]=sc.nextInt();
        }
       ```
5. Menggunakan perulangan, tampilkan semua isi elemen dari array `nilaiUAS`.
    ```java
        for(int i=0; i<6; i++){
            System.out.println("Nilai UAS ke-"+i+" adalah "+nilaiUAS[i]);
        }
       ```
6. Cocokkan dan amati hasilnya dengan gambar berikut ini:
<figure style="text-align: left">
          <img src="images/10-12.png" alt="Output array"/>
      </figure>
      
#### Pertanyaan
1. Ubah statement pada langkah No 4 menjadi seperti berikut ini :
    ```java
        for(int i=0; i<nilaiUAS.length; i++){
            System.out.print("Masukan nilai UAS ke-"+i+": ");
            nilaiUAS[i]=sc.nextInt();
        }
       ```
Jalankan program, Apakah terjadi perubahan? Mengapa demikian?
2. Apa kegunaan dari `nilaiUAS.length` ? 
3. Ubah statement pada langkah No 5 menjadi seperti berikut ini, sehingga program hanya menampilkan nilai Mahasiswa 
yang lulus saja :
    ```java
        for(int i=0; i<nilaiUAS.length; i++){
            if(nilaiUAS[i] > 70){
                System.out.println("Mahasiswa ke-"+i+" lulus");
            }   
        }
   ```
Jalankan program dan Jelaskan alur program!
4. Modifikasi program agar menampilkan semua mahasiswa, dan ditandai mana yang lulus dan tidak lulus.
<figure style="text-align: left">
          <img src="images/10-13.png" alt="Output array"/>
      </figure>
      
### Praktikum 3
Pada praktikum ini, akan dilakukan percobaan untuk menjumlahkan Array. Program akan menerima input sebanyak 10 nilai 
mahasiswa. Kemudian program akan menampilkan nilai rata-rata dari dari 10 Mahasiswa.
1. Buat class baru beri nama `rataNilai`.
2. Import dan deklarasikan `Scanner` untuk keperluan input. 

    `Scanner sc = new Scanner(System.in)`

3. Buat array nilaiMHS bertipe integer dengan kapasitas 10. Kemudian deklarisakan variable total dan rata seperti 
gambar berikut ini
    ```java
    int[] nilaiMHS = new int[10];
    int total = 0;
    double rata;
    ```
4. Menggunakan perulangan, buat input untuk mengisi array `nilaiMHS`
    ```java
        for(int i=0; i<nilaiMHS.length; i++){
            System.out.print("Masukkan nilai mahasiswa ke-"+(i+1)+": ");
            nilaiMHS[i]=sc.nextInt();
        }
       ```
5. Menggunakan perulangan untuk menghitung jumlah keseluruhan nilai.
    ```java
        for(int i=0; i<nilaiMHS.length; i++){
            total+=nilaiMHS[i];
        }
       ```
6.	Kemudian hitung nilai rata-rata dengan cara nilai total dibagi jumlah elemen dari array `nilaiMHS`
    ```java
    rata = total/nilaiMHS.length;
    System.out.println(rata);
    ```
7. Amati hasilnya
<figure style="text-align: left">
          <img src="images/10-14.png" alt="Output array"/>
      </figure>
      
#### Pertanyaan
1. Pada praktikum 4 no 6. Mengapa perhitungan rata berada diluar perulangan?
2. Modifikasi program pada praktikum 4 sehingga bisa mengeluarkan output seperti gambar berikut ini
<figure style="text-align: left">
          <img src="images/10-15.png" alt="Output array"/>
      </figure>

## Tugas
Kerjakan tugas sesuai dengan instruksi berikut ini.
1. Buatlah program yang terdapat array dengan jumlah elemen 5, buatlah input untuk mengisi elemen array tersebut, 
kemudian tampilkan isi array tersebut dengan urutan terbalik. Seperti ilustrasi gambar dibawah ini.
<figure style="text-align: center">
          <img src="images/10-16.png" alt="Output array"/>
      </figure>
      <figure style="text-align: center">
                <img src="images/10-17.png" alt="Output array"/>
            </figure>
2. Buatlah program yang menerima input jumlah elemen array, inputkan isi arraynya, kemudian tampilkan mana yang genap 
dan mana yang ganjil. Contoh hasil program:
<figure style="text-align: left">
                <img src="images/10-18.png" alt="Output array"/>
            </figure>
3. Dengan menggunakan konsep Array, Buatlah program untuk menghitung Nilai IP Semester berdasarkan Matakuliah yang 
Anda Ambil semester ini. Program meminta pengguna untuk memasukkan jumlah matakuliah yang diambil pada semester ini, 
selanjutnya program tersebut meminta pengguna untuk memasukkan nama matakuliah, bobot SKS masing-masing matakuliah, 
dan Nilai dari masing-masing matakuliah.
Contoh hasil program:
<figure style="text-align: left">
                <img src="images/10-19.png" alt="Output array"/>
            </figure>
<figure style="text-align: left">
                <img src="images/10-20.png" alt="Hasil"/>
            </figure>
            Catatan : konversi nilai yang digunakan sesuai dengan peraturan polinema
            <figure style="text-align: center">
                            <img src="images/10-21.png" alt="Output array"/>
                        </figure>
4. Buatlah program untuk menghapus elemen tertentu pada sebuah Array
5. **(ArrayMax)** Buatlah program yang menerima input jumlah elemen array, inputkan isi arraynya, kemudian tampilkan 
bilangan terbesar dari isi elemen arraynya. Contoh hasil program:

    ```xml
    Masukkan isi array: 4
     Masukkan array ke-0: 25
     Masukkan array ke-1: 10
     Masukkan array ke-2: 55
     Masukkan array ke-0: 15 
     Bilangan terbesar: 55
    ```

## Materi Pengayaan
### Pencarian Pada Array
Salah satu hal yang sering dilakukan pada operasi array adalah pencarian atau searching. Pencarian dilakukan untuk 
menemukan nilai tertentu pada elemen didalam array. Ada banyak algoritma searching, namun yang paling mudah adalah 
Linear Search.

Misalkan pada sebuah array, kita ingin mencari dimana posisi index dari sebuah array. Pada Linear Search, kita 
membandingkan “key” atau angka yang ingin kita cari, dengan tiap elemen yang ada didalam array. Amati gambar berikut:
<figure style="text-align: center">
                <img src="images/10-22.png" alt="Linier search"/>
                <figcaption style="text-align: center; font-weight: bold">Linier search</figcaption>
            </figure>
Pada gambar diatas, key atau angka yang ingin kita cari adalah 3. Menggunakan looping kita bandingkan masing-masing 
elemen dari array. Dan ternyata angka 3 berada di index ke 5. Maka setelah ketemu, looping akan berhenti, dan hasil 
akhir dari program adalah 5 (index dimana angka 3 berada). Amati contoh program berikut:
<figure style="text-align: left">
                <img src="images/10-23.png" alt="Output array"/>
            </figure>
<figure style="text-align: left">
                <img src="images/10-24.png" alt="Hasil"/>
                <figcaption style="text-align: left; font-weight: bold">Hasilnya</figcaption>
            </figure>
            
### Sorting
Sorting adalah proses mengurutkan elemen array dari yang terkecil ke besar (ascending) atau sebaliknya (descending). 
Ada banyak algoritma untuk pengurutan, namun yang paling mudah adalah Bubble Sort.

Didalam Bubble Sort, dilakukan looping dari elemen pertama sampai elemen terakhir dari array. Kemudian tiap elemen 
dibandingkan dengan elemen berikutnya. Jika elemen tersebut lebih besar dari elemen berikutnya, maka akan ditukar. 
Amati ilustrasi berikut ini:
<figure style="text-align: center">
                <img src="images/10-25.png" alt="Bubble sort"/>
                <figcaption style="text-align: center; font-weight: bold">Bubble sort</figcaption>
            </figure>
Berikut adalah contoh program Bubble Sort:
<figure style="text-align: left">
                <img src="images/10-26.png" alt="Output array"/>
            </figure>
<figure style="text-align: left">
                <img src="images/10-27.png" alt="Hasil"/>
                <figcaption style="text-align: left; font-weight: bold">Hasilnya</figcaption>
            </figure>

## Tugas Pengayaan
Kerjakan tugas sesuai dengan instruksi berikut ini.
1. Buatlah program yang menerima input jumlah array, isi array, key yang ingin dicari. Cetak ke layar index posisi 
elemen dari key yang ingin dicari. Contoh hasil program:
    ```xml
    Masukkan jumlah elemen array: 4
    Array ke 0: 5
    Array ke 1: 12
    Array ke 2: 25
    Array ke 3: 10
    Masukkan key yang ingin dicari: 12
    Key ada di posisi index ke: 1
    ```
2. Buatlah program yang menerima input jumlah array, isi array, kemudian urutkan array tersebut, kemudian tampilkan ke 
layar hasil pengurutannya. Contoh hasil program:
    ```xml
    Masukkan jumlah elemen array: 4
    Array ke 0: 5
    Array ke 1: 12
    Array ke 2: 
    ```
