#  Array Multidimensi

## Tujuan
1.	Mahasiswa mampu memahami konsep array 2 dimensi
2.	Mahasiswa mampu membuat program dengan menggunakan konsep array multidimensi.


## Alat dan Bahan

1. PC atau Laptop
2. JDK
3. NetBeans IDE

## Uraian Teori

### Array Dua Dimensi
Array yang telah kita pelajari sebelumnya adalah satu dimensi, yang hanya terdiri dari satu baris elemen. Biasanya untuk
menyajikan sebuah data dalam bentuk tabel, dalam tabel tersebut disajikan dalam bentuk **baris** dan **kolom**. Hal ini yang
menjadi ciri khas dari sebuah array 2 dimensi. 

Sebagai contoh 
1. Buku tamu yang terdapat di perpustakaan untuk melakukan pencatatan kunjungan pengunjung, dimana dalam buku tamu
tersebut terdapat informasi nim, nama, tanggal kunjungan, dan tanda tangan.
2. Rating film yang dilakukan oleh penonton atau viewer. Masing-masing baris atau record diisi atau dirating oleh
penonton, sedangkan pada bagian kolomnya adalah daftar judul film yang akan dilakukan rating. Visualisasi dapat dilihat
pada tabel di bawah ini

|     | judul_0 | judul_1 | judul_2 |
| --- | ---     | ---     | ---     |
| 0   | 4       | 4       | 3       |
| 1   | 2       | 4       | 3       |
| 2   | 4       | 4       | 3       |
| 3   | 1       | 2       | 2       |
| 4   | 4       | 4       | 4       |

Tabel di atas menggambarkan bahwa setiap view akan melakukan rating terhadap 3 judul film, misalkan pada baris pertama
melakukan rating pada `judul_0=4, judul_1=4, dan judul_2=3`.

> Jadi Array 2 dimensi adalah sebuah array yang penomoran indeksnya menggunakan 2 angka yaitu satu untuk baris dan satu
>lagi untuk kolom, atau sebenarnya array 2 dimensi adalah kumpulan dari array 1 dimensi.

#### Cara Mendeklarasikan Array 2 dimensi
Untuk dapat mendeklarasikan array 2 dimensi mirip dengan 1 dimensi, perbedaanya adalah jumlah kurung siku `[]` atau
subskrip. Pada array 2 dimensi berarti menggunakan 2 kurung siku `[]`, pada java deklarasinya seperti di bawah ini

```java
data_type[][] array_name = new data_type[x][y];
x = jumlah baris
Y = jumlah kolom
Contoh
int[][] arr = new int[10][20];
```

Selain contoh di atas, deklarasi yang lain juga dapat dilakukan seperti di bawah ini
1. `tipe_data[][] nama_variabel`
2. `tipe_data [][]nama_variabel`
3. `tipe_data nama_variabel[][]`   
4. `tipe_data []nama_variabel[]`

Akan tetapi, yang sering kita jumpai atau sering digunakan adalah pada no.1 dan no.3, ketika menggunakan Java adalah 
seperti di bawah ini
```java
int[][] ratings;
int [][]ratings;
int ratings[][];
int []ratings[];
```

#### Inisialisasi Array 2 Dimensi
Untuk memberikan nilai awal pada array 2 dimensi menggunakan operator assigment `=`, ketika melakukan inisialisasi array
2 dimensi kolom pada setiap baris boleh berbeda seperti dicontohkan di bawah ini

```java
int a[][]={
    {1,2,3,4},
    {5,6,7,8},
    {7,8,9,6}
}
int b[][]={
    {1},
    {5,6,7,8},
    {7,8,9}
}
```
Array yang pertama pada `variabel a` kolomnya semua sama antar baris, sedangkan jika kita lihat pada `array b` kolomnya
berbeda. Dalam array 2 multidimensi hal tersebut diperbolehkan. Ketika divisualisasikan ke dalam sebuah tabel seperti di
bawah ini

Visualisasi untuk `array a`

   |     | 0 | 1 | 2 | 3 |
   | --- |---|---|---|---|
   | 0   | 1[0,0] | 2[0,1] | 3[0,2] | 4[0,3] |    
   | 1   | 5[1,0] | 6[1,1] | 7[1,2] | 8[1,3] |
   | 2   | 7[2,0] | 8[2,1] | 9[2,2] | 6[2,3] |
   
Visualisasi untuk `array b`
   
   |     | 0 | 1 | 2 | 3 |
   | --- |---|---|---|---|
   | 0   | 1[0,0] |  |  |  |    
   | 1   | 5[1,0] | 6[1,1] | 7[1,2] | 8[1,3] |
   | 2   | 7[2,0] | 8[2,1] | 9[2,2] |  |

#### Ukuran Baris dan Kolom Array 2 Dimensi
Seriap array baik array 1 dimensi ataupun array 2 dimensi memiliki ukuran, jika pada array 2 dimensi berarti ukuran pada
baris atau kolom. Untuk mengetahui ukuran atau length, bisa menggunakan attribut `length` pada array. Cara penggunaannya
adalah sebagai berikut
```java
int[][] a = new int[3][4];
```
Ketika dipanggil `a.length` maka hasilnya adalah 3(jumlah baris), sedangkan ketika dipanggil `a[0].length` hasilnya 
4(jumlah kolom)

>Ketika menggunakan attribut length tentunya akan sangat menguntungkan, baik ketika akan menginputkan element atau
>menampilkan element menggunakan looping atau perulangan pada saat perubahan jumlah baris atau kolom. Kita tidak perlu
> mengubah kode yang ada di dalam looping untuk ukuran baris dan kolomnya.

### Array Tiga Dimensi

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
