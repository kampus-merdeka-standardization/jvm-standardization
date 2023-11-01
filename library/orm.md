## ORM - Java Persistence API (JPA)

Java Persistence API (JPA) adalah spesifikasi Java yang digunakan untuk mengakses, mengelola, dan mempertahankan data antara objek Java dan database relasional. JPA dianggap sebagai pendekatan standar untuk Object Relational Mapping.

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

Karena JPA merupakan spesifikasi, JPA tidak melakukan operasi apa pun sendiri, sehingga memerlukan implementasi. Beberapa implementasi ORM yang populer pada kalangan java adalah :

1. **Hibernate** adalah implementasi JPA yang paling _mature_ dan banyak digunakan dengan komunitas besar dan dokumentasi yang lengkap. Hibernate juga menyediakan beberapa fitur tambahan yang tidak termasuk dalam standar JPA, seperti kueri kriteria, kueri SQL asli, filter, interceptor, dan envers. Namun, Hibernate memiliki beberapa masalah kompatibilitas dengan spesifikasi JPA, terutama di bidang sintaks JPQL, pewarisan entitas, dan strategi penguncian.

2. **EclipseLink** adalah implementasi referensi dari JPA, yang berarti paling sesuai dengan standar dan mengikuti pembaruan terbaru. EclipseLink juga mendukung beberapa fitur canggih yang tidak tersedia di Hibernate, seperti memanggil fungsi SQL asli dalam kueri JPQL, menggunakan unit persistensi dinamis, dan memetakan objek ke XML atau JSON. Namun, EclipseLink kurang matang daripada Hibernate dan memiliki komunitas dan dokumentasi yang lebih sedikit. Beberapa pengguna juga melaporkan bahwa EclipseLink memiliki kinerja dan penanganan kesalahan yang lebih buruk daripada Hibernate.

3. **OpenJPA** adalah implementasi open source lain dari JPA, yang dikembangkan oleh Apache. OpenJPA mirip dengan EclipseLink dalam hal kesesuaian dengan spesifikasi JPA, tetapi memiliki fitur dan ekstensi yang lebih sedikit daripada Hibernate dan EclipseLink. OpenJPA terutama digunakan oleh IBM WebSphere Application Server dan Apache Geronimo, tetapi juga dapat diintegrasikan dengan kerangka kerja lain seperti Spring. OpenJPA dianggap stabil dan andal, tetapi kurang populer dan didukung daripada Hibernate dan EclipseLink.

4. **DataNucleus** adalah implementasi JPA yang mendukung berbagai jenis penyimpanan data, tidak hanya database relasional, tetapi juga NoSQL, spreadsheet, XML, dan lainnya. DataNucleus fleksibel dan dapat diperluas, tetapi mungkin memiliki kinerja dan kompatibilitas yang lebih rendah daripada implementasi lain yang fokus pada database relasional.

5. **ObjectDB** adalah implementasi JPA yang berbasis database objek, yang berarti tidak memerlukan pemetaan objek-relasional dan dapat menyimpan objek Java secara langsung. ObjectDB cepat dan mudah digunakan, tetapi mungkin tidak cocok untuk aplikasi yang perlu mengakses atau memanipulasi data secara relasional.

6. **EBean** adalah implementasi JPA yang ringan dan sederhana, menawarkan kinerja tinggi dan kemudahan penggunaan. EBean tidak mendukung beberapa fitur JPA seperti pemetaan pewarisan, objek tertanam, atau kueri bernama, tetapi memiliki API yang lancar dan penyetelan kueri otomatis.

### Kelebihan serta kekurangan tiap ORM

1. **Hibernate**: Keunggulannya adalah memiliki komunitas besar, dokumentasi lengkap, dan fitur tambahan yang tidak termasuk dalam standar JPA. Kekurangannya adalah memiliki masalah kompatibilitas dengan spesifikasi JPA, terutama di bidang sintaks JPQL, pewarisan entitas, dan strategi penguncian.

2. **EclipseLink**: Keunggulannya adalah paling sesuai dengan standar JPA dan mengikuti pembaruan terbaru. EclipseLink juga mendukung fitur canggih yang tidak tersedia di Hibernate, seperti memanggil fungsi SQL asli dalam kueri JPQL, menggunakan unit persistensi dinamis, dan memetakan objek ke XML atau JSON. Kekurangannya adalah kurang matang daripada Hibernate dan memiliki komunitas dan dokumentasi yang lebih sedikit. Beberapa pengguna juga melaporkan bahwa EclipseLink memiliki kinerja dan penanganan kesalahan yang lebih buruk daripada Hibernate.

3. **OpenJPA**: Keunggulannya adalah mirip dengan EclipseLink dalam hal kesesuaian dengan spesifikasi JPA, tetapi memiliki fitur dan ekstensi yang lebih sedikit daripada Hibernate dan EclipseLink. OpenJPA terutama digunakan oleh IBM WebSphere Application Server dan Apache Geronimo, tetapi juga dapat diintegrasikan dengan kerangka kerja lain seperti Spring. Kekurangannya adalah kurang populer dan didukung daripada Hibernate dan EclipseLink.

4. **DataNucleus**: Keunggulannya adalah mendukung berbagai jenis penyimpanan data, tidak hanya database relasional, tetapi juga NoSQL, spreadsheet, XML, dan lainnya. DataNucleus fleksibel dan dapat diperluas, tetapi mungkin memiliki kinerja dan kompatibilitas yang lebih rendah daripada implementasi lain yang fokus pada database relasional.

5. **ObjectDB**: Keunggulannya adalah berbasis database objek, yang berarti tidak memerlukan pemetaan objek-relasional dan dapat menyimpan objek Java secara langsung. ObjectDB cepat dan mudah digunakan, tetapi mungkin tidak cocok untuk aplikasi yang perlu mengakses atau memanipulasi data secara relasional.

6. **EBean**: Keunggulannya adalah ringan dan sederhana, menawarkan kinerja tinggi dan kemudahan penggunaan. EBean tidak mendukung beberapa fitur JPA seperti pemetaan pewarisan, objek tertanam, atau kueri bernama, tetapi memiliki API yang lancar dan penyetelan kueri otomatis.

### Rate :

| Komponen | Hibernate | EclipseLink | OpenJPA | DataNucleus | ObjectDB | EBean |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| maintenance | 4 | 4 | 2 | 3 | 4 | 3 |
| Reputable | 4 | 3 | 4 | 3 | 3 | 3 |
| Compatibility | 4 | 3 | 3 | 3 | 4 | 3 |
| Community | 4 | 4 | 4 | 3 | 3 | 3
| Documentation | 4 | 4 | 4 | 4 | 3 | 4 |
| Licensing | 4 | 4 | 4 | 4 | 3 | 4 |
| Extensible | 4 | 4 | 3 | 4 | 4 | 4 |
| Size | 3 | 2 | 3 | 2 | 3 | 3 |
| Total Score | 31 | 28 | 27 | 26 | 27 | 27 |
| Average Score | 3.875 | 3.5 | 3.375 | 3.25 | 3.375 | 3.375 |