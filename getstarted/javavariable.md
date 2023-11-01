## 2. Java Variabel
Variable adalah wadah untuk menyimpan nilai data

Di Java, ada berbagai jenis variable, misalnya
- `byte` menyimpan bilangan bulat pada rentang -128 ~ 127 

- `short` menyimpan bilangan bulat pada rentang -32768 ~ 32767

- `int` menyimpan bilangan bulat pada rentang -2147483648 ~ 2147483647 

- `long` menyimpan bilangan bulat pada rentang -9223372036854775808 ~ 9223372036854775807 

- `float` menyimpan angka floating point (desimal) pada rentang 1.4e-45f ~ 3.4028235e+38f

- `double` menyimpan angka floating point (desimal) pada rentang 4.9e-324 ~ 1.7976931348623157e+308

- `boolean` menyimpan nilai dengan dua status: `true` dan `false`

- `char` menyimpan karakter tunggal, seperti 'a' atau 'B'. Nilai char diapit oleh tanda kutip tunggal

- `String` menyimpan teks, seperti "Halo". Nilai string diapit oleh tanda kutip ganda

### Mendeklarasikan Variabel
---
untuk membuat variabel, kita harus menentukan tipe dan memberinya nilai, seperti:
```
type namaVariabel = value;
```
Dimana `type` adalah salah satu tipe data Java (misal `int` atau `String`), dan `namaVariabel` adalah nama variabel yang ingin kita tetapkan, dan tidak boleh diawali dengan angka, juga mengandung spasi. Tanda `=` digunakan untuk memberikan nilai pada variable.

berikut beberapa contoh membuat variabel:
```java
byte aByte = 100;
short aShort = 1000;
int anInt = 1000000;
int underscoreInt = 1_000_000; // untuk mempermudah membaca
int hexInt = 0xF4240;
int binInt = 0b11110100001001000000;
long aLong = 1000000000L;
long underscoreLong = 1_000_000_000L // untuk mempermudah membaca

float aFloat = 3.14F;
double aDouble = 123.5424234;

boolean benar = true;
boolean salah = false;

char n = 'N';
char F = 'F';
char L = 'L';

String firstString = "Hello";
String secondString = "World";
String fullString = firstString + " " + secondString; // Hello World
```

beberapa contoh bentuk lain dalam pembuatan variabel:
```java
float pi; // menyiapkan sebuah variabel yang tidak langsung diberi nilai
pi = 3.14F;

int a, b, c; // menyiapkan tiga buah variabel a, b, c yang belum diberi nilai
int x = 5, y = 10; // membuat dua variabel x dan y dengan tipe data yang sama
```

### `var` keyword
---
Java versi 10 mendukung kata kunci `var`, sehingga tipe data dapat menyesuaikan dengan nilai yang diberikan. kata kunci `var` **harus** langsung di-inisialisasi (beri nilai)

```java
var java = "Java"; // otomatis variabel java akan memiliki tipe data String
```

**contoh yang salah:**
```java
var java;
java = "Java";
```

### `final` keyword
---
Kata kunci `final` akan membuat variabel yang ditandainya hanya bisa memasukkan nilai **sekali** saja. Contoh :
```java
final String name = "John Doe";
name = "Jane Doe"; // error
```
```java
final String name;
name = "John Doe";
name = "Jane Doe"; // error
```

### Primitive vs Non-Primitive
---
#### primitive
- Bawaan bahasa pemrograman
- Memiliki default value
    - Default value untuk tipe data :
        - number = 0
        - boolean = false
        - char = \u0000 (representasi karakter escape)
- Diawali huruf kecil
    - `b`yte
    - `s`hort
    - `i`nt
    - `l`ong
    - `f`loat
    - `d`ouble
    - `b`oolean
    - `c`har

#### Non-Primitive
- Tidak memiliki default value (null)
- Didalamnya memiliki method/function untuk kebutuhan kita, seperti pengecekan, komparasi, manipulasi, dan sebagainya
- Setiap data primitive memiliki representasi Non-Primitive
- Diawali huruf besar
    - `B`yte
    - `S`hort
    - `I`nteger
    - `L`ong
    - `F`loat
    - `D`ouble
    - `B`oolean
    - `C`haracter
    - `S`tring

### Konversi Tipe Data
---
```java
// dari ukuran kecil ke besar
byte aByte = 10;
short aShort = aByte;
int anInt = aShort;

// dari ukuran besar ke kecil
byte aByte = (byte) anInt;


// Primitive ke Non-Primitive
int anInt = 100
Integer anInteger = anInt;

// Non-Primitive ke Primitive
int primInt = anInteger;
short aShort = anInteger.shortValue();
long aLong = anInteger.longValue();
float aFloat = anInteger.floatValue();
```
### Arrays
---
Arrays digunakan untuk menyimpan lebih dari satu value dalam satu variable dengan ukuran yang tetap.

Untuk membuat arrays di java kita bisa menyebutkan tipe data dengan diakhiri tanda `[]`
```java
String[] cars;
```
Kemudian untuk memasukkan nilai, kita bisa memasukkan nilai dengan tanda koma `,` sebagai pemisah, dimasukkan ke dalam kurung kurawal `{}`:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
int[] myNum = {10, 20, 30, 40};
```
Berikut merupakan contoh untuk mengakses sebuah elemen didalam array:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]); // Output: Volvo
```
Untuk mendapatkan panjang sebuah array:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);  // Output: 4
```
Untuk membuat array kosong dengan panjang tertentu:
```java
int[] numbers = new int[5];
```
Kemudian untuk memberi nilai kedalam array, kita bisa melakukannya seperti:
```java
int[] numbers = new int[5];
number[0] = 1;
number[1] = 2;
number[2] = 3;
number[3] = 4;
number[4] = 5;
```
beberapa cara lain untuk membuat array:
```java
int[] numbers = new int[]{
    1, 2, 3, 4, 5
};
System.out.println(numbers.length);  // Output: 5

String[] names;
names = new String[2];
names[0] = "James";
names[1] = "Gosling";

// array dua dimensi
String[][] teams = {
    {"Billie", "James"},
    {"Justin", "Anang"},
    {"Ariana", "Bryan"}
};
System.out.println(teams[1][1]); // Output: Anang
```