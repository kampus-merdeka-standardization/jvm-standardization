# Routing
Routing adalah pemetaan permintaan HTTP ke metode tertentu pada kelas kontroler. Dengan kata lain, routing memungkinkan aplikasi untuk menentukan bagaimana permintaan dari klien harus ditangani.

Cara routing pada Spring _framework_, kita dapat menggunakan Spring Boot dan Spring WebFlux.

## Spring Boot vs Spring WebFlux
**Spring Boot** biasanya digunakan dengan Spring MVC, yang merupakan framework berbasis servlet untuk mengembangkan aplikasi web. Dalam konteks ini, routing biasanya dilakukan dengan anotasi seperti `@RequestMapping` atau `@GetMapping` dan `@PostMapping` pada metode dalam kelas kontroler

**Spring WebFlux** adalah bagian dari Spring 5 dan dirancang untuk membangun aplikasi web reaktif dan non-blocking. Ini menggunakan model pemrograman yang berbeda yang didasarkan pada Reactive Streams. Dalam WebFlux, Anda dapat mendefinisikan routing menggunakan RouterFunction. Ini memungkinkan Anda untuk membuat routing yang lebih fungsional dan fleksibel.

## _Use-Case_
**Spring Boot (Spring MVC)** Cocok untuk aplikasi yang memanfaatkan arsitektur berbasis blok dan sinkronisasi, di mana setiap permintaan diproses satu per satu. Ini adalah pendekatan yang baik untuk aplikasi yang tidak memerlukan skalabilitas tinggi atau penanganan permintaan simultan.

**Spring WebFlux** Cocok untuk aplikasi yang memerlukan penanganan permintaan _non-blocking_ dan asinkron, di mana banyak permintaan dapat diproses secara bersamaan. Ini adalah pendekatan yang baik untuk aplikasi dengan beban tinggi atau aplikasi yang memerlukan penanganan permintaan _real-time_.

## Kelebihan dan kekurangan
### Spring Boot (Spring MVC)
**Kelebihan** :
1. **Pendekatan Berbasis Anotasi**: Spring MVC menggunakan pendekatan berbasis anotasi untuk mendefinisikan rute, yang membuatnya lebih mudah dipahami dan digunakan bagi banyak pengembang.

2. **Maturitas dan Stabilitas**: Spring MVC telah ada lebih lama dan memiliki ekosistem yang matang dengan banyak dokumentasi, tutorial, dan contoh kode.

3. **Integrasi dengan Teknologi Lain**: Spring MVC memiliki integrasi yang baik dengan teknologi lain seperti JPA, Hibernate, dan banyak lagi.

4. **Lebih Cocok untuk Aplikasi Bloking**: Jika aplikasi Anda tidak memerlukan penanganan permintaan non-blocking atau asinkron, maka menggunakan Spring MVC mungkin lebih sederhana dan efisien.

**Kekurangan**
1. Kurangnya Dukungan Non-Blocking: Spring MVC dirancang untuk aplikasi berbasis blok dan sinkronisasi, di mana setiap permintaan diproses satu per satu. Jika aplikasi Anda memerlukan penanganan permintaan non-blocking atau asinkron, maka Spring MVC mungkin tidak sesuai.

2. Skalabilitas: Spring MVC mungkin tidak seefisien Spring WebFlux dalam hal penanganan permintaan simultan dan beban tinggi. Jika aplikasi Anda memerlukan skalabilitas tinggi, maka Spring WebFlux mungkin lebih sesuai.

3. Pemrograman Fungsional: Spring MVC tidak mendukung pendekatan pemrograman fungsional yang ditawarkan oleh Spring WebFlux. Jika Anda lebih suka gaya pemrograman ini, maka Spring WebFlux mungkin lebih sesuai.

### Spring WebFlux
**Kelebihan**
1. **Dukungan Non-Blocking dan Asinkron**: Spring WebFlux dirancang untuk penanganan permintaan non-blocking dan asinkron, yang memungkinkan banyak permintaan dapat diproses secara bersamaan. Ini sangat berguna untuk aplikasi dengan beban tinggi atau aplikasi yang memerlukan penanganan permintaan real-time.

