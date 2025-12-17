Once the project is set up, you start writing code, primarily defining **Beans** and leveraging **Dependency Injection**.

#### Define a Service (The Bean)
In [[Spring]], business logic resides in classes that are managed by the IoC container. You mark these classes using annotations.
```Java
package com.example.app;

import org.springframework.stereotype.Service;

// @Service marks this class as a Spring Bean (a service layer component)
@Service
public class GreetingService {

    public String getGreeting() {
        return "Hello from Spring!";
    }

}
```

#### Use Dependency Injection (DI)
You don't create an instance of `GreetingService`; you ask [[Spring]] to give it to you where it is needed (e.g., in a Controller).
```Java
package com.example.app;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

// @RestController combines @Controller and @ResponseBody 
// to quickly create RESTful APIs
@RestController
public class GreetingController {

    // 1. Dependency Injection: 
    // The @Autowired annotation tells Spring to find a 'GreetingService' 
    // Bean in the container and inject it here.
    private final GreetingService greetingService;

    // 2. Constructor Injection (Recommended Pattern)
    // Spring automatically manages the injection via the constructor
    public GreetingController(GreetingService greetingService) {
        this.greetingService = greetingService;
    }

    // 3. Define the Endpoint
    @GetMapping("/hello")
    public String hello() {
        return greetingService.getGreeting(); // Uses the injected service
    }
}
```

#### Run the Application
Since [[Spring]] Boot includes an embedded web server (usually Tomcat), you can run the main application class directly from your IDE:
```Java
package com.example.app;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

// The starting point of the Spring Boot application
@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```
After running, the application will typically be accessible at `http://locahost:800/hello`.
