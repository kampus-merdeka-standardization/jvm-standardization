## Java Lombok
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
#### 1. Getter Setter
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

#### 2. Constructor

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
#### 3. ToString
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
#### 4. Equals And HashCode
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
#### 5. Builder
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
#### 6. SneakyThrows
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
#### 7. Synchronized
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

#### Dan lain-lain
Dan masih banyak lagi yang lainnya sehingga dapat mempermudah dan mempercepat kita dalam proses development. [Click here for the references !](https://projectlombok.org/)