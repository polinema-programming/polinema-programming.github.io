# Bahasa Pemrograman

## Tujuan

- Mahasiswa mengenal konsep program dan bahasa pemrograman
- Mahasiswa mampu melakukan instalasi tools pemrograman
- Mahasiswa memahami struktur dasar bahasa pemrograman
- Mahasiswa mampu melakukan proses compile dan debug

## Praktikum

### Percobaan 1: Melakukan Instalasi Java Development Kit/JDK

1. Unduh JDK pada alamat tautan berikut: [Download JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html)

2. Klik dua kali pada file instalasi yang sudah diunduh kemudian ikuti instruksi proses instalasinya.

3. Langkah selanjutnya adalah pengaturan **PATH** (langkah ini khusus untuk
   sistem operasi Windows), sehingga perintah java dapat dikenali.

4. Cara melakukan pengaturan **PATH** dengan membuka **Control Panel** ->
   **System** -> **Advanced System Setting** -> **Environment Variable**.
   Kemudian cari variabel **PATH**.

   > **Catatan**: jika variabel **PATH** tidak ditemukan, silahkan anda
   > menambahkan variabel tersebut.

5. Langkah selanjutnya adalah mengisi variabel **PATH**, jika variabel **PATH**
   sudah ada isinya jangan menghapus nilai yang sudah ada tetapi tambahkan
   `C:\Program Files\Java\jdk\bin` (sebagai pemisah antar nilai gunakan karakter
   `;`, khusus untuk sistem operasi di bawah Windows 10)

   > **Catatan**: Lokasi nilai JDK yang ditambahkan sesuaikan dengan direktori dimana
   > program Java terinstall, pada contoh langkah di atas JDK terinstall pada
   > `C:\Program Files\Java\jdk\bin`

6. Buka Command Prompt (`Win + R`, kemudian ketik `cmd`), selanjutnya ketikan
   perintah `javac`. Jika perintah tersebut dikenali maka lingkungan sistem
   operasi Windows telah mendukung program java. Tetapi jika belum dikenali
   lakukan pengecekan pada pengaturan **PATH** (kemungkinan ada kesalahan ketika
   memasukkan lokasi direktori bin pada variable **PATH**)

### Pertanyaan

1. Jelaskan apa kegunaan memasukkan lokasi direktori bin dari Java ke dalam
   variabel **PATH**!
2. Jelaskan kegunaan perintah `javac` ketika masuk di command prompt!
