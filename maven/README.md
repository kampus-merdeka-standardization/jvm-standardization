# Apache Maven 🪶🪶🪶

Salah satu _Build Automation Tool_ yang populer pada kalangan _developer_ Java adalah **Maven**. _Build Automation_ adalah proses otomatisasi pembangunan perangkat lunak yang bertujuan untuk mempermudah pengembang dalam mengelola dan mengotomatisasi tugas-tugas yang terkait dengan kompilasi, pengujian, dan distribusi kode sumber. Maven adalah salah satu alat (tool) yang digunakan dalam build automation di dunia pengembangan perangkat lunak, khususnya dalam proyek-proyek berbasis Java.

Ada opsi lain selain **Apache Maven**, seperti **Gradle**. Gradle sendiri populer untuk kalangan programmer bahasa **Kotlin**.

Untuk lebih lengkapnya, kita bisa langsung melihat pada dokumentasi-nya langsung pada tautan https://maven.apache.org/guides/getting-started/index.html

## Instalasi Maven [^](#)

- Maven dibuat menggunakan bahasa pemrograman java yang notabene-nya multiplatform, jadi segala jenis OS dapat menginstallnya pada tautan [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)

- Seletah instalasi `zip` file, kemudian ekstrak pada direktori yang kita inginkan

- Masukkan lokasi direktori kedalam environment variable dengan nama variable `MAVEN_HOME`

- Masukkan lokasi `bin` direktori dari maven ke dalam `Path` di dalam environment variable

