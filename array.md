---
title: Array
layout: default
author: "@deovaliandro"
---


Array adalah kelompok data dengan tipe yang sama.

Dalam Java, pada saat mendeklarasikan sebuah array panjang array harus
ditentukan, dan tidak dapat diubah setelahnya (nilai fix). Setiap item dalam
sebuah array disebut element, dan setiap element dapat diakses dengan indexnya.
Index array selalu mulai dari 0 sampai n-1, dengan n adalah panjang array.

## Deklarasi
Sebelum digunakan, Array harus dideklarasikan terlebih dahulu dengan
menentukan tipe data dan panjangnya.

Bentuk umum:

```java
tipeData[] namaArray = new tipeData[n];

//atau

tipeData namaArray[] = new tipeData[n];
```

Contoh:

```java
int[] arr = new int[20];
```

## Mengisi

Ada beberapa cara untuk menginisialisasi array, diantaranya adalah:

```java
tipeData[] namaArray = { element1, element2, element3, element4 };

//atau

tipeData[] namaArray = new int[4];
namaArray[0] = element1;
namaArray[1] = element2;
namaArray[2] = element3;
namaArray[3] = element4;
```

Contoh:

```java
int[] arr = { 132, 11, 134, 33};

atau

int[] arr = new int[4];
arr[0] = 132;
arr[1] = 11;
arr[2] = 134;
arr[3] = 33;
```

## Mengakses

Untuk mengakses element tertentu pada array cukup dengan menyebutkan nama array
disertai dengan kurung siku dan index element yang ingin diakses.

Bentuk umum:

```java
namaArray[index];
```

Contoh:

```java
int[] arr = { 132, 11, 134, 33};
System.out.println(arr[0]);
```

## Array multi-dimensi

Array multidimensi dapat diilustrasikan sebagai array dalam array. Artinya
setiap element pada array tersebut adalah sebuah array juga (Array dua dimensi).
Hal ini juga berlaku untuk Array NxN dimensi. 

Contoh:

```java
int[][] arr = new int[4][5];
```

Kemudian untuk mengisinya dengan:

```java
int[][] arr = {
    {1, 1, 1, 1, 1},
    {1, 1, 1, 1, 1},
    {1, 1, 1, 1, 1},
    {1, 1, 1, 1, 1}
};
```

Untuk mengaksesnya, digunakan cara yang sama dengan array 1-dimensi, misalnya:

```java
System.out.println(arr[0][1]);
```