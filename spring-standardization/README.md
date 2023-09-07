# Spring Standardization 🍃🍃🍃
Sebuah dokumentasi untuk menyesuaikan gaya penggunaan Spring menggunakan bahasa Java

## Kelebihan dan Kekurangan Spring Framework [^](#)

### Kelebihan [^](#)
1. ***Flexibility*** : Menawarkan perpustakaan fleksibel untuk membantu pengembang. Pengguna dapat memilih antara anotasi berbasis XML atau Java mengenai konfigurasi. Fitur IoC dan DI juga hadir untuk memberikan fungsionalitas dan fitur yang luas.

2. ***Portability***: Ini adalah kerangka kerja yang portabel karena kita dapat menggunakan sisi klien dalam logika bisnis aplikasi swing dan sisi server dalam aplikasi web/EJB.

3. ***Consistent configuration***: Ini juga membantu dalam menyediakan cara konfigurasi yang konsisten. Ini menawarkan konfigurasi terpisah untuk mempermudah pengembang.

4. ***Fast delivery***: Ini juga merupakan alasan _startup_ dan _shutdown_ cepat. Ini menghasilkan peningkatan kinerja dan membuat _framework_ ini cepat. Eksekusi yang dioptimalkan yang ditawarkan oleh Spring juga membantu dalam hal ini.

5. ***Secure***:  _framework_ ini menyediakan pembaruan yang sering untuk membuat data dan aplikasi kita lebih aman. Kita juga dapat menggunakan _Spring security framework_ dalam hal ini.

6. ***Simpler testing***: Para pengembang dapat melakukan pengujian dengan mudah berkat _framework_ Spring. Ini memungkinkan karena penggunaan _dependency injection_

7. ***AOP module***: Para pengembang dapat mencapai beberapa unit kompilasi. Mereka juga dapat memiliki _loader_ kelas yang terpisah

### Kekurangan [^](#)
1. ***Fewer guidelines***: Tidak ada prosedur yang tepat dalam dokumentasi Spring untuk mengatasi ancaman seperti XSS atau cross-site scripting. Informasi dan pedoman yang berguna harus disediakan untuk menghentikan peretas dari mengakses dan merusak aplikasi Anda.

2. ***Complexity***: Ini cukup kompleks untuk bekerja dengan Spring. Para pengembang harus memiliki keterampilan dan keahlian yang lebih relevan untuk menggunakan _framework_ ini.

3. ***Hard to learn***: Jika Anda tidak memiliki pengalaman dalam pengembangan, cukup sulit bagi Anda untuk mempelajari Spring. Hal ini disebabkan oleh penggabungan teknik pemrograman terbaru dalam kerangka kerja ini.

4. ***Uses XML***: Kita memerlukan banyak XML saat mengembangkan aplikasi Spring. Ini juga bisa menjadi masalah bagi para pengembang.

5. ***Parallel mechanism***: Para pengembang dapat memperoleh banyak opsi. Ini dapat membantu para pengembang tetapi juga dapat menjadi sumber kebingungan. Para pengembang dapat menghadapi masalah dalam memilih mekanisme yang tepat dan ini dapat mengakibatkan pengambilan keputusan yang salah. Pilihan yang salah ini bisa menyebabkan penundaan besar dalam pengembangan aplikasi.

