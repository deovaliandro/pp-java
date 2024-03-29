---
title: Method
layout: default
author: "@deovaliandro"
---


Method adalah suatu fungsi.

Method melaksanakan suatu tugas tertentu (menurut prinsip SOLID).

Method pada Java memiliki bentuk umum seperti berikut ini:

```java
return-type methodName(parameter-list) {
    //body of method
}
```

dimana:

1. `return-type` adalah jenis nilai yang akan dikembalikan oleh method
tersebut.
2. methodName adalah nama method
3. parameter-list adalah daftar nilai yang dikirim ke method tersebut.

Contohnya:

sebuah method yang berfungsi untuk menghitung hasil perkalian dua buah bilangan.

```java
public int multipication(int a, int b) {
    return a*b;
}
```

`int` adalah tipe data yang akan dikembalikan oleh method tersebut, yaitu hasil
perkalian a dengan b. `multipication` adalah nama method tersebut, `int a` dan
`int b` adalah 2 jenis parameter yang diterima oleh method tersebut, parameter
ini akan berguna sebagai nilai yang akan diolah oleh method tersebut.

`public` adalah access modifier, akan di diskusikan di
![materi PBO](https://github.com/deovaliandro/pbo-java).

Sedangkan untuk memanggil method tersebut, kita dapat memanggil dengan
menggunakan namanya, misalnya kita akan memanggil method yang telah kita buat
diatas:

```java
int hasil = multipication(12, 14);
```

12 dan 14 disini adalah argumen yang dikirim.

> untuk mengembalikan multiple values, dapat menggunakan return array

Sebuah method juga dapat mengembalikan object. Misalnya:

```java

class Demo{
    int a;
    double b;
    int c;

    Demo(int m, double d, int a) {
        a = m;
        b = d;
        c = a;
    }
}

class MethodDemo4{ 
    static Demo get(int x, int y) {
        return new Demo(x * y, (double)x / y, (x + y)); 
    }

    public static void main(String[] args) {
        Demo ans = get(25, 5); 
        System.out.println("Multiplication = " + ans.a); 
        System.out.println("Division = " + ans.b); 
        System.out.println("Addition = " + ans.c); 
    } 
}
  
```
Sumber: ![https://www.studytonight.com](https://www.studytonight.com/java/methods-in-java.php)

> Java menggunakan call-by-value bukan call-by-reference

Note:
1. Tambahkan call-by-value vs call-by-reference