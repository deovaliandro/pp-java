---
title: File IO
layout: default
author: "@deovaliandro"
---


Input dan output pada file digunakan untuk mengolah file tersebut.

Untuk membaca suatu file, kita menggunakan class `FileReader` dan untuk menulis
pada suatu file, kita menggunakan class `FileWriter`.

Contoh kasusnya, menyalin suatu isi file ke file lain. Disini kita akan
menggunakan `FileReader` untuk membaca isi file tersebut, lalu kita akan menulis
dengan menggunakan `FileWriter` kepada file lainnya.

```java
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
 
public class Main {
    public static void main(String[] args) {
        try {
            FileReader fileReader = new FileReader("source.txt");
            FileWriter fileWriter = new FileWriter("destination.txt");

            int i;

            while( ( i = fileReader.read()) != -1 ){
                fileWriter.write(i);
            }
            
            fileReader.close();
            fileWriter.close();
        } catch (FileNotFoundException e) {
            System.out.println("File tidak ada! " + e);
        } catch (IOException e) {
            System.out.println("Terdapat masalah ada I/O" + e);
        }
    }
}
```

Hasilnya:

![file-io](/img/Screenshot_20210921_204112.png)