- Kedua langkah diatas kurang lebih sama dengan cara menambahkan environment variable untuk java yang dapat dilihat pada laman [**<u>ini</u>**](/java-standardization/README.md#b-instalasi-jdk-)

- Pastikan dengan mencoba perintah
    ```
    mvn --version
    ```

    kalau berhasil akan muncul detail versi maven seperti

    ```
    Apache Maven 3.9.4 (dfbb324ad4a7c8fb0bf182e6d91b0ae20e3d2dd9)
    Maven home: C:\Program Files\Maven\apache-maven-3.9.4
    Java version: 17.0.2, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-17.0.2
    Default locale: en_US, platform encoding: Cp1252
    OS name: "windows 11", version: "10.0", arch: "amd64", family: "windows"
    ```
    versi mungkin berbeda sesuai yang kita install sebelumnya

## Membuat Project [^](#)
- Buka terminal pada direktori dimana project akan disimpan
- Ketik
    ```sh
    mvn archetype:generate
    ```
- Akan muncul berbagai template, kemudian carilah `maven-archetype-quickstart`
    ```
    Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): : maven-archetype-quickstart
    Choose archetype:
    1: remote -> com.github.ywchang:maven-archetype-quickstart (Provide up-to-date java quickstart archetype)
    2: remote -> com.haoxuer.maven.archetype:maven-archetype-quickstart (a simple maven archetype)
    3: remote -> org.apache.maven.archetypes:maven-archetype-quickstart (An archetype which contains a sample Maven project.)
    Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): 3:
    ```
    pilih nomor 3 dan enter

- Pilih versi
    ```
    Choose org.apache.maven.archetypes:maven-archetype-quickstart version:
    1: 1.0-alpha-1
    2: 1.0-alpha-2
    3: 1.0-alpha-3
    4: 1.0-alpha-4
    5: 1.0
    6: 1.1
    7: 1.3
    8: 1.4
    Choose a number: 8:
    ```
    default terpilih nomor 8, kita bisa tinggal tekan enter

- 
    ```
    Define value for property 'groupId':
    ```
    Tulislah nama untuk `groupId` sesuai yang kita inginkan.<br/>`groupId` biasanya merepresentasikan nama company. Misal kita isi dengan **company-name**

- 
    ```
    Define value for property 'artifactId':
    ```
    Tulislah nama untuk `artifactId` sesuai yang kita inginkan.<br/>`artifactId` merepresentasikan nama project kita. Misal kita isi dengan **demo-maven**

- 
    ```
    Define value for property 'version' 1.0-SNAPSHOT: :
    ```
    Tulislah versi aplikasi project kita. Default `1.0-SNAPSHOT`, kita bisa langsung enter bila ingin menggunakan default version.

- 
    ```
    Define value for property 'package' company-name: :
    ```
    Ini merupakan package pada main program kita. Biasanya penamaan package dinamai secara terbalik dari nama domain kita. Contoh, jika domain kita adalah **example.com**, maka package dapat dinamai **com.example.maven**.<br/>Misal kita isi dengan **com.example.maven**

- 
    ```
    Confirm properties configuration:
    groupId: company-name
    artifactId: demo-maven
    version: 1.0-SNAPSHOT
    package: com.example.maven
    Y: :
    ```
    Tekan `Y` (atau langsung enter, karena secara default sudah 'Y') jika detail yang diberikan sudah sesuai dengan apa yang kita isi 

- Project siap di gunakan

## Struktur Maven Project [^](#)
```
nama-project/
├── pom.xml
└── src/
    ├── main/
    |   └── java/
    |       └── com.example.app/
    |           └── App.java
    └── test/
        └── java/
            └── com.example.app/
                └── AppTest.java
```

#### Penjelasan Struktur kode di atas :
- `src.main.java.com.example.app` merupakan lokasi dimana kode program java ditempatkan

- `src.test.java.com.example.app` merupakan lokaasi dimana unit test program java ditempatkan

- `pom.xml` merupakan inti dari konfigurasi project Maven. Ini merupakan file konfigurasi yang berisi sebagian besar informasi yang diperlukan untuk membangun project sesuai yang kita inginkan.

## Maven Lifecycle [^](#)

- `validate`: validate the project is correct and all necessary information is available
- `clean`: Deleting the target folder (where the compilation results are stored)
- `compile`: compile the source code of the project
- `test`: test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
- `package`: take the compiled code and package it in its distributable format, such as a JAR.
- `integration-test`: process and deploy the package if necessary into an environment where integration tests can be run
- `verify`: run any checks to verify the package is valid and meets quality criteria
- `install`: install the package into the local repository, for use as a dependency in other projects locally
- `deploy`: done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.
- untuk lebih lengkapnya, bisa dilihat pada dokumentasi nya langsung https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html

#### Cara menjalankan lifecycle :
Cara menjalankan lifecycle, cukup dengan menggunakan perintah `mvn namalifecycle`. Bisa juga lebih dari satu seperti `mvn clean test install`

## Dependency [^](#)
Dalam pembuatan aplikasi, sering kali kita butuh library dari luar untuk mendukung kemudahan kita dalam mengembangkan aplikasi. Tanpa Build Automation Tool seperti Apache Maven ini, akan banyak sekali yang harus dilakukan ketika kita ingin menambahkan library luar.

Untuk mencari dependency dari luar, kita bisa mencarinya pada :
- https://central.sonatype.com/
- https://mvnrepository.com/

Kemudian kita bisa menambahkan dependency yang kita butuhkan kedalam `pom.xml` pada bagian 
```xml
<dependencies>
    <!-- letakkan disini -->
</dependencies>
```

contoh : 
```xml
<dependencies>
    <dependency>
        <groupId>com.google.code.gson</groupId>
        <artifactId>gson</artifactId>
        <version>2.10.1</version>
    </dependency>
</dependencies>
```

## Repository [^](#)
Saat kita menambahkan dependency, maven akan mencari dependecy tersebut pada berbagai repository yang maven miliki. 

Terkadang kita ingin maven mencarinya pada repository yang kita inginkan, contoh repository pribadi atau milik perusahaan

untuk kita kita bisa menambahkannya pada bagian 
```xml
<repositories>
    <!-- letakkan disini -->
</repositories>
```

contoh :
```xml
<repositories>
    <repository>
        <id>id</id>
        <name>name</name>
        <url>url</url>
    </repository>
</repositories>
```