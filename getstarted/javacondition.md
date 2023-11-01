## 4. Java Condition
Java Condition memungkinkan untuk mengeksekusi kode program tertentu jika memenuhi kondisi yang diinginkan.

### Expression, Statement, & Block
Sebelum lebih jauh dalam mengetahui Java Condition, kita perlu tahu perbedaan antara Expression, Statement, & Block
- Expression

    Expression adalah bagian dari kode yang menghasilkan sebuah nilai. Contoh dari ekspresi adalah perhitungan matematika seperti 3 + 5, pemanggilan metode seperti `Math.max(4, 7)`, atau penggunaan variabel seperti x * 2.
- Statement 
    
    Statement adalah unit dasar dari instruksi dalam program Java. Ini adalah tindakan atau pernyataan yang dijalankan oleh program. Sebuah statement dapat berupa sebuah ekspresi yang diakhiri dengan tanda titik koma (;) atau pernyataan yang lebih kompleks seperti pernyataan kondisional if, perulangan for, atau pernyataan switch. Contoh pernyataan adalah:
- Block

    Block adalah kumpulan _statement_ yang dikelompokkan bersama dalam sepasang kurung kurawal {}. Ini digunakan untuk mengelompokkan _statement-statement_ bersama-sama sehingga mereka dapat dianggap sebagai satu unit. Block biasanya digunakan dalam pernyataan kondisional, perulangan, atau dalam metode. Contoh block adalah:

Sederhananya, kita dapat melihat gambaran berikut 
```java
public static void main(String[] args) {
    // block
    int a = 10;
    System.out.println(a = 100);
                    // ^------^expression
    // ^-----------------------^statement
}
```


### If Else Statement
If Else Statement terdiri dari sebuah ekspresi `boolean` dan diikuti satu atau lebih statement. Pada bagian [Java Operators](#3-java-operators-) kita mengetahui bahwa ada operator yang menghasilkan nilai `boolean` seperti [operasi perbandingan](#operasi-perbandingan) dan [operasi boolean](#operasi-boolean). Kita bisa menggunakan operasi-operasi tersebut pada bagian kondisi.

berikut contoh penggunaaan if else statement
```java
int nilai = 8;

if (nilai == 10) {
    System.out.println("lulus dengan nilai sempurna");
} else if (nilai > 5) {
    System.out.println("lulus");
} else if (nilai > 2 && nilai <= 5) {
    System.out.println("hampir lulus");
} else {
    System.out.println("tidak lulus. nilai anda: " + nilai);
}
```
penjelasan kode di atas:<br>
dilakukan pengecekkan `nilai` dengan urutan seperti berikut :
- 1. **jika** `nilai` sama dengan 10, maka akan menghasilkan output `lulus dengan nilai sempurna`
- 2. **tapi jika** `nilai` lebih besar dari 5, maka akan menghasilkan output `lulus`
- 3. **tapi jika** `nilai` lebih besar dari 2 `dan` kurang dari sama dengan 5, maka akan menghasilkan output `hampir lulus`
- 4. jika tidak ada yang memenuhi seluruh kemungkinan kondisi, maka block `else` akan tereksekusi. Dan akan menghasilkan output `tidak lulus. nilai anda: 1`, dengan permisalan _value_ dari variable nilai adalah 1

### Switch Statement
Pada kasus dimana kita hanya butuh menggunakan kondisi sederhana di `if statement` seperti hanya menggunakan perbadingan `==`, maka kita bisa menggunakan `switch statement`.<br/>
Switch Statement digunakan ketika kita memiliki satu nilai ekspresi yang akan dibandingkan dengan sejumlah nilai yang mungkin.<br/>
Perbedaan `if statement` dengan `switch statement`:
- if statement
    ```java
    char nilai = 'A';

    if (nilai == 'A') {
        System.out.println("lulus dengan nilai sempurna");
    } else if (nilai == 'B' || nilai == 'C') {
        System.out.println("lulus dengan nilai cukup");
    } else if (nilai == 'D') {
        System.out.println("tidak lulus");
    } else {
        System.out.println("tidak terdeteksi");
        System.out.println("coba lagi");
    }
    ```
- switch statement
    ```java
    char nilai = 'A';
    switch (nilai) {
        case 'A':
            System.out.println("lulus dengan nilai sempurna");
            break;

        case 'B':
        case 'C':
            System.out.println("lulus dengan nilai cukup");
            break;

        case 'D':
            System.out.println("tidak lulus");
            break;

        default:
            System.out.println("tidak terdeteksi");
            System.out.println("coba lagi");
            break;
    }
    ```
- switch lambda<br/>
    Sejak versi java 14, penulisan `switch` statement bisa lebih sederhana tanpa menggunakan `break;`, seperti
    ```java
    char nilai = 'A';
    switch (nilai) {
        case 'A' -> System.out.println("lulus dengan nilai sempurna");
        case 'B', 'C' -> System.out.println("lulus dengan nilai cukup");
        case 'D' -> System.out.println("tidak lulus");
        default -> {
            System.out.println("tidak terdeteksi");
            System.out.println("coba lagi");
        }
    }
    ```
    Sejak versi java 14 juga, diperkenalkan keyword `yield` yang dapat mengembalikan nilai pada switch statement.
    - berikut contoh sebelum ada `yield`:
        ```java
        char nilai = 'A';

        String pesanKelulusan;

        switch (nilai) {
            case 'A' -> pesanKelulusan = "lulus dengan nilai sempurna";
            case 'B', 'C' -> pesanKelulusan = "lulus dengan nilai cukup";
            case 'D' -> pesanKelulusan = "tidak lulus";
            default -> pesanKelulusan = "coba lagi";
        }

        System.out.println(pesanKelulusan); // lulus dengan nilai sempurna
        ```    
    - berikut contoh menggukan `yield`:
        ```java
        char nilai = 'A';

        String pesanKelulusan = switch (nilai) {
            case 'A':
                yield "lulus dengan nilai sempurna";
            case 'B': 
            case 'C': 
                yield "lulus dengan nilai cukup";
            case 'D':
                yield "tidak lulus";
            default: 
                yield "coba lagi";
        };

        System.out.println(pesanKelulusan); // lulus dengan nilai sempurna
        ```
- Ternary Operator(`? :`)<br/>
Ternary Operator adalah operator yang digunakan untuk membuat ekspresi bersyarat yang menggantikan penggunaan pernyataan if-else dalam beberapa kasus yang sederhana. Kita dapat menggunakan ternary operator ketika kita ingin mengevaluasi suatu ekspresi dan memilih nilai berdasarkan kondisi tertentu.<br/>
    - Contoh tanpa ternary operator:
        ```java
        int nilai = 8;
        String pesanKelulusan;
        if (nilai >= 7) {
            pesanKelulusan = "Anda lulus";
        } else {
            pesanKelulusan = "Anda tidak lulus";
        }
        System.out.println(pesanKelulusan); // Anda lulus
        ```
    - Contoh dengan ternary operator:
        ```java
        int nilai = 8;
        String pesanKelulusan = nilai >= 7 ? "Anda lulus" : "Anda tidak lulus";
        System.out.println(pesanKelulusan); // Anda lulus
        ```