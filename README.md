# A. Pendahuluan
## Sejarah Singkat
Java adalah bahasa pemrograman yang dapat dijalankan di berbagai komputer termasuk telepon genggam. Bahasa ini awalnya dibuat oleh James Gosling saat masih bergabung di Sun Microsystems, yang saat ini merupakan bagian dari Oracle dan dirilis tahun 1995. Java terlahir dari The Green Project, yang berjalan selama 18 bulan, dari awal tahun 1991 hingga musim panas 1992. Proyek ini dimotori oleh Patrick Naughton, Mike Sheridan, dan James Gosling, beserta sembilan pemrogram lainnya dari Sun Microsystems. Salah satu hasil proyek ini adalah maskot Duke yang dibuat oleh Joe Palrang. Awalnya, Proyek ini dikenal sebagai "Oak" dan ditujukan untuk perangkat elektronik konsumen, seperti mesin cuci, tetapi visinya berkembang menjadi lebih luas. Nama Oak, diambil dari pohon oak yang tumbuh di depan jendela ruangan kerja “bapak java”, James Gosling. Nama Oak ini tidak dipakai untuk versi release Java karena sebuah perangkat lunak sudah terdaftar dengan merek dagang tersebut, sehingga diambil nama penggantinya menjadi “Java”. Nama ini diambil dari kopi murni yang digiling langsung dari biji (kopi tubruk) kesukaan Gosling.

## Kelebihan Java
1. ***Multiplatform***: Program Java dapat dijalankan di berbagai platform karena kode sumber Java dikompilasi menjadi bytecode yang dapat dijalankan di Mesin Virtual Java (JVM). Ini membuatnya sangat portabel dan dapat digunakan di berbagai sistem operasi.

2. ***Sintaksis yang Mudah Dipahami***: Sintaksis Java mirip dengan bahasa-bahasa pemrograman lainnya seperti C++ dan C#, sehingga mudah dipahami oleh banyak programmer.

3. ***Orientasi Objek***: Java adalah bahasa pemrograman berorientasi objek (OOP) yang memungkinkan pemodelan yang baik dari dunia nyata dan memudahkan pengembangan dan pemeliharaan kode.

4. ***Manajemen Memori Otomatis***: Java memiliki sistem pengelolaan memori otomatis yang mengelola alokasi dan penghapusan memori, menghindari banyak kesalahan yang terkait dengan memori, seperti kebocoran memori.

5. ***Keamanan***: Java dirancang dengan keamanan dalam pikiran. Itu memiliki mekanisme keamanan yang kuat, termasuk pemisahan kelas dan pustaka yang dapat diakses oleh kode sumber yang berbeda.

6. ***Kaya akan Ekosistem***: Java memiliki ekosistem yang kaya dengan berbagai pustaka dan framework yang mendukung pengembangan berbagai jenis aplikasi, termasuk aplikasi web, mobile, dan desktop.

7. ***Multithreading***: Java mendukung multithreading dengan mudah, yang memungkinkan pengembangan aplikasi yang dapat menjalankan beberapa tugas secara bersamaan, meningkatkan kinerja.

8. ***Ketahanan***: Program Java cenderung lebih tahan terhadap kesalahan dan kegagalan karena manajemen memori yang baik dan mekanisme penanganan pengecualian.

9. ***Dukungan Komunitas***: Java memiliki komunitas pengembang yang besar dan aktif, sehingga Anda dapat dengan mudah menemukan dukungan, dokumentasi, dan solusi untuk masalah yang mungkin Anda hadapi.

10. ***Perusahaan***: Java sering digunakan dalam pengembangan perangkat lunak bisnis dan aplikasi perusahaan, sehingga memiliki dukungan kuat dari banyak perusahaan besar.

11. ***Performa yang Cukup Baik***: Meskipun Java tidak selalu secepat bahasa pemrograman lain seperti C++ atau Rust, performanya cukup baik dan terus meningkat dengan setiap versi baru.

12. ***Pembaruan Rutin***: Java secara teratur diperbarui oleh Oracle dan komunitas terbuka, yang memastikan adanya peningkatan terus-menerus dalam bahasa dan platformnya.

13. ***Kompatibilitas Mundur***: Java biasanya mendukung kompatibilitas mundur, yang berarti kode Java lama cenderung masih berjalan pada versi Java yang lebih baru dengan sedikit atau tanpa perubahan.

## Kekurangan Java
1. ***Konsumsi Memori:*** Java membutuhkan memori yang cukup tinggi. Bahasa pemrograman Java menawarkan banyak fitur yang luar biasa, mulai dari kemudahan dalam menyusun skrip, hingga fitur berorientasi objek, yang menjadi salah satu ciri khas dari bahasa pemrograman Java. Namun, hal ini juga berdampak pada penggunaan memori yang cukup besar, sehingga dapat memperlambat kinerja aplikasi atau program yang dibuat dengan Java

2. ***Mudah Didekompilasi:*** Kode sumber Java yang telah dikompilasi menjadi bytecode dapat dengan mudah didekompilasi kembali menjadi kode sumber asli dengan menggunakan alat decompiler. Hal ini dapat menimbulkan masalah keamanan dan privasi bagi pengembang aplikasi atau program yang ingin melindungi kode sumber mereka dari orang lain.