[_reference_](https://www-educative-io.translate.goog/answers/what-are-java-spring-framework-advantages-and-disadvantages?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=id&_x_tr_pto=tc&_x_tr_hist=true)

## Pembuatan Project [^](#)
1. Membuat project pada [https://start.spring.io](https://start.spring.io)
2. nama project (artifact) ditulis, menggunakan penulisan `kebab-case`

## Penulisan di Java [^](#)
1. Untuk nama `class` menggunakan `PascalCase`.
2. Untuk nama variable serta method, menggunakan `camelCase`.
3. Segala variable di letakkan pada bagian atas dalam sebuah kelas, kemudian baru diikuti method dan sebagainya.
4. Method ditulis secara berurutan sesuai dengan tingkat kepentingannya.


## Struktur Project [^](#)
```
nama-project/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.nama.group/
│   │   │       ├── config/
│   │   │       │   └── ContohConfig.java
│   │   │       ├── controller/
│   │   │       │   └── ContohController.java
│   │   │       ├── dto/
│   │   │       │   ├── request/
│   │   │       │   │   └── ContohRequest.java
│   │   │       │   └── response/
│   │   │       │       └── ContohResponse.java
│   │   │       ├── entity/
│   │   │       │   └── User.java /* dalam bentuk tunggal, bukan jamak */
│   │   │       ├── repository/
│   │   │       │   └── ContohRepository.java
│   │   │       ├── security/
│   │   │       ├── service/
│   │   │       │   ├── impl
│   │   │       │   │   └── ContohServiceImpl.java /* interface implementation */
│   │   │       │   └── ContohService.java /* interface */
│   │   │       └── util/
│   │   │           └── ContohUtil.java
│   │   └── resources/
│   │       └── application.yaml
│   └── test/
│       └── java/
│           └── com.nama.group/
│               ├── config/
│               │   └── ContohConfigTest.java
│               ├── controller/
│               │   └── ContohControllerTest.java
│               ├── dto/
│               │   ├── request/
│               │   │   └── ContohRequestTest.java
│               │   └── response/
│               │       └── ContohResponseTest.java
│               ├── entity/
│               │   └── UserTest.java 
│               ├── repository/
│               │   └── ContohRepositoryTest.java
│               ├── security/
│               ├── service/
│               │   └── ContohServiceTest.java
│               └── util/
│                 └── ContohUtilTest.java
├── pom.xml
└── README.md
```
### Penjelasan Struktur Project [^](#) : 
1. Biasanya nama `class` ditulis dengan diakhiri dengan nama package. Contoh pada package `controller`, nama class di dalamnya menjadi `ContohController`.
2. Ada beberapa class yang tidak diakhiri nama package, seperti `entity`
3. `entity` ditulis dengan nama yang ditulis `tunggal (singular)`. Tidak seperti nama tabel di database yang ditulis jamak.

## Java Lombok [^](#)
Tujuannya adalah untuk mempermudah developer untuk fokus dengan logika pemrograman saja, dengan cara mengotomatisasi hal-hal berikut:
1. Getter Setter
2. Constructor
3. ToString
4. Equals And HashCode
5. Builder
6. Slf4j
7. Throws
8. Synchronized
9. dan masih banyak fitur lainnya lagi 

[Click here for the references !](https://projectlombok.org/)

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <optional>true</optional>
</dependency>
```

## ORM - Java Persistence API (JPA) [^](#)
Tujuannya adalah untuk mempermudah developer dalam berinteraksi dengan database, (contoh: MySql, PostgreSql, MongoDb, etc.)

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

## JDBC Template [^](#)
Sebagai opsi lain dari JPA. Digunakan ketika dirasa butuh yang lebih cepat

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jdbc</artifactId>
</dependency>
```

## Penulisan API [^](#)
```java
@GetMapping(
        path = "/api/contoh",
        consumes = MediaType.APPLICATION_JSON_VALUE
)
public ContohResponse get(User user) {
    /* ... */
}
```
```java
@PostMapping(
        path = "/api/contoh",
        consumes = MediaType.APPLICATION_JSON_VALUE,
        produces = MediaType.APPLICATION_JSON_VALUE
)
public ContohResponse post(@RequestBody ContohRequest request) {
    /* ... */
}
```


## Spring Validation [^](#)
Untuk membuat validation umum (seperti minimal/maximal size, format email, nonull/noblank, etc.) lebih mudah.

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml 
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

## Membuat Data Class untuk kebutuhan Request & Response API (DTO) [^](#)
Tujuannya adalah agar lebih fleksibel akan kebutuhan request serta response. Juga berguna ketika membuat validasi

## Segala Validasi dilakukan di DTO, bukan pada entity-nya langsung [^](#)
Tujuannya adalah agar lebih mudah di-maintain