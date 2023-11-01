# C. Get Started

Di Java, setiap aplikasi dimulai dengan nama kelas, dan nama tersebut harus sesuai dengan nama file.

## 1. Hello World
Tradisi programmer dalam mempelajari bahasa pemrograman adalah dengan membuat program yang menampilkan "Hello World". Untuk itu mari kita lakukan :
```java
public class HelloWorld {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```

### Kompilasi Program
- Untuk menjalankan kode program di atas, kita harus menyimpannya kedalam file dengan nama yang sama dengan nama `public class`-nya dengan ekstensi file `.java`. Contoh pada kasus ini adalah `HelloWorld.java`

- Untuk proses kompilasi-nya, kita bisa membuka `terminal` lalu arahkan ke direktori dimana kita menyimpan file-nya, dan ketikkan : 
    ```sh
    javac FileName.java
    ```
- Karena nama file yang kita buat sebelumnya adalah `HelloWorld.java`, maka kita bisa ketik `javac HelloWorld.java`
- Nantinya compiler akan mengkompilasi program tersebut dan membuat file dengan ekstensi `.class`
- Untuk menjalankan hasil kompilasi tersebut kita bisa mengetikkan pada terminal :
    ```sh
    java ClassName
    ``` 
- Karena nama `.class` kita adalah `HelloWorld`, maka kita bisa ketik `java HelloWorld`.
- Selamat, program berhasil berjalan

### Menjalankan Program
- Sejak Java versi 11, kita bisa menjalankan aplikasi Java tanpa harus melakukan langkah kompilasi. Kita cukup mengetikkan perintah :
    ```sh
    java FileName.java
    ```
- Pada kasus sebelumnya, kita bisa menjalankan program hanya dengan langsung menuliskan perintah `java HelloWorld.java`, maka program berhasil berjalan