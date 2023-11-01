# Spring Framework

## Sejarah Singkat
Spring Framework adalah sebuah framework open source berbasis Java yang menyediakan infrastruktur yang komprehensif untuk mengembangkan aplikasi Java dengan mudah dan cepat. Spring pertama kali ditulis dan dirilis oleh Rod Johnson dengan lisensi Apache 2.0 pada bulan Juni 2003.

Framework ini membantu programmer dalam pengembangan aplikasi dengan build yang sederhana, portable, cepat dan sistem berbasis JVM yang fleksibel. Spring dapat digunakan untuk melakukan pengaturan deklarasi manajemen transaksi, remote access dengan menggunakan RMI atau layanan web lainnya, fasilitas mailing, dan beragam opsi untuk pengaturan data ke database.

Dengan menggunakan Spring Framework, developer dapat membuat aplikasi enterprise ataupun web. Selain itu juga, para developer dapat membuat aplikasi untuk keamanan dan aplikasi yang terkait dengan big data1. Spring termasuk portabel karena aplikasi yang dikembangkan dapat berjalan pada JVM manapun

## Why Spring?
**References:** [spring.io/why-spring](https://spring.io/why-spring)
### 1. Spring is everywhere
&emsp;&emsp;&emsp;_Library_ Spring yang _flexible_ dipercaya oleh developer seluruh dunia. Spring menghadirkan pengalaman menyenangkan bagi jutaan pengguna sehari-hari, baik itu streaming TV, belanja online, atau banyak solusi inovatif lainnya. Spring jug amendapat kontribusi dari semua nama besar di bidang teknologi, termasuk **Alibaba**, **Amazon**, **Google**, **Microsoft**, dan banyak lagi
### 2. Spring is flexible
&emsp;&emsp;&emsp;Kumpulan _extensions_ dan _Library third party_ yang fleksibel dan komprehensif dari Spring memungkinkan _developer_ untuk membangun hampir semua jenis aplikasi yang dapat dibayangkan. Pada intinya, fitur _Inversion of Control_ (IoC) dan _Dependency Injection_ (DI) dari Spring Framework menyediakan dasar untuk berbagai macam fitur dan fungsionalitas. Baik Anda sedang membangun _microservice_ berbasis cloud yang aman dan responsif untuk web, atau aliran data streaming yang kompleks untuk perusahaan, Spring memiliki alat yang dapat membantu.
### 3. Spring is productive
&emsp;&emsp;&emsp;Spring boot menyederhanakan pemrograman java secara drastis. Spring Boot menggabungkan kebutuhan seperti konteks aplikasi dan server web yang terkonfigurasi otomatis, untuk membuat pengembangan _microservice_ menjadi sangat mudah. Untuk lebih cepat lagi, Anda dapat menggabungkan Spring Boot dengan kumpulan _library_, server, pola, dan _template_ pendukung yang kaya dari Spring Cloud, untuk dengan aman menerapkan seluruh arsitektur berbasis _microservice_ ke cloud, dalam waktu singkat.
### 4. Spring is fast
&emsp;&emsp;&emsp;Para _developer_ Spring sangat perduli dengan kinerja. Dengan Spring, secara _default_ Anda akan melihat _startup_ yang cepat, _shutdown_ yang cepat, dan eksekusi yang dioptimalkan. Semakin meningkat, proyek spring juga mendukung model pemrograman reaktif (non-blocking) untuk efisiensi yang lebih besar. Produktivitas _developer_ adalah kekuatan utama Spring. Spring Boot membantu _developer_ membangun aplikasi dengan mudah dan dengan lebih sedikit pekerjaan dibandingkan paradiga kompetitor lainnya. Server web tertanam (_Embedded web servers_), _auto-configuration_, dan "_fat jars_" membantu anda memulai dengan cepat, dan inovasi seperti LiveReload dalam Spring DevTools berarti _developer_ dapat mengiterasi lebih cepat daripada sebelumnya. Anda bahkan dapat memulai proyek Spring baru dalam hitungan detik, dengan Spring Initializr di [start.spring.io](https://start.spring.io)
### 5. Spring is secure
&emsp;&emsp;&emsp;Spring memiliki catatan yang terbukti dalam menangani masalah keamanan dengan cepat dan bertanggung jawab. Para kontributor Spring bekerja dengan profesional keamanan untuk memperbaiki dan menguji kerentanan yang dilaporkan. Ketergantungan pihak ketiga (_third party_) juga dipantau secara ketat, dan pembaruan berkala diberikan untuk membantu menjaga data dan aplikasi Anda seaman mungkin. Selain itu, Spring Security membuatnya lebih mudah bagi Anda untuk mengintegrasikan skema keamanan standar industri dan memberikan solusi yang dapat dipercaya yang secara default aman.
### 6. Spring is supportive
&emsp;&emsp;&emsp;Komunitas Spring sangat besar, global, beragam, dan melibatkan orang dari segala usia dan kemapuan, mulai dari pemula hingga profesional berpengalaman. Tidak peduli di mana Anda berada dalam perjalanan Anda, Anda dapat menemukan dukungan dan sumber daya yang Anda butuhkan untuk membantu Anda mencapai tingkat berikutnya: panduan cepat, video, pertemuan, dukungan, atau bahkan pelatihan formal dan sertifikasi

### What Spring can do ?
- Microservices 
- Reactive
- Cloud
- Web apps
- Serverless
- Event Driven
- Batch 

## Kelebihan dan Kekurangan Spring Framework

### Kelebihan
1. ***Flexibility*** : Menawarkan perpustakaan fleksibel untuk membantu pengembang. Pengguna dapat memilih antara anotasi berbasis XML atau Java mengenai konfigurasi. Fitur IoC dan DI juga hadir untuk memberikan fungsionalitas dan fitur yang luas.

2. ***Portability***: Ini adalah kerangka kerja yang portabel karena kita dapat menggunakan sisi klien dalam logika bisnis aplikasi swing dan sisi server dalam aplikasi web/EJB.

3. ***Consistent configuration***: Ini juga membantu dalam menyediakan cara konfigurasi yang konsisten. Ini menawarkan konfigurasi terpisah untuk mempermudah pengembang.

4. ***Fast delivery***: Ini juga merupakan alasan _startup_ dan _shutdown_ cepat. Ini menghasilkan peningkatan kinerja dan membuat _framework_ ini cepat. Eksekusi yang dioptimalkan yang ditawarkan oleh Spring juga membantu dalam hal ini.

5. ***Secure***:  _framework_ ini menyediakan pembaruan yang sering untuk membuat data dan aplikasi kita lebih aman. Kita juga dapat menggunakan _Spring security framework_ dalam hal ini.

6. ***Simpler testing***: Para pengembang dapat melakukan pengujian dengan mudah berkat _framework_ Spring. Ini memungkinkan karena penggunaan _dependency injection_

7. ***AOP module***: Para pengembang dapat mencapai beberapa unit kompilasi. Mereka juga dapat memiliki _loader_ kelas yang terpisah

### Kekurangan
1. ***Fewer guidelines***: Tidak ada prosedur yang tepat dalam dokumentasi Spring untuk mengatasi ancaman seperti XSS atau cross-site scripting. Informasi dan pedoman yang berguna harus disediakan untuk menghentikan peretas dari mengakses dan merusak aplikasi Anda.

2. ***Complexity***: Ini cukup kompleks untuk bekerja dengan Spring. Para pengembang harus memiliki keterampilan dan keahlian yang lebih relevan untuk menggunakan _framework_ ini.

3. ***Hard to learn***: Jika Anda tidak memiliki pengalaman dalam pengembangan, cukup sulit bagi Anda untuk mempelajari Spring. Hal ini disebabkan oleh penggabungan teknik pemrograman terbaru dalam kerangka kerja ini.

4. ***Uses XML***: Kita memerlukan banyak XML saat mengembangkan aplikasi Spring. Ini juga bisa menjadi masalah bagi para pengembang.

5. ***Parallel mechanism***: Para pengembang dapat memperoleh banyak opsi. Ini dapat membantu para pengembang tetapi juga dapat menjadi sumber kebingungan. Para pengembang dapat menghadapi masalah dalam memilih mekanisme yang tepat dan ini dapat mengakibatkan pengambilan keputusan yang salah. Pilihan yang salah ini bisa menyebabkan penundaan besar dalam pengembangan aplikasi.

[_reference_](https://www-educative-io.translate.goog/answers/what-are-java-spring-framework-advantages-and-disadvantages?_x_tr_sl=en&_x_tr_tl=id&_x_tr_hl=id&_x_tr_pto=tc&_x_tr_hist=true)

## Kapan Harus Menggunakan Spring?

1. ***Aplikasi Berbasis Web***: Spring Framework sangat cocok untuk pengembangan aplikasi web, baik itu aplikasi monolitik tradisional atau mikroservis. Anda dapat menggunakan Spring MVC untuk mengembangkan aplikasi web dengan mudah, yang menyediakan kontroler, model, dan tampilan untuk mengelola permintaan HTTP.

2. ***Aplikasi Berbasis Mikroservis***: Spring Boot adalah pilihan populer untuk pengembangan mikroservis. Ini memungkinkan Anda untuk dengan cepat membuat dan menjalankan layanan mikro yang independen, dan Spring Cloud menyediakan alat untuk manajemen, koordinasi, dan keamanan layanan mikro.

3. ***Aplikasi Berbasis Data***: Spring menyediakan dukungan yang kuat untuk berbagai teknologi penyimpanan data, termasuk Hibernate, JPA (Java Persistence API), JDBC (Java Database Connectivity), dan Redis. Ini memudahkan pengembangan aplikasi yang berinteraksi dengan basis data.

4. ***Manajemen Transaksi***: Spring menyediakan fasilitas untuk manajemen transaksi, baik melalui pemrograman programatik maupun dengan deklaratif menggunakan anotasi. Ini berguna dalam pengembangan aplikasi yang melibatkan operasi transaksional, seperti operasi database yang transaksional.

5. ***Keamanan Aplikasi***: Spring Security adalah bagian dari ekosistem Spring yang digunakan untuk mengamankan aplikasi. Ini memungkinkan Anda mengimplementasikan autentikasi, otorisasi, dan kontrol akses dengan mudah.

6. ***Pengujian***: Spring Framework menyediakan dukungan yang baik untuk pengujian unit dan integrasi. Anda dapat dengan mudah menguji berbagai komponen aplikasi Anda dengan bantuan kerangka kerja pengujian seperti JUnit.

7. ***Messaging dan Integrasi***: Spring Integration memungkinkan integrasi mudah dengan sistem pesan dan integrasi dengan berbagai sistem eksternal, seperti layanan web, layanan REST, dan banyak lagi.

8. ***Pengembangan Aplikasi Berbasis RESTful***: Jika Anda mengembangkan layanan web RESTful, Spring MVC dapat digunakan untuk membuat endpoint REST dengan cepat. Ini memungkinkan Anda untuk membangun aplikasi berbasis REST yang responsif dan scalable.

9. ***Aplikasi Berbasis Batch***: Spring Batch adalah bagian dari Spring Framework yang digunakan untuk mengembangkan aplikasi batch. Ini cocok untuk pekerjaan berulang yang perlu dijadwalkan dan dijalankan secara teratur.

10. ***Aplikasi Cloud***: Spring Framework memiliki dukungan yang baik untuk pengembangan aplikasi cloud-native. Anda dapat menggunakan Spring Cloud untuk manajemen mikroservis dan Spring Cloud Data Flow untuk mengelola aliran data.

11. ***Aplikasi Real-time***: Jika Anda perlu mengembangkan aplikasi real-time, Anda dapat menggunakan Spring Framework dengan WebSocket atau integrasi dengan teknologi lain seperti Apache Kafka.

_Spring Framework_ adalah alat yang sangat fleksibel, jadi _framework_ ini dapat digunakan dalam berbagai konteks pengembangan perangkat lunak, mulai dari aplikasi sederhana hingga yang sangat kompleks.

## Penilaian Komponen
| Komponen | Spring |
| :---: | :---: |
| maintenance | 4 |
| Reputable | 4 |
| Compatibility | 4 |
| Community | 4 |
| Documentation | 4 |
| Licensing | 4 |
| Extensible | 4 |
| Size | 3 |
| Total Score| 31 |
| Average Score | 3.875 |