2. **Skalabilitas**: Spring WebFlux dapat menangani lebih banyak permintaan secara simultan dengan menggunakan lebih sedikit sumber daya (misalnya, thread), yang membuatnya lebih skalabel dibandingkan dengan Spring MVC.

3. **Pemrograman Fungsional**: Spring WebFlux mendukung pendekatan pemrograman fungsional untuk mendefinisikan rute, yang dapat membuat kode lebih ringkas dan mudah dipahami bagi beberapa pengembang.

4. **Efisiensi**: Dalam beberapa kasus, Spring WebFlux dapat lebih efisien dibandingkan dengan Spring MVC dalam hal penggunaan memori dan CPU, terutama untuk aplikasi dengan beban tinggi.

**Kekurangan**
1. **Kurva Belajar**: Meskipun WebFlux mendukung model pemrograman reaktif, ada kurva belajar yang cukup curam jika Anda belum terbiasa dengan pemrograman reaktif.

2. **Kompatibilitas**: Beberapa pustaka dan kerangka kerja mungkin belum sepenuhnya kompatibel dengan model pemrograman reaktif yang digunakan oleh WebFlux.

3. **Kompleksitas**: Pendekatan non-blocking dan asinkron yang digunakan oleh WebFlux dapat menambah kompleksitas ke aplikasi Anda, terutama jika aplikasi tersebut tidak memerlukan penanganan permintaan non-blocking atau asinkron.

## Contoh Penggunaan
### Spring Boot (Spring MVC)

```java
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String hello() {
        return "Hello, World!";
    }
}

```

Dalam contoh di atas, kita membuat _controller_ dengan anotasi `@RestController` dan metode `hello()` dengan anotasi `@GetMapping`. Metode ini akan dipanggil ketika ada permintaan `GET` ke `/hello`.

### Spring WebFlux

```java
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.web.reactive.function.server.RouterFunction;
import org.springframework.web.reactive.function.server.ServerResponse;

import static org.springframework.web.reactive.function.server.RequestPredicates.GET;
import static org.springframework.web.reactive.function.server.RouterFunctions.route;

@Configuration
public class HelloRouter {

    @Bean
    public RouterFunction<ServerResponse> routeHello(HelloHandler helloHandler) {
        return route(GET("/hello"), helloHandler::hello);
    }
}

```
Dalam contoh di atas, kita mendefinisikan fungsi router dengan anotasi `@Bean`. Fungsi ini akan memetakan permintaan `GET` ke `/hello` ke metode `hello()` pada `HelloHandler`.

## Reference
1. [spring mvc - What is the difference between Router and Annotated Controllers? - Stack Overflow](https://stackoverflow.com/questions/51786154/what-is-the-difference-between-router-and-annotated-controllers)

2. [java - Spring webflux - Routing - Stack Overflow](https://stackoverflow.com/questions/63537517/spring-webflux-routing)

3. [Difference between spring-boot-starter-web and spring-boot-starter-webflux? - Stack Overflow](https://stackoverflow.com/questions/60787693/difference-between-spring-boot-starter-web-and-spring-boot-starter-webflux)

4. [Reactive Programming, Project Reactor, Spring WebFlux, Oh my!! | Intuit Engineering](https://medium.com/intuit-engineering/reactive-programming-project-reactor-webflux-oh-my-4bfa470feee7)

5. [What are the advantages of Spring WebFlux over standard Spring Boot, TomCat, Jetty, Servlet 3.1, Netty? - Stack Overflow](https://stackoverflow.com/questions/46592042/what-are-the-advantages-of-spring-webflux-over-standard-spring-boot-tomcat-jet)

6. [Request Handling and Routing Mechanism in Spring Boot | by BecomeGeeks | Medium](https://becomegeeks.medium.com/request-handling-and-routing-mechanism-in-spring-boot-3805ce6f6f4b)

7. [Guide to Spring 5 WebFlux | Baeldung](https://www.baeldung.com/spring-webflux)

8. [reactive programming - Java Spring WebFlux vs RxJava - Stack Overflow](https://stackoverflow.com/questions/56461260/java-spring-webflux-vs-rxjava)