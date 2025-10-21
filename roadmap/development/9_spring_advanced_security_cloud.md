# 9️⃣ Spring Advanced: Security, WebFlux, Messaging, Cloud

---

## 9.1 Spring Security — Fundamentals

- [ ] **Purpose:** Protect web applications and APIs.
- [ ] **Authentication vs authorization:** Who you are vs what you can do.
- [ ] **Default login:** Spring Boot provides built-in login form and user.
- [ ] **UserDetailsService:** Custom user authentication source.
- [ ] **Password encoding:** `BCryptPasswordEncoder` for secure storage.

### 🧩 Practical Tasks 9.1

1. **Basic auth setup:**  
   Add `spring-boot-starter-security` and explore default login form.

2. **Custom user:**  
   Define in-memory users with roles in `SecurityConfig`.

3. **Custom login page:**  
   Replace default form with your own HTML login page.

4. **Endpoint protection:**  
   Secure `/admin` for `ROLE_ADMIN` only.

5. **Password encoder:**  
   Configure `BCryptPasswordEncoder` and encode passwords before saving.

---

## 9.2 Advanced Security — JWT and REST APIs

- [ ] **Stateless authentication:** No sessions, use JWT (JSON Web Tokens).
- [ ] **JWT structure:** Header, payload, signature.
- [ ] **Token generation:** Create JWT after successful login.
- [ ] **Filters:** Use `OncePerRequestFilter` for token validation.
- [ ] **CORS and CSRF:** Handle securely for REST APIs.

### 🧩 Practical Tasks 9.2

1. **JWT library:**  
   Add `jjwt` or `java-jwt` dependency.

2. **Generate token:**  
   On successful login, return JWT instead of session ID.

3. **Token validation filter:**  
   Implement filter that validates and extracts username from token.

4. **Role-based access:**  
   Configure roles via claims in JWT.

5. **CORS setup:**  
   Enable CORS for API endpoints in security configuration.

---

## 9.3 Spring WebFlux — Reactive Programming

- [ ] **Purpose:** Non-blocking, asynchronous web stack.
- [ ] **Key types:** `Mono<T>` and `Flux<T>`.
- [ ] **Reactive controller:** Annotate with `@RestController` but return reactive types.
- [ ] **WebClient:** Asynchronous HTTP client replacing RestTemplate.
- [ ] **Backpressure:** Controlling data flow in streams.

### 🧩 Practical Tasks 9.3

1. **Reactive endpoint:**  
   Create endpoint returning `Flux<String>` with delayed elements.

2. **Mono example:**  
   Return single user info as `Mono<User>`.

3. **WebClient usage:**  
   Call external API reactively and print result.

4. **Chaining:**  
   Combine multiple async calls using `flatMap()`.

5. **Error handling:**  
   Add `.onErrorResume()` to handle network failures.

---

## 9.4 Reactive Data and R2DBC

- [ ] **R2DBC:** Reactive alternative to JDBC.
- [ ] **Dependencies:** `spring-boot-starter-data-r2dbc`, `r2dbc-postgresql`.
- [ ] **Repositories:** `ReactiveCrudRepository`.
- [ ] **Transactions:** Limited but supported via reactive transaction manager.
- [ ] **When to use:** For high-load, reactive microservices.

### 🧩 Practical Tasks 9.4

1. **R2DBC setup:**  
   Configure reactive PostgreSQL connection.

2. **Reactive repository:**  
   Create repository extending `ReactiveCrudRepository<User, Long>`.

3. **Save and retrieve:**  
   Insert and read reactive entities.

4. **Chaining operations:**  
   Chain multiple operations with `flatMap()` and `then()`.

5. **Error flow:**  
   Handle errors gracefully with `onErrorContinue()`.

---

## 9.5 Messaging — RabbitMQ and Kafka

- [ ] **Purpose:** Asynchronous communication between services.
- [ ] **Message brokers:** RabbitMQ (AMQP) and Kafka (stream-based).
- [ ] **Spring AMQP:** `@RabbitListener`, `RabbitTemplate`.
- [ ] **Spring Kafka:** `KafkaTemplate`, `@KafkaListener`.
- [ ] **Error handling and retries.**

### 🧩 Practical Tasks 9.5

1. **RabbitMQ setup:**  
   Configure `spring-boot-starter-amqp` and declare queue + listener.

2. **Send message:**  
   Use `RabbitTemplate.convertAndSend()` to publish a message.

3. **Receive message:**  
   Consume messages with `@RabbitListener`.

4. **Kafka alternative:**  
   Send and consume messages using Spring Kafka.

