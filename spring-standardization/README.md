# Spring Standardization 🍃🍃🍃
Sebuah dokumentasi untuk menyesuaikan gaya penggunaan Spring menggunakan bahasa Java

## Pembuatan Project
#### 1. Membuat project pada [https://start.spring.io](https://start.spring.io)
### 2. nama project (artifact) ditulis, menggunakan penulisan `kebab-case`

## Penulisan di Java
#### 1. Untuk nama `class` menggunakan `PascalCase`.
#### 2. Untuk nama variable serta method, menggunakan `camelCase`.
#### 3. Segala variable di letakkan pada bagian atas dalam sebuah kelas, kemudian baru diikuti method dan sebagainya.
#### 4. Method ditulis secara berurutan sesuai dengan tingkat kepentingannya.


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
#### 1. Biasanya nama `class` ditulis dengan diakhiri dengan nama package. Contoh pada package `controller`, nama class di dalamnya menjadi `ContohController`.
#### 2. Ada beberapa class yang tidak diakhiri nama package, seperti `entity`
#### 3. `entity` ditulis dengan nama yang ditulis `tunggal (singular)`. Tidak seperti nama tabel di database yang ditulis jamak.

## Java Lombok
### Tujuannya adalah untuk mempermudah developer untuk fokus dengan logika pemrograman saja, dengan cara mengotomatisasi hal-hal berikut:
#### 1. Getter Setter
#### 2. Constructor
#### 3. ToString
#### 4. Equals And HashCode
#### 5. Builder
#### 6. Slf4j
#### 7. Throws
#### 8. Synchronized
#### 9. dan masih banyak fitur lainnya lagi 
#### [Click here for the references !](https://projectlombok.org/)

#### Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.projectlombok</groupId>
    <artifactId>lombok</artifactId>
    <optional>true</optional>
</dependency>
```

## ORM - Java Persistence API (JPA)
### Tujuannya adalah untuk mempermudah developer dalam berinteraksi dengan database, (contoh: MySql, PostgreSql, MongoDb, etc.)

#### Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

## JDBC Template
### Sebagai opsi lain dari JPA. Digunakan ketika dirasa butuh yang lebih cepat
#### Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jdbc</artifactId>
</dependency>
```

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


## Spring Validation
#### Untuk membuat validation umum (seperti minimal/maximal size, format email, nonull/noblank, etc.) lebih mudah.

#### Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml 
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

## Membuat Data Class untuk kebutuhan Request & Response API (DTO)
#### Tujuannya adalah agar lebih fleksibel akan kebutuhan request serta response. Juga berguna ketika membuat validasi

## Segala Validasi dilakukan di DTO, bukan pada entity-nya langsung
#### Tujuannya adalah agar lebih mudah di-maintain