3. ***GUI Kurang Menarik:*** Java memiliki Graphical User Interface (GUI) yang kurang menarik. Dibandingkan dengan bahasa pemrograman lain seperti C# atau Visual Basic, Java memiliki GUI yang kurang menarik dan variatif. Hal ini dapat mengurangi minat pengguna untuk menggunakan aplikasi atau program yang dibuat dengan Java.

4. ***Kode yang Panjang***: Beberapa pengembang menganggap kode Java lebih panjang daripada bahasa pemrograman lain seperti Python. Hal ini bisa mengakibatkan penulisan kode yang lebih lambat dan berisiko terhadap kesalahan.

## Reference
- [https://idwebhost.com/blog/apa-itu-java/](https://idwebhost.com/blog/apa-itu-java/)
- [https://dosenit.com/kuliah-it/pemrograman/kelebihan-dan-kekurangan-java](https://dosenit.com/kuliah-it/pemrograman/kelebihan-dan-kekurangan-java/)
- [https://www.microdataindonesia.co.id/news/read/235/mengenal-kelabihan-dan-kekurangan-java](https://www.microdataindonesia.co.id/news/read/235/mengenal-kelabihan-dan-kekurangan-java)

## JDK vs JRE
sederhananya `JDK (Java Development Kit)` merupakan tools untuk `mengembangkan` program java, sedangkan `JRE (Java Runtime Environment)` merupakan tools untuk `menjalankan` program java. Ketika menginstall JDK didalamnya sudah terdapat JRE, sehingga kita tidak perlu lagi untuk menginstal JRE

# B. Instalasi JDK
Pada dokumentasi ini, kita akan mencoba meng-install menggunakan [OpenJDK](https://openjdk.java.net/) dikarenakan open source dan juga free.

Selain OpenJDK ada beberapa alternatif lain seperti:
- [OracleJDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Amazon Corretto](https://aws.amazon.com/id/corretto/)
- [Zulu](https://www.azul.com/downloads/zulu-community/)


## Windows
1. Install dan pilih versi java yang diinginkan pada laman https://jdk.java.net/archive/

2. Lalu ekstrak file pada lokasi yang kita inginkan

3. Atur environment variable
    - tekan tombol windows
    - cari 'env' maka nanti akan muncul seperti ini<br/>
    ![Searching Environtment Image](/installation/windows/environment-search.jpg)
    - Klik Environment Variables<br/>
    ![Environtment Variables Image](/installation/windows/environment-variables.jpg)
    - Tambahkan environment variable baru dengan nama variable `JAVA_HOME`, dan nilai variable berupa lokasi direktori yang mengarah pada jdk yang kita install sebelumnya. Lokasi direktori adalah lokasi **sebelum `bin`** folder<br/>
    ![Menambahkan environment JAVA_HOME](/installation/windows/JAVA_HOME.jpg)
    - Tambahkan lokasi folder jdk bin pada `Path` di system variable<br/>
    ![Edit Path di system variable](/installation/windows/edit-path.jpg)
    ![tambahkan '%JAVA_HOME%/bin'](/installation/windows/jdk-bin-on-path.jpg)
4. Kemudian simpan dan pastikan berhasil dengan mencoba perintah 
    - `$ java --version`
    - kalau berhasil akan muncul detail versi java seperti 
        ```
        openjdk 17.0.2 2022-01-18
        OpenJDK Runtime Environment (build 17.0.2+8-86)
        OpenJDK 64-Bit Server VM (build 17.0.2+8-86, mixed mode, sharing)
        ```
        versi mungkin berbeda sesuai yang kita install sebelumnya
    - `$ javac --version`
    - kalau berhasil akan muncul detail versi java compiler seperti 
        ```
        javac 17.0.2
        ```

## Linux atau MacOs
1. Install dan pilih versi java yang diinginkan pada laman https://jdk.java.net/archive/

2. Atur environment variable 
    - Tambahkan lokasi jdk **(sebelum direktori `bin`)** yang kita install kedalam environment dengan nama `JAVA_HOME`
    - Tambahkan lokasi jdk bin pada environment `PATH` 
    - Dua tahapan diatas bisa dilakukan dengan menambahkan baris berikut pada `.bashrc` atau `.profile` atau `.zshrc`
        ```sh
        export JAVA_HOME="/lokasi/ke/jdk/yang/kita/simpan"
        export PATH="$JAVA_HOME/bin:$PATH"
        ```

3. Pastikan dengan mencoba perintah 
    - `$ java --version`
    - kalau berhasil akan muncul detail versi java seperti 
        ```
        openjdk 17.0.2 2022-01-18
        OpenJDK Runtime Environment (build 17.0.2+8-86)
        OpenJDK 64-Bit Server VM (build 17.0.2+8-86, mixed mode, sharing)
        ```
        versi mungkin berbeda sesuai yang kita install sebelumnya
    - `$ javac --version`
    - kalau berhasil akan muncul detail versi java compiler seperti 
        ```
        javac 17.0.2
        ```