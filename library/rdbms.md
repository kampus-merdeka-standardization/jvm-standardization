# RDBMS
RDBMS atau _Relational Database Management System_ adalah program atau sistem yang melayani sistem basis data. Entitas utama dari sistem ini terdiri dari tabel-tabel yang mempunyai relasi dari satu tabel ke tabel yang lain. Suatu database terdiri dari banyak tabel. Tabel ini terdiri dari banyak field yang merupakan kolomnya.

## Beberapa RDBMS
Beberapa RDBMS ialah :

### 1. **Oracle**:
   - Oracle adalah sistem manajemen basis data relasional (RDBMS) yang paling populer di dunia pada September 2023.
   - Oracle menyediakan lebih banyak fitur dan manfaat bagi pengguna.
   - Oracle memiliki skor peringkat 1240.88, menjadikannya RDBMS terpopuler.

### 2. **Spring Data JPA**:
   - Spring Data JPA adalah abstraksi akses data JPA.
   - Spring Data JPA tidak dapat bekerja tanpa penyedia JPA.
   - Spring Data JPA menawarkan solusi untuk pola Repository DDD (Domain-Driven Design) atau pola DAO (Data Access Object).
   - Spring Data JPA juga dapat menghasilkan query JPA atas nama Anda melalui konvensi nama metode.
   - Spring Data JPA adalah pilihan otomatis untuk aplikasi yang menghargai kesederhanaan dalam domain dan generasi kode.
   - [Spring Data JPA](/documentationbe/java/library/orm)

### 3. **Spring Data JPA R2DBC**:
   - Spring Data R2DBC berbagi kode dan properti dengan Spring Data JDBC.
   - Ini pada dasarnya adalah pengganti Spring Data JPA.
   - Spring Data R2DBC menggunakan aliran reaktif dan model I/O non-blocking untuk menangani operasi basis data, membuatnya sangat cocok untuk sistem konkuren.
   - R2DBC jelas memberikan waktu respons terbaik pada konkurensi yang lebih tinggi.

### 4. **MySQL Connector/J**:
   - MySQL Connector/J adalah driver JDBC untuk MySQL.
   - mysql-connector-java-5.1.46.jar dan mysql-connector-java-5.1.46-bin.jar adalah identik secara biner, kecuali untuk META-INF/INDEX.LIST (yang berisi nama file jar sebenarnya).
   - Anda dapat menggunakan salah satu dari mereka sesuai preferensi Anda.

## Kelebihan dan kekurangan dari setiap RDBMS
**_reference_** : 
- [https://www.baeldung.com/jdbc-vs-r2dbc-vs-spring-jdbc-vs-spring-data-jdbc](https://www.baeldung.com/jdbc-vs-r2dbc-vs-spring-jdbc-vs-spring-data-jdbc)
- [https://www.baeldung.com/spring-data-jpa-vs-jpa](https://www.baeldung.com/spring-data-jpa-vs-jpa)
- [https://www.jetorbit.com/blog/mengenal-apa-itu-oracle-database/](https://www.jetorbit.com/blog/mengenal-apa-itu-oracle-database/)


### Kelebihan
#### 1. **Oracle**:
- Oracle Database menawarkan fitur keamanan yang kuat, seperti enkripsi data, kontrol akses, dan audit.
- Oracle Database mendukung banyak platform, termasuk Windows, Linux, Unix, dan macOS.
- Oracle Database menawarkan kinerja yang cepat dan skalabilitas yang baik.

#### 2. **Spring Data JPA**:
- Spring Data JPA menyediakan antarmuka pemrograman aplikasi (API) yang mudah digunakan untuk mengakses database relasional.
- Spring Data JPA menghilangkan boilerplate code dengan menyediakan implementasi default untuk operasi dasar seperti menyimpan, mengambil, dan menghapus data.
- Spring Data JPA memungkinkan pengembang untuk menggunakan anotasi Java untuk menentukan kueri SQL daripada menulis kueri SQL secara manual.

#### 3. **Spring Data JPA R2DBC**:
- Spring Data R2DBC menggunakan model pemrograman reaktif untuk mengakses database relasional. Ini memungkinkan aplikasi untuk beroperasi secara non-blocking dan dapat meningkatkan kinerja dalam sistem konkuren.
- Spring Data R2DBC mendukung banyak database relasional seperti MySQL, PostgreSQL, Microsoft SQL Server, dan lain-lain.

#### 4. **MySQL Connector/J**:
- MySQL Connector/J adalah driver JDBC resmi untuk MySQL. Ini mendukung banyak fitur MySQL seperti transaksi, indeks, dan prosedur tersimpan.
- MySQL Connector/J mudah diinstal dan dikonfigurasi.


### Kekurangan
#### 1. **Oracle**:
- Oracle Database adalah perangkat lunak komersial yang tidak gratis. Oleh karena itu, tidak cocok untuk penggunaan jangka pendek atau perusahaan kecil dan menengah.
- Oracle Database memerlukan sumber daya sistem yang cukup besar untuk menjalankannya

#### 2. **Spring Data JPA**:
- Spring Data JPA memiliki keterbatasan dalam hal kinerja dan skalabilitas ketika digunakan dalam sistem yang sangat konkuren.
- Spring Data JPA memiliki kurva pembelajaran yang curam bagi pengembang baru.

#### 3. **Spring Data JPA R2DBC**:
- Spring Data R2DBC adalah teknologi baru sehingga tidak semua database mendukungnya. Selain itu, driver yang tersedia mungkin berbeda tergantung pada database yang digunakan.
- Spring Data R2DBC memiliki kurva pembelajaran yang curam bagi pengembang baru.

#### 4. **MySQL Connector/J**:
- MySQL Connector/J menggunakan model I/O blocking sehingga dapat membatasi skalabilitas dalam sistem konkuren.
- MySQL Connector/J memiliki kurva pembelajaran yang curam bagi pengembang baru.


## JDBC vs. R2DBC vs. Spring JDBC vs. Spring Data JDBC
| Feature | JDBC | R2DBC | Spring JDBC | Spring Data JDBC |
|:--------|:----:|:-----:|:-----------:|:----------------:|
| API | Low level | Low level | High level | High level |
| Performance | Good | Excellent | Good | Good |
| Communication | Synchronous | Reactive | Synchronous | Asynchronous |
| Maturity | Mature | Newer | Mature | Newer |
| Features | Fewer features | Few features | More features | More features |
| Ease of use | Easy | Moderate | Easy | Easy |
| Support | Widespread | Growing | Widespread | Growing |

**_reference_** : [https://www.baeldung.com/jdbc-vs-r2dbc-vs-spring-jdbc-vs-spring-data-jdbc](https://www.baeldung.com/jdbc-vs-r2dbc-vs-spring-jdbc-vs-spring-data-jdbc)