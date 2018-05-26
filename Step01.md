# SpringBoot-api
SpringBoot Practice: 


## pom.xml
      <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>1.5.6.RELEASE</version>
      </parent>

      <dependencies>
        <dependency>
          <groupId>org.springframework.boot</groupId>
          <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
      </dependencies>

      <properties>
        <java.version>1.8</java.version>
      </properties>
      
## Application.java

    import org.springframework.boot.SpringApplication;
    import org.springframework.boot.autoconfigure.SpringBootApplication;

    @SpringBootApplication
    public class Application {
      public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
      }
    }
    
## HelloController.java

      import org.springframework.web.bind.annotation.RestController;
      import org.springframework.web.bind.annotation.RequestMapping;

      @RestController
      public class HelloController {
          @RequestMapping("/")
          public String index() {
              return "Greetings from Spring Boot!";
          }
          @RequestMapping("/hello")
          public String sayHello() {
              return "Hi!";
          }
      }
