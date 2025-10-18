# 8️⃣ Spring Framework and Spring Boot

---

## 8.1 Introduction to Spring Framework

- [ ] **Purpose:** Simplify Java enterprise development through dependency injection and modular design.
- [ ] **Spring modules:** Core, Context, Web, Data, Security, AOP, etc.
- [ ] **Dependency Injection (DI):** Managing object creation and dependencies via the IoC container.
- [ ] **Inversion of Control (IoC):** Framework, not the developer, controls dependencies.
- [ ] **Configuration methods:** XML, Java-based (`@Configuration`), annotation-based (`@Component`, `@Bean`).

### 🧩 Practical Tasks 8.1

1. **Simple DI:**  
   Create two classes `Car` and `Engine`. Inject `Engine` into `Car` using `@Autowired`.

2. **ApplicationContext:**  
   Create an `ApplicationContext` from configuration and retrieve beans manually.

3. **Bean definition:**  
   Define a bean using `@Bean` in a `@Configuration` class.

4. **Scope test:**  
   Create a bean with `@Scope("prototype")` and observe different instances.

5. **Manual vs automatic wiring:**  
   Compare manual bean creation with annotation-based DI.

---

## 8.2 Spring Boot Fundamentals

- [ ] **Spring Boot:** Simplifies setup, dependency management, and configuration.
- [ ] **Starters:** Predefined dependency sets (`spring-boot-starter-web`, `spring-boot-starter-data-jpa`, etc.).
- [ ] **Auto-configuration:** Automatically configures based on classpath contents.
- [ ] **Application structure:** Typical project layout (controller, service, repository, model).
- [ ] **Properties and YAML:** Configuring application settings via `application.properties` or `application.yml`.

### 🧩 Practical Tasks 8.2

1. **Create a Spring Boot app:**  
   Initialize via Spring Initializr and run `Hello World` REST API.

2. **Auto-configuration:**  
   Explore which beans are created automatically by Boot.

3. **Custom properties:**  
   Add custom property in `application.yml` and inject it using `@Value`.

4. **Profiles:**  
   Define `dev` and `prod` profiles with different DB configs.

5. **CommandLineRunner:**  
   Print startup info after application launch.

---

## 8.3 Spring Beans and Lifecycle

- [ ] **Bean lifecycle:** Creation → initialization → usage → destruction.
- [ ] **Annotations:** `@PostConstruct`, `@PreDestroy`.
- [ ] **Bean scopes:** `singleton`, `prototype`, `request`, `session`.
- [ ] **ApplicationContextAware:** Access application context programmatically.
- [ ] **Lazy initialization:** Use `@Lazy` for deferred creation.

### 🧩 Practical Tasks 8.3

1. **Lifecycle demo:**  
   Add `@PostConstruct` and `@PreDestroy` methods to a bean and observe output.

2. **Custom scope:**  
   Create singleton and prototype beans and compare lifecycle behavior.

3. **Lazy loading:**  
   Mark a bean as `@Lazy` and see when it gets initialized.

4. **Context access:**  
   Implement `ApplicationContextAware` to fetch another bean manually.

5. **Shutdown hook:**  
   Observe bean destruction when the app stops.

---

## 8.4 Spring MVC — REST API Development

