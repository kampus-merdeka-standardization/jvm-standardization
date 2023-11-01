## Pembuatan Project
1. Membuat project pada [https://start.spring.io](https://start.spring.io)
2. nama project (artifact) ditulis, menggunakan penulisan `kebab-case`

## Penulisan di Java
1. Untuk nama `class` menggunakan `PascalCase`.
2. Untuk nama variable serta method, menggunakan `camelCase`.
3. Segala variable di letakkan pada bagian atas dalam sebuah kelas, kemudian baru diikuti method dan sebagainya.
4. Method ditulis secara berurutan sesuai dengan tingkat kepentingannya.


## Struktur Project
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
### Penjelasan Struktur Project : 
1. Biasanya nama `class` ditulis dengan diakhiri dengan nama package. Contoh pada package `controller`, nama class di dalamnya menjadi `ContohController`.
2. Ada beberapa class yang tidak diakhiri nama package, seperti `entity`
3. `entity` ditulis dengan nama yang ditulis `tunggal (singular)`. Tidak seperti nama tabel di database yang ditulis jamak.

## Scheduler
Scheduler adalah komponen penting yang digunakan untuk mengatur eksekusi tugas atau proses secara otomatis berdasarkan jadwal tertentu. Scheduler dapat digunakan untuk menjalankan berbagai jenis tugas, seperti pemrosesan batch, pembaruan database, atau tugas pemeliharaan lainnya. Jadi, dalam konteks back-end, scheduler adalah alat yang sangat berguna untuk membantu mengelola dan mengotomatisasi tugas-tugas yang perlu dijalankan secara berkala atau pada waktu tertentu.

1. Quartz Scheduler
<br>Ini adalah _scheduling framework_ yang memungkinkan Anda untuk menjalankan sesuatu setiap jam atau setiap Jumat terakhir dalam sebulan. Quartz menyediakan _scheduling framework_ dan _job framework_ (semisal Anda tidak ingin menggunakan _Spring batch jobs_).

2. Spring Batch
<br>Ini adalah _framework_ yang mendefinisikan “sesuatu” yang akan dieksekusi. Anda dapat mendefinisikan pekerjaan, yang terdiri dari langkah-langkah. Biasanya, langkah adalah sesuatu yang terdiri dari pembaca item, prosesor item opsional, dan penulis item, tetapi Anda dapat mendefinisikan langkah kustom. Spring Batch menyediakan fungsionalitas untuk memproses volume data yang besar.

3. Spring Scheduler
<br> Ini adalah lapisan abstraksi yang ditulis untuk menyembunyikan implementasi Executors di berbagai JDK seperti Java SE 1.4, Java SE 5 dan lingkungan Java EE, yang memiliki implementasi spesifik mereka sendiri.

## Penulisan API
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

## Membuat Data Class untuk kebutuhan Request & Response API (DTO)
Tujuannya adalah agar lebih fleksibel akan kebutuhan request serta response. Juga berguna ketika membuat validasi

## Segala Validasi dilakukan di DTO, bukan pada entity-nya langsung
Tujuannya adalah agar lebih mudah di-maintain