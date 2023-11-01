# Spring Validation

Spring Validation adalah fitur yang disediakan oleh Spring Boot untuk memvalidasi inputan pengguna. Ini adalah tugas yang sangat umum namun kritis.

**_reference_**: [https://reflectoring.io/bean-validation-with-spring-boot/](https://reflectoring.io/bean-validation-with-spring-boot/)

## Cara penggunaan
Cara menggunakannya adalah dengan menambahkan dependency pada pom.xml dan jangan lupa untuk refresh maven
```xml 
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

## Beberapa anotasi validasi yang umum
### 1. @Notnull
Untuk memberitahu bahwa field tersebut tidak boleh null
### 2. @NotEmpty
Untuk memberitahu bahwa field tersebut tidak boleh null dan kosong
### 3. @NotBlank
Untuk memberitahu bahwa field tersebut tidak boleh null dan kosong, tetapi sebeleum melakukan pengecekan, ia akan memotong (trim) nilai terlebih dahulu.
### 4. @Min dan @Max
untuk memberitahu bahwa bidang numerik hanya valid jika nilainya di atas atau di bawah nilai tertentu.
### 5. @Pattern
untuk memberitahu bahwa bidang string hanya valid jika cocok dengan ekspresi reguler (_regex_) tertentu.
### 6. @Email
untuk memberitahu bahwa bidang string harus berupa alamat email yang valid.

## Contoh Penggunaan
```java
class Customer {

  @Email
  private String email;

  @NotBlank
  private String name;
  
  // ...
}
```

## Validator
Untuk memvalidasi apakah suatu objek valid, kita meneruskannya ke Validator yang memeriksa apakah batasannya terpenuhi:
```java
Set<ConstraintViolation<Input>> violations = validator.validate(customer);
if (!violations.isEmpty()) {
  throw new ConstraintViolationException(violations);
}
```

## Validasi input pada Spring MVC Controller
Katakanlah kita telah mengimplementasikan Spring REST Controller dan ingin memvalidasi input yang diteruskan oleh klien. Ada tiga hal yang dapat kami validasi untuk setiap permintaan HTTP yang masuk:
1. Request Body
2. Path Variable (seperti `id` pada `/foos/{id}`)
3. Query Parameter


### Contoh validasi pada Request Body
Dalam permintaan POST dan PUT, merupakan hal yang umum untuk meneruskan payload JSON dalam isi permintaan. Spring secara otomatis memetakan JSON yang masuk ke objek Java. Sekarang, kami ingin memeriksa apakah objek Java yang masuk memenuhi persyaratan kami.

contoh payload yang masuk :
```java
class Input {

  @Min(1)
  @Max(10)
  private int numberBetweenOneAndTen;

  @Pattern(regexp = "^[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}$")
  private String ipAddress;
  
  // ...
}
```

disini terdapat dua variable yaitu `numberBetweenOneAndTen` tipe `int` dengan ketentuan nilainya harus diantara 1~10 dan `ipAddress` tipe `string` dengan ketentuan nilainya harus berisi alamat IP seperti yang ditentukan oleh _regex_ pada anotasi `@Pattern` 


Untuk memvalidasi isi _request_ HTTP yang masuk, kami menganotasi isi _request_ dengan anotasi `@Valid` di REST Controller
```java
@RestController
class ValidateRequestBodyController {

  @PostMapping("/validateBody")
  ResponseEntity<String> validateBody(@Valid @RequestBody Input input) {
    return ResponseEntity.ok("valid");
  }

}
```

Kita bisa mencobanya dengan membuat integration test seperti :
```java
@ExtendWith(SpringExtension.class)
@WebMvcTest(controllers = ValidateRequestBodyController.class)
class ValidateRequestBodyControllerTest {

  @Autowired
  private MockMvc mvc;

  @Autowired
  private ObjectMapper objectMapper;

  @Test
  void whenInputIsInvalid_thenReturnsStatus400() throws Exception {
    Input input = invalidInput();
    String body = objectMapper.writeValueAsString(input);

    mvc.perform(post("/validateBody")
            .contentType("application/json")
            .content(body))
            .andExpect(status().isBadRequest());
  }
}
```

### Contoh validasi pada Path Variable dan Request Parameter

Daripada memberi anotasi pada _field_ _class_ seperti di atas, kita bisa menambahkan anotasi batasan (dalam hal ini `@Min`) langsung ke parameter metode di Spring _controller_:

```java
@RestController
@Validated
class ValidateParametersController {

  @GetMapping("/validatePathVariable/{id}")
  ResponseEntity<String> validatePathVariable(
      @PathVariable("id") @Min(5) int id) {
    return ResponseEntity.ok("valid");
  }
  
  @GetMapping("/validateRequestParameter")
  ResponseEntity<String> validateRequestParameter(
      @RequestParam("param") @Min(5) int param) { 
    return ResponseEntity.ok("valid");
  }
}
```

Perhatikan bahwa kita harus menambahkan anotasi `@Validated` Spring ke _controller_ di tingkat kelas untuk memberi tahu Spring agar mengevaluasi anotasi batasan pada parameter metode.