- [ ] **Controllers:** Annotate with `@RestController`.
- [ ] **Request mapping:** `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.
- [ ] **Request/response handling:** `@RequestBody`, `@PathVariable`, `@RequestParam`.
- [ ] **ResponseEntity:** Custom responses with HTTP status codes.
- [ ] **Exception handling:** Global handlers with `@ControllerAdvice`.

### 🧩 Practical Tasks 8.4

1. **Simple controller:**  
   Create `GreetingController` with endpoint `/hello` returning `"Hello, Spring!"`.

2. **Path variables:**  
   Implement `/users/{id}` returning user info from memory.

3. **Request body:**  
   Accept JSON payload for creating new users.

4. **ResponseEntity:**  
   Return proper HTTP codes (201 for created, 404 for not found).

5. **Exception handling:**  
   Add global handler that returns custom error JSON.

---

## 8.5 Spring Data JPA

- [ ] **Repository abstraction:** Simplifies database access.
- [ ] **JpaRepository:** Built-in CRUD methods.
- [ ] **Derived queries:** Find by field name (e.g. `findByEmail()`).
- [ ] **Custom queries:** Use `@Query` for JPQL or native SQL.
- [ ] **Pagination and sorting:** `Pageable` and `Sort`.

### 🧩 Practical Tasks 8.5

1. **Entity + repository:**  
   Create `User` entity and `UserRepository` extending `JpaRepository`.

2. **Find methods:**  
   Add methods like `findByName()` and `findByEmail()`.

3. **Custom query:**  
   Add `@Query("SELECT u FROM User u WHERE u.active = true")`.

4. **Pagination:**  
   Retrieve paged results for users list.

5. **Sorting:**  
   Sort results by creation date descending.

---

## 8.6 Spring Validation

- [ ] **Validation annotations:** `@NotNull`, `@Size`, `@Email`, `@Pattern`, etc.
- [ ] **Bean Validation (JSR-380):** `javax.validation` and `jakarta.validation`.
- [ ] **`@Valid` and `@Validated`:** Trigger validation automatically.
- [ ] **Custom validators:** Implement `ConstraintValidator`.
- [ ] **Error handling:** Return structured validation errors.

### 🧩 Practical Tasks 8.6

1. **Field validation:**  
   Add validation to `User` entity fields.

2. **Global validation:**  
   Apply `@Valid` in controller request methods.

3. **Custom validator:**  
   Create `@ValidPassword` annotation and custom validator class.

4. **Error response:**  
   Handle validation exceptions globally.

5. **Group validation:**  
   Use validation groups for different use cases (e.g., create vs update).

---

## 8.7 Spring Boot Configuration and Profiles

- [ ] **Configuration files:** `application.yml` and profile-based overrides.
- [ ] **`@ConfigurationProperties`:** Map config sections to Java objects.
- [ ] **Environment abstraction:** Access environment variables and system properties.
- [ ] **Profile activation:** Use `spring.profiles.active`.
- [ ] **External configuration sources:** Command-line args, env vars, config server.

### 🧩 Practical Tasks 8.7

1. **YAML configuration:**  
   Create hierarchical settings under `app:` prefix and load via `@ConfigurationProperties`.

2. **Profile-specific files:**  
   Add `application-dev.yml` and `application-prod.yml`.

3. **Environment print:**  
   Print active profile on startup.

4. **External config:**  
   Pass config values as CLI args when running the app.

5. **Custom prefix:**  
   Use custom property prefix for business configuration.

---

## 8.8 Logging and Monitoring

- [ ] **Logging frameworks:** SLF4J, Logback, Log4j2.
- [ ] **Configuration:** Log levels and appenders in `logback-spring.xml`.
- [ ] **Application metrics:** Spring Actuator endpoints.
- [ ] **Health checks:** `/actuator/health` for service status.
- [ ] **Custom metrics:** Expose counters and gauges.

### 🧩 Practical Tasks 8.8

1. **Basic logging:**  
   Use `LoggerFactory` to log at different levels.

2. **Custom configuration:**  
   Modify logging pattern and level in `logback-spring.xml`.

3. **Actuator setup:**  
   Add `spring-boot-starter-actuator` and test `/actuator/health`.

4. **Custom endpoint:**  
   Create a new actuator endpoint `/actuator/info/custom`.

5. **Metrics dashboard:**  
   Use `/actuator/metrics` to observe request counts and response times.

---

## 8.9 Spring Boot Dev Tools and Testing Utilities

- [ ] **DevTools:** Auto-restart and live reload for development.
- [ ] **Spring Boot Test:** Integration test setup using `@SpringBootTest`.
- [ ] **MockMvc:** Simulate HTTP requests to controllers.
- [ ] **Test configuration:** Use in-memory DB (H2).
- [ ] **Profile-based test configs:** Activate `test` profile.

### 🧩 Practical Tasks 8.9

1. **DevTools setup:**  
   Add DevTools dependency and verify auto-restart.

2. **Integration test:**  
   Write a test for your REST controller using `@SpringBootTest`.

3. **MockMvc test:**  
   Simulate GET and POST endpoints and assert responses.

4. **Test database:**  
   Configure `spring.datasource.url=jdbc:h2:mem:testdb`.

5. **Profile switching:**  
   Use `@ActiveProfiles("test")` for test environment setup.

---

## 🧠 Summary Practice Tasks

1. **User management API:**  
   Create a CRUD API for users with validation, repository, and service layer.

2. **Todo REST service:**  
   Build a complete REST service with filtering, sorting, and pagination.

3. **Profile-based setup:**  
   Implement different configurations for local, dev, and prod environments.

4. **Logging and health:**  
   Add custom logs and monitor your app via `/actuator/health`.

5. **Integration test suite:**  
   Test controllers and repositories end-to-end using H2 and MockMvc.

---

✅ **End of Section 8 — Spring Framework and Spring Boot**  
Next: [9. Spring Advanced: Security, WebFlux, Messaging, Cloud →](./9_spring_advanced_security_cloud.md)
