To use other features, you integrate the relevant [[Spring]] modules.

#### Using Spring Data JPA
- 1. **Add Dependencies**: In your `pom.xml`, ensure you have `spring-boot-starter-data-jpa` and a database driver (e.g., `h2` for testing)
- 2. **Define an Entity**: Create a standard Java class to represent a row in your database table.

```Java
import jakarta.persistence.Entity;
import jakarta.persistence.Id;

@Entity
public class Product {
    @Id
    private Long id;
    private String name;
    // ... getters and setters
}
```

- 3. **Create a Repository**: This is where [[Spring]] Data saves immense boilerplate. You define an interface that extends a [[Spring]] Data interface, and [[Spring]] automatically writes the implementation for basic CRUD operations.

```Java
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;

// Spring automatically generates the implementation for basic methods 
// like findAll(), save(), findById(), etc.
@Repository
public interface ProductRepository extends JpaRepository<Product, Long> {
    
    // You can also define custom query methods just by naming them correctly
    List<Product> findByName(String name);
}
```

- 4. **Inject and Use the Repository**: You can now inject `ProductRepository` into your `Service` layer and use methods like `repository.findAll()` without writing any SQL or JDBC code.