## JDBC Template
Sebagai opsi lain dari JPA. Digunakan ketika dirasa butuh yang lebih cepat

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jdbc</artifactId>
</dependency>
```

### Spring Data JPA vs JDBC Template

- Spring Data JPA :
    - JPA adalah standar Java yang memungkinkan kita untuk mengikat objek Java ke _records_ dalam database relasional.

    - JPA memungkinkan pengembang untuk membuat program Java yang didukung database menggunakan semantik berorientasi objek.

    - JPA adalah agnostik database, yang berarti kode yang sama dapat digunakan dalam berbagai database dengan sedikit (atau tanpa) modifikasi.

    - JPA adalah _Java Persistence API_, yang merupakan API standard Java untuk melakukan _object-relational mapping_

    - _Spring Framework_ terdiri dari beberapa projek, salah satunya adalah _Spring Data_. _Spring Data_ bertujuan untuk mempermudah kita dalam bekerja pada jenis database yang berbeda, mulai dari relational databases sampai NoSQL Databases.

    - Jika Anda ingin mengakses skema database Anda melalui model domain, maka Spring Data JPA bisa menjadi pilihan yang baik.

- JDBC Template
    - JDBC adalah antarmuka tingkat pemrograman untuk aplikasi Java yang berkomunikasi dengan database.

    - JDBC memungkinkan kita untuk menulis perintah SQL untuk membaca data dari dan memperbarui data ke database relasional.

    - JDBC adalah dependen database, yang berarti bahwa skrip yang berbeda harus ditulis untuk database yang berbeda.
    
    - Gunakan JDBC Template jika Anda tidak ingin mengakses skema database Anda melalui model domain.

### Performa
Perbedaan antara JPA dan JDBC pada dasarnya adalah siapa yang melakukan pengkodean: JPA _framework_ atau pengembang lokal. Apa pun itu, kita harus berurusan dengan ketidakcocokan impedansi relasi objek.

Agar adil, ketika kita menulis query SQL dengan tidak benar, kinerja JDBC bisa sangat lamban. Ketika memutuskan antara kedua teknologi tersebut, kinerja seharusnya tidak menjadi titik perselisihan. Pengembang profesional lebih dari mampu menghasilkan aplikasi Java yang berjalan sama baiknya terlepas dari teknologi yang digunakan.

### _Exception Handling_
Karena JDBC melempar _checked exception_, seperti SQLException, kita harus menuliskannya dalam blok _try-catch_. Di sisi lain, kerangka kerja JPA hanya menggunakan _unchecked exception_, seperti Hibernate. Oleh karena itu, kita tidak perlu _catch_ atau mendeklarasikannya di setiap tempat kita menggunakannya.

### Pros and Cons
Manfaat yang paling jelas dari JDBC dibandingkan JPA adalah lebih mudah dipahami. Di sisi lain, jika pengembang tidak memahami cara kerja internal kerangka kerja JPA atau desain basis data, mereka tidak akan dapat menulis kode yang baik.

Selain itu, JPA dianggap lebih cocok untuk aplikasi yang lebih canggih oleh banyak pengembang. Namun, JDBC dianggap sebagai alternatif yang lebih baik jika sebuah aplikasi akan menggunakan database yang sederhana dan kita tidak berencana untuk memigrasikannya ke vendor database yang berbeda.

Keuntungan utama JPA dibandingkan JDBC bagi para pengembang adalah bahwa mereka dapat mengkodekan aplikasi Java mereka menggunakan prinsip-prinsip berorientasi objek dan praktik terbaik tanpa harus mengkhawatirkan semantik database. Hasilnya, pengembangan dapat diselesaikan lebih cepat, terutama ketika pengembang perangkat lunak tidak memiliki pemahaman yang kuat tentang SQL dan database relasional.

Selain itu, karena kerangka kerja yang telah teruji dan kuat menangani interaksi antara database dan aplikasi Java, kita akan melihat penurunan kesalahan dari lapisan pemetaan database ketika menggunakan JPA.

### reference
1. [A Comparison Between JPA and JDBC | Baeldung](https://www.baeldung.com/jpa-vs-jdbc)
2. [java - Spring Data vs Spring Data JPA vs JdbcTemplate - Stack Overflow](https://stackoverflow.com/questions/52532319/spring-data-vs-spring-data-jpa-vs-jdbctemplate)