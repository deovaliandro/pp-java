---
title: Tipe Data
layout: default
author: "@deovaliandro"
---


Java merupakan bahasa pemrograman yang strongly typed, maka kita tidak bisa
mengabaikan tipe data. Kita harus tahu data seperti apa yang disimpan ke dalam
variabel. Selain itu, Java juga bersifat statically typed, yang artinya setiap
variabel harus dideklarasikan terlebih dahulu sebelum digunakan.

## Tipe Data Primitif

Tipe data primitif adalah tipe data standar yang tidak diturunkan dari objek
manapun. Tipe data primitif telah ditentukan dengan kata kuncinya masing-masing.
Terdapat 8 (delapan) tipe data primitif yang Java dukung, antara lain:

### Integer

1. byte
    
    byte adalah tipe data yang menampung angka 8 bit dengan range -127 - 128
    (2^8). Tipe data byte memiliki nilai default 0.

    ```java
    byte n = 12;
    ```

2. short
    
    short adalah tipe data yang menampung angka 16 bit dengan range -32.768 -
    32.767 (2^16). Tipe data byte memiliki nilai default 0.

    ```java
    short n = 1200;
    ```

3. int

    int adalah tipe data yang menampung angka 32 bit dengan range -2,147,483,648
    - 2,147,483,647 (2^32). Tipe data byte memiliki nilai default 0.

    ```java
    int n = 289000;
    ```

4. long

    long adalah tipe data yang lebih panjang dari int, yaitu
    -9,223,372,036,854,775,808 sampai 9,223,372,036,854,775,807 (2^64). Tipe
    data long memiliki nilai default 0L.

    ```java
    long n = 122334445;
    ```

5. float

    Tipe data float adalah tipe data untuk bilangan desimal seperti 3.14, 2.1
    atay bilangan desimal lainnya. Tipe data ini bisa nemapung nilai 2^32. Nilai
    default-nya 0.0f.

    ```java
    float n = 3.14f;
    ```
    penulisannya ditambahkan huruf `f` di belakang angkanya, ini untuk menandai
    bahwa bilangan tersebut adalah `float` bukan `double`.

6. double

    Tipe data double mirip dengan tipe data float, kecuali data yang bisa ditamp
    ungnya lebih besar yaitu 2^64. Nilai default-nya 0.0d.

    ```java
    double n = 144.2;
    ```
7. char

    Tipe data char adala tipe data yang hanya bisa menampung satu huruf saja.
    Nilai yang bisa ditampung adalah 0 to 65,535.
    Misalnya:

    ```java
    char c = 'a';
    ```

    Nilai yang diberikan disimpan dalam satu tanda kutip.

8. Boolean

Boolean adalah tipe data yang bisa menampung dua nilai, yaitu benar atau salah.
Tipe data ini akan banyak digunakan kemudian. Nilai default-nya false.

```java
boolean b = true;
```

## Tipe Data Reference

Tipe data reference merupakan sebuah tipe data yang merujuk ke sebuah objek atau
instance dari sebuah class. Salah satu tipe data yang termasuk ke dalam tipe
data reference adalah `string`. Tipe data string menunjuk ke instance dari class
`java.lang.String`.

### String

String adalah tipe data yang menampung karakter. String bisa menampung lebih
dari satu karakter, misalnya kata, kalimat atau paragraf.

```java
String name = "Deo";
```

perhatikan, penulisan `String` menggunakan kapital di awal kata, kemudian isinya
disimpan di dalam tanda kutip dua ("...").

## Deklarasi variabel

Sebuah data dapat disimpan ke dalam variabel. Format penulisannya sebagai
berikut:

```java
type namaVariabel;
```
### Deklarasi

Deklarasi adalah pembuatan sebuah variabel, namun belum di isi dengan suatu
nilai. Contoh:

```java
int n;
boolean b;
char c;
```

### Inisiasi

Inisiasi adalah pengisian sebuah variabel dengan data. Contoh:

```java
n = 12;
b = false;
c = 'A';
```

Deklarasi sekaligus inisiasi juga dapat dilakukan, misalnya dengan:

```java
float f = 21.0f;
boolean b = false;
```

### Inisiasi dinamis

Dua atau lebih data dapat di isi secara bersamaan dalam satu baris dengan syarat
tipe datanya sama. Contoh:

```java
int a = 12, b = 13, c = 14;
```
atau bisa juga jika semua data memiliki nilai yang sama, misalnya:

```java
int x = y = z = 100;
```

## Mengubah tipe ke tipe data lain

Suatu tipe data dapat di ubah ke tipe data lain, misalnya dari byte ke int.
Syaratnya adalah:

-   kedua tipe data kompatible, misalnya antara byte dengan int, int dengan
    float, tetapi char dan boolean tidak memiliki kompatible.
-   tipe data yang dituju memiliki ruang penyimpanan yang lebih besar, misalnya
    byte memiliki ruang penyimpanan 2^8, akan diubah ke int yang memiliki
    penyimpanan 2^32. Tetapi jika dari tipe data int ke byte, maka jika nilai
    yang akan diubah lebih besar dari 2^8, maka akan menyebabkan nilai akhir
    adalah hasil modulo dari ukuran byte.

Cara mengubah tipe data dapat dicontohkan sebagai berikut:

```java
int n = 12;
byte b = (int) n;
```

Bagaimana jika int ke float, silahkan coba sendiri.

### Konversi otomatis

Misalnya terdapat a, b, c yang merupakan byte, kemudian dilakukan operasi sebagai
berikut:

```java
byte a = 40;
byte b = 50;
byte c = 100;
int d = a * b / c;
```

maka nilai a, b dan c akan otomatis diubah menjadi int.

Aturan promosi ini adalah:

1. byte, short, char akan di ubah ke int,
2. jika operasinya adalah long, maka akan diubah ke long,
3. float akan di ubah ke double,
4. jika operasi melibatkan double, maka otomatis akan diubah semua ke double.