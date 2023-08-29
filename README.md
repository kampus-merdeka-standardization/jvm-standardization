# Spring Standardization 🍃🍃🍃
Sebuah dokumentasi untuk menyesuaikan gaya penggunaan Spring menggunakan bahasa Java

## Pembuatan Project
### 1. Membuat project pada [https://start.spring.io](https://start.spring.io)
### 2. nama project (artifact) ditulis, menggunakan penulisan `kebab-case`

## Penulisan di Java
### 1. Untuk nama `class` menggunakan `PascalCase`.
### 2. Untuk nama variable serta method, menggunakan `camelCase`


## Struktur Project
```
nama-project/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com.nama.group/
│   │   │   │   ├── controller/
│   │   │   │   │   ├── ContohController
│   │   │   │   ├── repository/
│   │   │   │   │   ├── ContohRepository
│   │   │   │   ├── service/
│   │   │   │   │   ├── impl
│   │   │   │   │   │   ├── ContohServiceImpl (interface implementation)
│   │   │   │   │   ├── ContohService (interface)
│   │   ├── resources/
│   │   │   ├── application.yaml
│   ├── test/ 
│   │   ├── java/
│   │   │   ├── com.nama.group/
│   │   │   │   ├── controller/
│   │   │   │   │   ├── ContohControllerTest
│   │   │   │   ├── repository/
│   │   │   │   │   ├── ContohRepositoryTest
│   │   │   │   ├── service/
│   │   │   │   │   ├── ContohServiceTest
├── pom.xml
├── README.md
```

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

## ORM - Java Persistence API (JPA)
### Tujuannya adalah untuk mempermudah developer dalam berinteraksi dengan database, (contoh: MySql, PostgreSql, MongoDb, etc.)

## JDBC Template
### Sebagai opsi lain dari JPA. Digunakan ketika dirasa butuh yang lebih cepat

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
### Untuk membuat validation umum (seperti minimal/maximal size, format email, nonull/noblank, etc.) lebih mudah

## Membuat Data Class untuk kebutuhan Request & Response API (DTO)
### Tujuannya adalah agar lebih fleksibel akan kebutuhan request serta response. Juga berguna ketika membuat validasi

## Menaruh Segala Validasi pada DTO, bukan pada entity-nya langsung
### Tujuannya adalah agar lebih mudah di-maintain