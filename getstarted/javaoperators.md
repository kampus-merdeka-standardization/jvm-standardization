## 3. Java Operators
Opertator digunanakan untuk melakukan operasi pada variabel dan nilai.
- Operasi Matematika
    - `+` Penjumlahan
    - `-` Pengurangan
    - `*` Perkalian
    - `/` Pembagian
    - `%` Sisa Pembagian
    - `++` Increment, seperti `+1`
    - `--` Decrement, seperti `-1`
- Operasi Perbandingan
    - `>` lebih dari
    - `<` kurang dari
    - `>=` lebih dari sama dengan
    - `<=` kurang dari sama dengan 
    - `==` sama dengan
    - `!=` tidak sama dengan
- Operasi Boolean
    - `&&` dan
    - `||` atau
    - `!` kebalikan 
### Operasi Matematika
```java
int a = 100;
int b = 10;
System.out.println(a + b); // Output: 110
System.out.println(a - b); // Output: 90
System.out.println(a * b); // Output: 1000
System.out.println(a / b); // Output: 10
System.out.println(a % b); // Output: 0
```
---
### Increment Decrement
Pada contoh ini, akan dilakukan contoh increment, karena perbedaannya kalau increment menaikkan 1 nilai menggunakan operator `++`, sedangkan decrement menurunkan 1 nilai menggunakan operator `--`.
Misal ada variabel `a`, Pertanyaannya apa perbedaan `a++` dengan `++a`?
- `a++`
    ```java
    int a = 100;
    System.out.println(a++); // Output: 100
    System.out.println(a); // Output: 101
    ```
    Kode di atas, akan bekerja seperti:
    ```java
    int a = 100;
    System.out.println(a); // Output: 100
    a = a + 1;
    System.out.println(a); // Output: 101
    ```
    ---
- `++a`
    ```java
    int a = 100;
    System.out.println(++a); // Output: 101
    System.out.println(a); // Output: 101
    ```
    Kode di atas, akan bekerja seperti:
    ```java
    int a = 100;
    a = a + 1;
    System.out.println(a); // Output: 101
    System.out.println(a); // Output: 101
    ```
---
### Operasi Perbandingan
Operasi Perbandingan berfungsi untuk membandingkan dua buah data, dan akan menghasilkan nilai `boolean` yaitu `true` atau `false`
```java
System.out.println(1 > 2); // Output: false
System.out.println(1 < 2); // Output: true
System.out.println(1 >= 2); // Output: false
System.out.println(1 >= 1); // Output: true
System.out.println(1 <= 2); // Output: true
System.out.println(1 <= 1); // Output: true
System.out.println(1 == 2); // Output: false
System.out.println(1 != 2); // Output: true
```
---

### Operasi Boolean 
Operasi Boolean adalah operasi yang melibatkan dua nilai boolean, dan akan menghasilkan nilai `boolean` yaitu `true` atau `false`
- Operasi `&&` akan bernilai true jika kedua nilai bernilai true, misal:
    ```java
    boolean example1 = true && true;
    boolean example2 = true && false;
    boolean example3 = false && true;
    boolean example4 = false && false;

    System.out.println(example1); // true
    System.out.println(example2); // false
    System.out.println(example3); // false
    System.out.println(example4); // false
    ```
- Operasi `||` akan bernilai true jika salah satu nilainya true, misal:
    ```java
    boolean example1 = true || true;
    boolean example2 = true || false;
    boolean example3 = false || true;
    boolean example4 = false || false;

    System.out.println(example1); // true
    System.out.println(example2); // true
    System.out.println(example3); // true
    System.out.println(example4); // false
    ```
- Operasi `!` akan membalikkan nilai dari nilai aslinya, misal:
    ```java
    boolean falseValue = !true; // false
    boolean trueValue = !false; // true

    System.out.println(falseValue);
    System.out.println(trueValue);
    ```