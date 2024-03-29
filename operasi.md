---
title: Operasi
layout: default
author: "@deovaliandro"
---


## Operator Aritmatika

|           Hasil           | Operator |
| :-----------------------: | :------: |
|        Additional         |    +     |
|        Subtraction        |    -     |
|      Multiplication       |    *     |
|         Division          |    /     |
|          Modulus          |    %     |
|         Increment         |    ++    |
|         Decrement         |    --    |
|   Additional assignment   |    +=    |
|  Subtraction assignment   |    -=    |
| Multiplication assignment |    *=    |
|    Division assignment    |    /=    |
|    Modulus asignement     |    %=    |

Operator ini hanya bisa digunakan pada tipe data angka, tidak bisa digunakan
pada data `boolean`, tetapi dapat digunakan pada tipe data `char`, karena `char`
pada dasarnya adalah `int` di dalama Java.

Contoh:

```java
public class OperatorAritmatika {
 
    public static void main(String[] args) {
        System.out.println("Operasi Penjumlahan");
        int hasilPenjumlahan = 5 + 1;
        System.out.println("Hasil 5 + 1 = " + hasilPenjumlahan);
        System.out.println();

        System.out.println("Operasi Pengurangan");
        int hasilPengurangan = 4 - 1;
        System.out.println("Hasil 4 - 1 = " + hasilPengurangan);
        System.out.println();

        System.out.println("Operasi Pengalian");
        int hasilPengalian = 5 * 5;
        System.out.println("Hasil 5 * 5 = " + hasilPengalian);
        System.out.println();

        System.out.println("Operasi Pembagian");
        int hasilPembagian = 20 / 2;
        System.out.println("Hasil 20 / 2 = " + hasilPembagian);
        System.out.println();

        System.out.println("Operasi Habis bagi");
        int hasilSisa = 8 % 2;
        System.out.println("Hasil 8 % 2 = " + hasilSisa);
        System.out.println();

        int hasilSisaLain = 9 % 2;
        System.out.println("Hasil 9 % 2 = " + hasilSisaLain);
    }
}
```

## Operator pembanding

|          Hasil           | Operator |
| :----------------------: | :------: |
|         Equal to         |    ==    |
|       Not equal to       |    !=    |
|       Greater than       |    >     |
|        Less than         |    <     |
| Greater than or equal to |    >=    |
|  Less than or equal to   |    <=    |

Hasil operator ini adalah nilai boolean, bisa berupa true atau false.

Integer, floating-point numbers, characters, dan Booleans bisa digunakan pada
operator equal to dan not equal to, tetapi boolean tidak bisa digunakan pada
operator lain (operator order) hanya integer, floating-point numbers dan
characters.

Contoh:

```java
int i = 12, b = 3;

if (i < b) {
    System.out.println("True");
} else if (i == b) {
    System.out.println("Equal");
}
```

## Operator Logika

| Hasil | Operator |
| :---: | :------: |
|  AND  |    &&    |
|  OR   |   \|\|   |
|  XOR  |    ^     |
|  NOT  |    !     |

Digunakan logika digunakan pada tipe data boolean untuk menyelesaikan
permasalahan yang membutuhkan nilai-nilai logika.

Contoh penggunaan:

```java
boolean a = true;
int b = 12;

if (a == true && b < 20) {
    System.out.println("True");
} else {
    System.out.println("False");
}
```