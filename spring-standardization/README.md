# Spring Standardization 🍃🍃🍃
Sebuah dokumentasi untuk menyesuaikan gaya penggunaan Spring menggunakan bahasa Java

## Why Spring? [^](#)
#### Reference: [spring.io/why-spring](https://spring.io/why-spring)
### 1. Spring is everywhere [^](#)
&emsp;&emsp;&emsp;_Library_ Spring yang _flexible_ dipercaya oleh developer seluruh dunia. Spring menghadirkan pengalaman menyenangkan bagi jutaan pengguna sehari-hari, baik itu streaming TV, belanja online, atau banyak solusi inovatif lainnya. Spring jug amendapat kontribusi dari semua nama besar di bidang teknologi, termasuk **Alibaba**, **Amazon**, **Google**, **Microsoft**, dan banyak lagi
### 2. Spring is flexible [^](#)
&emsp;&emsp;&emsp;Kumpulan _extensions_ dan _Library third party_ yang fleksibel dan komprehensif dari Spring memungkinkan _developer_ untuk membangun hampir semua jenis aplikasi yang dapat dibayangkan. Pada intinya, fitur _Inversion of Control_ (IoC) dan _Dependency Injection_ (DI) dari Spring Framework menyediakan dasar untuk berbagai macam fitur dan fungsionalitas. Baik Anda sedang membangun _microservice_ berbasis cloud yang aman dan responsif untuk web, atau aliran data streaming yang kompleks untuk perusahaan, Spring memiliki alat yang dapat membantu.
### 3. Spring is productive [^](#)
&emsp;&emsp;&emsp;Spring boot menyederhanakan pemrograman java secara drastis. Spring Boot menggabungkan kebutuhan seperti konteks aplikasi dan server web yang terkonfigurasi otomatis, untuk membuat pengembangan _microservice_ menjadi sangat mudah. Untuk lebih cepat lagi, Anda dapat menggabungkan Spring Boot dengan kumpulan _library_, server, pola, dan _template_ pendukung yang kaya dari Spring Cloud, untuk dengan aman menerapkan seluruh arsitektur berbasis _microservice_ ke cloud, dalam waktu singkat.
### 4. Spring is fast [^](#)
&emsp;&emsp;&emsp;Para _developer_ Spring sangat perduli dengan kinerja. Dengan Spring, secara _default_ Anda akan melihat _startup_ yang cepat, _shutdown_ yang cepat, dan eksekusi yang dioptimalkan. Semakin meningkat, proyek spring juga mendukung model pemrograman reaktif (non-blocking) untuk efisiensi yang lebih besar. Produktivitas _developer_ adalah kekuatan utama Spring. Spring Boot membantu _developer_ membangun aplikasi dengan mudah dan dengan lebih sedikit pekerjaan dibandingkan paradiga kompetitor lainnya. Server web tertanam (Embedded web servers_), _auto-configuration, dan "_fat jars_" membantu anda memulai dengan cepat, dan inovasi seperti LiveReload dalam Spring DevTools berarti _developer_ dapat mengiterasi lebih cepat daripada sebelumnya. Anda bahkan dapat memulai proyek Spring baru dalam hitungan detik, dengan Spring Initializr di [start.spring.io](https://start.spring.io)
### 5. Spring is secure [^](#)
&emsp;&emsp;&emsp;Spring memiliki catatan yang terbukti dalam menangani masalah keamanan dengan cepat dan bertanggung jawab. Para kontributor Spring bekerja dengan profesional keamanan untuk memperbaiki dan menguji kerentanan yang dilaporkan. Ketergantungan pihak ketiga (_third party_) juga dipantau secara ketat, dan pembaruan berkala diberikan untuk membantu menjaga data dan aplikasi Anda seaman mungkin. Selain itu, Spring Security membuatnya lebih mudah bagi Anda untuk mengintegrasikan skema keamanan standar industri dan memberikan solusi yang dapat dipercaya yang secara default aman.
### 6. Spring is supportive [^](#)
&emsp;&emsp;&emsp;Komunitas Spring sangat besar, global, beragam, dan melibatkan orang dari segala usia dan kemapuan, mulai dari pemula hingga profesional berpengalaman. Tidak peduli di mana Anda berada dalam perjalanan Anda, Anda dapat menemukan dukungan dan sumber daya yang Anda butuhkan untuk membantu Anda mencapai tingkat berikutnya: panduan cepat, video, pertemuan, dukungan, atau bahkan pelatihan formal dan sertifikasi

### What Spring can do ? [^](#)
- Microservices 
- Reactive
- Cloud
- Web apps
- Serverless
- Event Driven
- Batch

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

## Kapan Harus Menggunakan Spring? [^]()

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

## Komponen [^](#)
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

### Perbedaan menggunakan Java Lombok, dengan Manual Java
1. Getter Setter
    - Dengan Java Lombok

        ```java
        import lombok.AccessLevel;
        import lombok.Getter;
        import lombok.Setter;

        public class GetterSetterExample {
            /**
             * Age of the person.
             * 
             * @param age New value for this person's age.
             * @return The current value of this person's age.
             */
            @Getter @Setter private int age = 10;
            
            /**
             * Name of the person.
             * -- SETTER --
             * Changes the name of this person.
             * 
             * @param name The new value.
             */
            @Setter(AccessLevel.PROTECTED) private String name;
            
            @Override public String toString() {
                return String.format("%s (age: %d)", name, age);
            }
        }
        ```
    - Manual Java
        ```java
        public class GetterSetterExample {
        /**
        * Age of the person.
        */
        private int age = 10;

        /**
        * Name of the person.
        */
        private String name;
        
        @Override public String toString() {
            return String.format("%s (age: %d)", name, age);
        }
        
        /**
        * Age of the person.
        *
        * @return The current value of this person's age.
        */
        public int getAge() {
            return age;
        }
        
        /**
        * Age of the person. 
        *
        * @param age New value for this person's age.
        */
        public void setAge(int age) {
            this.age = age;
        }
        
        /**
        * Changes the name of this person.
        *
        * @param name The new value.
        */
        protected void setName(String name) {
            this.name = name;
        }
        }
        ```

2. Constructor
    - Dengan Java Lombok
        ```java
        import lombok.AccessLevel;
        import lombok.RequiredArgsConstructor;
        import lombok.AllArgsConstructor;
        import lombok.NonNull;

        @RequiredArgsConstructor(staticName = "of")
        @AllArgsConstructor(access = AccessLevel.PROTECTED)
        public class ConstructorExample<T> {
            private int x, y;
            @NonNull private T description;
            
            @NoArgsConstructor
            public static class NoArgsExample {
                @NonNull private String field;
            }
        }
        ```
    - Manual Java
        ```java
        public class ConstructorExample<T> {
            private int x, y;
            @NonNull private T description;
            
            private ConstructorExample(T description) {
                if (description == null) throw new NullPointerException("description");
                this.description = description;
            }
            
            public static <T> ConstructorExample<T> of(T description) {
                return new ConstructorExample<T>(description);
            }
            
            @java.beans.ConstructorProperties({"x", "y", "description"})
            protected ConstructorExample(int x, int y, T description) {
                if (description == null) throw new NullPointerException("description");
                this.x = x;
                this.y = y;
                this.description = description;
            }
            
            public static class NoArgsExample {
                @NonNull private String field;
                
                public NoArgsExample() {
                }
            }
        }
        ```
3. ToString
    - Dengan Java Lombok
        ```java
        import lombok.ToString;

        @ToString
        public class ToStringExample {
            private static final int STATIC_VAR = 10;
            private String name;
            private Shape shape = new Square(5, 10);
            private String[] tags;
            @ToString.Exclude private int id;
            
            public String getName() {
                return this.name;
            }
            
            @ToString(callSuper=true, includeFieldNames=true)
            public static class Square extends Shape {
                private final int width, height;
                
                public Square(int width, int height) {
                this.width = width;
                this.height = height;
                }
            }
        }
        ```
    - Manual Java
        ```java
        import java.util.Arrays;

        public class ToStringExample {
            private static final int STATIC_VAR = 10;
            private String name;
            private Shape shape = new Square(5, 10);
            private String[] tags;
            private int id;
            
            public String getName() {
                return this.name;
            }
            
            public static class Square extends Shape {
                private final int width, height;
                
                public Square(int width, int height) {
                this.width = width;
                this.height = height;
                }
                
                @Override public String toString() {
                return "Square(super=" + super.toString() + ", width=" + this.width + ", height=" + this.height + ")";
                }
            }
            
            @Override public String toString() {
                return "ToStringExample(" + this.getName() + ", " + this.shape + ", " + Arrays.deepToString(this.tags) + ")";
            }
        }
        ```
4. Equals And HashCode
    - Dengan Java Lombok
        ```java
        import lombok.EqualsAndHashCode;

        @EqualsAndHashCode
        public class EqualsAndHashCodeExample {
            private transient int transientVar = 10;
            private String name;
            private double score;
            @EqualsAndHashCode.Exclude private Shape shape = new Square(5, 10);
            private String[] tags;
            @EqualsAndHashCode.Exclude private int id;
            
            public String getName() {
                return this.name;
            }
            
            @EqualsAndHashCode(callSuper=true)
            public static class Square extends Shape {
                private final int width, height;
                
                public Square(int width, int height) {
                this.width = width;
                this.height = height;
                }
            }
        }
        ```
    - Manual Java
        ```java
        import java.util.Arrays;

        public class EqualsAndHashCodeExample {
            private transient int transientVar = 10;
            private String name;
            private double score;
            private Shape shape = new Square(5, 10);
            private String[] tags;
            private int id;
            
            public String getName() {
                return this.name;
            }
            
            @Override public boolean equals(Object o) {
                if (o == this) return true;
                if (!(o instanceof EqualsAndHashCodeExample)) return false;
                EqualsAndHashCodeExample other = (EqualsAndHashCodeExample) o;
                if (!other.canEqual((Object)this)) return false;
                if (this.getName() == null ? other.getName() != null : !this.getName().equals(other.getName())) return false;
                if (Double.compare(this.score, other.score) != 0) return false;
                if (!Arrays.deepEquals(this.tags, other.tags)) return false;
                return true;
            }
            
            @Override public int hashCode() {
                final int PRIME = 59;
                int result = 1;
                final long temp1 = Double.doubleToLongBits(this.score);
                result = (result*PRIME) + (this.name == null ? 43 : this.name.hashCode());
                result = (result*PRIME) + (int)(temp1 ^ (temp1 >>> 32));
                result = (result*PRIME) + Arrays.deepHashCode(this.tags);
                return result;
            }
            
            protected boolean canEqual(Object other) {
                return other instanceof EqualsAndHashCodeExample;
            }
            
            public static class Square extends Shape {
                private final int width, height;
                
                public Square(int width, int height) {
                    this.width = width;
                    this.height = height;
                }
                
                @Override public boolean equals(Object o) {
                    if (o == this) return true;
                    if (!(o instanceof Square)) return false;
                    Square other = (Square) o;
                    if (!other.canEqual((Object)this)) return false;
                    if (!super.equals(o)) return false;
                    if (this.width != other.width) return false;
                    if (this.height != other.height) return false;
                    return true;
                }
                
                @Override public int hashCode() {
                    final int PRIME = 59;
                    int result = 1;
                    result = (result*PRIME) + super.hashCode();
                    result = (result*PRIME) + this.width;
                    result = (result*PRIME) + this.height;
                    return result;
                }
                
                protected boolean canEqual(Object other) {
                    return other instanceof Square;
                }
            }
        }
        ```
5. Builder
    - Dengan Java Lombok
    ```java
    import lombok.Builder;
    import lombok.Singular;
    import java.util.Set;

    @Builder
    public class BuilderExample {
        @Builder.Default private long created = System.currentTimeMillis();
        private String name;
        private int age;
        @Singular private Set<String> occupations;
    }
    ```
    - Manual Java
    ```java
    import java.util.Set;

    public class BuilderExample {
        private long created;
        private String name;
        private int age;
        private Set<String> occupations;
        
        BuilderExample(String name, int age, Set<String> occupations) {
            this.name = name;
            this.age = age;
            this.occupations = occupations;
        }
        
        private static long $default$created() {
            return System.currentTimeMillis();
        }
        
        public static BuilderExampleBuilder builder() {
            return new BuilderExampleBuilder();
        }
        
        public static class BuilderExampleBuilder {
            private long created;
            private boolean created$set;
            private String name;
            private int age;
            private java.util.ArrayList<String> occupations;
            
            BuilderExampleBuilder() {
            }
            
            public BuilderExampleBuilder created(long created) {
                this.created = created;
                this.created$set = true;
                return this;
            }
            
            public BuilderExampleBuilder name(String name) {
                this.name = name;
                return this;
            }
            
            public BuilderExampleBuilder age(int age) {
                this.age = age;
                return this;
            }
            
            public BuilderExampleBuilder occupation(String occupation) {
                if (this.occupations == null) {
                    this.occupations = new java.util.ArrayList<String>();
                }
                
                this.occupations.add(occupation);
                return this;
            }
            
            public BuilderExampleBuilder occupations(Collection<? extends String> occupations) {
                if (this.occupations == null) {
                    this.occupations = new java.util.ArrayList<String>();
                }

                this.occupations.addAll(occupations);
                return this;
            }
            
            public BuilderExampleBuilder clearOccupations() {
                if (this.occupations != null) {
                    this.occupations.clear();
                }
                
                return this;
            }

            public BuilderExample build() {
                // complicated switch statement to produce a compact properly sized immutable set omitted.
                Set<String> occupations = ...;
                return new BuilderExample(created$set ? created : BuilderExample.$default$created(), name, age, occupations);
            }
                
            @java.lang.Override
            public String toString() {
                return "BuilderExample.BuilderExampleBuilder(created = " + this.created + ", name = " + this.name + ", age = " + this.age + ", occupations = " + this.occupations + ")";
            }
        }
    }
    ```
6. SneakyThrows
    - Dengan Java Lombok
        ```java
        import lombok.SneakyThrows;

        public class SneakyThrowsExample implements Runnable {
            @SneakyThrows(UnsupportedEncodingException.class)
            public String utf8ToString(byte[] bytes) {
                return new String(bytes, "UTF-8");
            }
            
            @SneakyThrows
            public void run() {
                throw new Throwable();
            }
        }
        ```
    - Manual Java
        ```java
        import lombok.Lombok;

        public class SneakyThrowsExample implements Runnable {
            public String utf8ToString(byte[] bytes) {
                try {
                    return new String(bytes, "UTF-8");
                } catch (UnsupportedEncodingException e) {
                    throw Lombok.sneakyThrow(e);
                }
            }
            
            public void run() {
                try {
                    throw new Throwable();
                } catch (Throwable t) {
                    throw Lombok.sneakyThrow(t);
                }
            }
        }
        ```
7. Synchronized
    - Dengan Java Lombok
        ```java
        import lombok.Synchronized;

        public class SynchronizedExample {
            private final Object readLock = new Object();
            
            @Synchronized
            public static void hello() {
                System.out.println("world");
            }
            
            @Synchronized
            public int answerToLife() {
                return 42;
            }
            
            @Synchronized("readLock")
            public void foo() {
                System.out.println("bar");
            }
        }
        ```
    - Manual Java
        ```java
        public class SynchronizedExample {
            private static final Object $LOCK = new Object[0];
            private final Object $lock = new Object[0];
            private final Object readLock = new Object();
            
            public static void hello() {
                synchronized($LOCK) {
                    System.out.println("world");
                }
            }
            
            public int answerToLife() {
                synchronized($lock) {
                    return 42;
                }
            }
            
            public void foo() {
                synchronized(readLock) {
                    System.out.println("bar");
                }
            }
        }
        ```

Dan masih banyak lagi yang lainnya sehingga dapat mempermudah dan mempercepat kita dalam proses development. [Click here for the references !](https://projectlombok.org/)

## ORM - Java Persistence API (JPA) [^](#)

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

## JDBC Template [^](#)
Sebagai opsi lain dari JPA. Digunakan ketika dirasa butuh yang lebih cepat

Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jdbc</artifactId>
</dependency>
```

## Scheduler
Scheduler adalah komponen penting yang digunakan untuk mengatur eksekusi tugas atau proses secara otomatis berdasarkan jadwal tertentu. Scheduler dapat digunakan untuk menjalankan berbagai jenis tugas, seperti pemrosesan batch, pembaruan database, atau tugas pemeliharaan lainnya. Jadi, dalam konteks back-end, scheduler adalah alat yang sangat berguna untuk membantu mengelola dan mengotomatisasi tugas-tugas yang perlu dijalankan secara berkala atau pada waktu tertentu.

1. Quartz Scheduler
<br>Ini adalah _scheduling framework_ yang memungkinkan Anda untuk menjalankan sesuatu setiap jam atau setiap Jumat terakhir dalam sebulan. Quartz menyediakan _scheduling framework_ dan _job framework_ (semisal Anda tidak ingin menggunakan _Spring batch jobs_).

2. Spring Batch
<br>Ini adalah _framework_ yang mendefinisikan “sesuatu” yang akan dieksekusi. Anda dapat mendefinisikan pekerjaan, yang terdiri dari langkah-langkah. Biasanya, langkah adalah sesuatu yang terdiri dari pembaca item, prosesor item opsional, dan penulis item, tetapi Anda dapat mendefinisikan langkah kustom. Spring Batch menyediakan fungsionalitas untuk memproses volume data yang besar.

3. Spring Scheduler
<br> Ini adalah lapisan abstraksi yang ditulis untuk menyembunyikan implementasi Executors di berbagai JDK seperti Java SE 1.4, Java SE 5 dan lingkungan Java EE, yang memiliki implementasi spesifik mereka sendiri.

## Routing
Routing adalah pemetaan permintaan HTTP ke metode tertentu pada kelas kontroler. Dengan kata lain, routing memungkinkan aplikasi untuk menentukan bagaimana permintaan dari klien harus ditangani.

Cara routing pada Spring _framework_, kita dapat menggunakan Spring Boot dan Spring WebFlux.

### Spring Boot vs Spring WebFlux
**Spring Boot** biasanya digunakan dengan Spring MVC, yang merupakan framework berbasis servlet untuk mengembangkan aplikasi web. Dalam konteks ini, routing biasanya dilakukan dengan anotasi seperti @RequestMapping atau @GetMapping dan @PostMapping pada metode dalam kelas kontroler

**Spring WebFlux** adalah bagian dari Spring 5 dan dirancang untuk membangun aplikasi web reaktif dan non-blocking. Ini menggunakan model pemrograman yang berbeda yang didasarkan pada Reactive Streams. Dalam WebFlux, Anda dapat mendefinisikan routing menggunakan RouterFunction. Ini memungkinkan Anda untuk membuat routing yang lebih fungsional dan fleksibel.

#### Keunggulan dan kekurangan
- **Spring Boot**
    - Keunggulan :
        - Dapat menciptakan aplikasi Spring yang berdiri sendiri.

        - Menyediakan fitur Embed Tomcat, Jetty, dan Undertow secara langsung, sehingga Anda tidak perlu menerapkan file WAR.

        - Menyediakan dependensi ‘starter’ yang dapat membantu konfigurasi dapat dilakukan dengan lebih sederhana.

        - Mengkonfigurasikan pustaka Spring dan pihak ketiga secara otomatis jika memungkinkan.

    - Kekurangan :
        - Karena gaya yang _opinionated_, ketika ada satu cara yang sudah teruji dan terbukti untuk mengembangkan aplikasi, hal ini mengambil banyak kontrol dari tangan pengembang.

- **Spring WebFlux**
    - Keunggulan :

        - Spring WebFlux adalah _framework_ web reaktif berdasarkan lapisan HTTP reaktif; aplikasi semacam ini dapat diterapkan pada Netty atau Undertow (dengan adapter asli) atau Jetty/Tomcat/semua wadah Servlet 3.1 (berkat adapter Servlet 3.1).

        - Pendekatan ini dapat bermanfaat untuk efisiensi dan skalabilitas untuk beban kerja yang berurusan dengan banyak latensi dan konkurensi.
    - Kekurangan :
        - Memerlukan pemahaman yang lebih dalam tentang pemrograman reaktif dan paradigma non-blocking, yang bisa menjadi tantangan bagi beberapa pengembang.

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