5. **Retries:**  
   Configure retry logic on message failures.

---

## 9.6 Caching in Spring

- [ ] **Purpose:** Improve performance by storing frequently accessed data.
- [ ] **Annotations:** `@Cacheable`, `@CacheEvict`, `@CachePut`.
- [ ] **Cache providers:** ConcurrentMapCache, Redis, Caffeine.
- [ ] **Spring Boot integration:** Minimal setup for caching.
- [ ] **Key generation:** Customize cache keys for complex parameters.

### 🧩 Practical Tasks 9.6

1. **Enable caching:**  
   Add `@EnableCaching` and test with `@Cacheable` on a service method.

2. **Eviction:**  
   Use `@CacheEvict` when data changes.

3. **Custom key:**  
   Define a cache key using SpEL.

4. **Redis cache:**  
   Integrate `spring-boot-starter-data-redis`.

5. **Performance test:**  
   Measure execution time before and after caching.

---

## 9.7 Spring Cloud — Microservices Overview

- [ ] **Purpose:** Build distributed systems using Spring Cloud.
- [ ] **Key modules:** Config Server, Eureka, Gateway, OpenFeign.
- [ ] **Service discovery:** Register and discover services dynamically.
- [ ] **API Gateway:** Central entry point for routing and filtering requests.
- [ ] **Resilience:** Circuit breakers and retries with Resilience4j.

### 🧩 Practical Tasks 9.7

1. **Eureka setup:**  
   Create Eureka Server and register a simple microservice.

2. **Config Server:**  
   Centralize configuration with Spring Cloud Config.

3. **Gateway:**  
   Implement `spring-cloud-gateway` for routing requests.

4. **Feign Client:**  
   Call other microservices using `@FeignClient`.

5. **Resilience4j:**  
   Add retry and circuit breaker for a remote API call.

---

## 9.8 Spring Boot in Docker and Kubernetes

- [ ] **Containerization:** Run apps in isolated environments.
- [ ] **Dockerfile:** Build container images for Spring Boot.
- [ ] **Docker Compose:** Combine app, DB, and message broker.
- [ ] **Kubernetes basics:** Pods, deployments, services.
- [ ] **Helm charts:** Simplify deployment configuration.

### 🧩 Practical Tasks 9.8

1. **Dockerfile:**  
   Write Dockerfile for Spring Boot app and build an image.

2. **Compose setup:**  
   Use `docker-compose.yml` to run app + PostgreSQL.

3. **Kubernetes deployment:**  
   Deploy app to a local cluster (e.g., Minikube).

4. **Service exposure:**  
   Expose app via `Service` type `LoadBalancer`.

5. **Helm chart:**  
   Create a basic Helm chart for deployment automation.

---

## 9.9 Observability and Cloud Monitoring

- [ ] **Distributed tracing:** Track requests across microservices (Zipkin, Sleuth).
- [ ] **Metrics:** Use Micrometer for Prometheus/Grafana.
- [ ] **Logging correlation:** Link logs with trace IDs.
- [ ] **Health monitoring:** Integrate Actuator with monitoring systems.
- [ ] **Alerts:** Set thresholds for latency or errors.

### 🧩 Practical Tasks 9.9

1. **Tracing setup:**  
   Add `spring-cloud-starter-sleuth` and verify trace IDs in logs.

2. **Zipkin integration:**  
   Send traces to local Zipkin server.

3. **Prometheus metrics:**  
   Expose `/actuator/prometheus` endpoint.

4. **Grafana dashboard:**  
   Visualize app metrics in Grafana.

5. **Health alerts:**  
   Create alert rules for failed health checks.

---

## 🧠 Summary Practice Tasks

1. **JWT-secured REST API:**  
   Build an API with Spring Security and JWT authentication.

2. **Reactive microservice:**  
   Implement a reactive service using WebFlux + R2DBC.

3. **Async communication:**  
   Connect two microservices using RabbitMQ or Kafka.

4. **Cloud-native app:**  
   Containerize your Spring Boot app and deploy to Kubernetes.

5. **Monitoring dashboard:**  
   Combine Actuator + Prometheus + Grafana for full observability.

---

✅ **End of Section 9 — Spring Advanced: Security, WebFlux, Messaging, Cloud**

🎯 **You’ve reached the end of the Java Junior Roadmap!**  
From core Java to cloud-native Spring, you now have a complete foundation to grow toward **Mid-level and beyond.**

Next steps:
- Build your own project integrating multiple sections.
- Contribute to open source.
- Continue learning system design, testing, and cloud architecture.
- Keep coding daily — mastery is repetition. 💪
