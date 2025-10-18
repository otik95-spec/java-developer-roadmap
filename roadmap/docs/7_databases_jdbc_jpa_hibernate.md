# 7️⃣ Working with Databases, JDBC, JPA, and Hibernate

---

## 7.1 Introduction to Databases

- [ ] **What is a database:** Structured data storage for long-term use.
- [ ] **Relational databases:** Tables, rows, columns, relationships.
- [ ] **SQL basics:** `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
- [ ] **Primary/foreign keys:** Ensuring uniqueness and relationships.
- [ ] **Popular DBMS:** PostgreSQL, MySQL, H2, SQLite.

### 🧩 Practical Tasks 7.1

1. **Install a DBMS:**  
   Install PostgreSQL or MySQL and connect via command-line or GUI (DBeaver, IntelliJ).

2. **Create schema:**  
   Create a new database `school` and table `students(id, name, age, grade)`.

3. **SQL basics:**  
   Insert a few rows and retrieve them with `SELECT * FROM students;`.

4. **Constraints:**  
   Add `PRIMARY KEY` to `id` and `NOT NULL` to `name`.

5. **Relationships:**  
   Create a second table `courses` and a linking table `student_courses`.

---

## 7.2 Introduction to JDBC

- [ ] **JDBC (Java Database Connectivity):** Java API for connecting to databases.
- [ ] **DriverManager and Connection:** Establishing connection with DB.
- [ ] **Statement and PreparedStatement:** Executing SQL commands.
- [ ] **ResultSet:** Reading query results.
- [ ] **Closing resources:** Always close connections, statements, and result sets.

### 🧩 Practical Tasks 7.2

1. **Connect to DB:**  
   Write a small program connecting to your local database.

2. **Insert data:**  
   Use `PreparedStatement` to insert a new student into `students`.

3. **Select and print:**  
   Query all students and print their names and ages.

4. **Update data:**  
   Change one student’s grade with an `UPDATE` statement.

5. **Delete record:**  
   Remove a student with a specific ID.

---

## 7.3 Best Practices with JDBC

- [ ] **try-with-resources:** Automatically close connections.
- [ ] **SQL injection protection:** Always use `PreparedStatement`.
- [ ] **Transactions:** Use `setAutoCommit(false)` and `commit()`/`rollback()`.
- [ ] **Batch updates:** Efficiently insert multiple rows.
- [ ] **Connection pooling:** Reuse connections using libraries like HikariCP.

### 🧩 Practical Tasks 7.3

1. **Transaction test:**  
   Transfer money between accounts using commit/rollback.

2. **Batch insert:**  
   Insert 100 students efficiently with batch processing.

3. **SQL injection demo:**  
   Show difference between `Statement` and `PreparedStatement` when user inputs malicious SQL.

4. **Connection pooling:**  
   Integrate HikariCP and configure minimum and maximum pool size.

5. **Logging:**  
   Log SQL queries being executed to the console.

---

## 7.4 ORM and JPA Introduction

- [ ] **ORM (Object-Relational Mapping):** Maps Java objects to database tables.
- [ ] **JPA (Java Persistence API):** Standard API for ORM frameworks.
- [ ] **Entities and annotations:** `@Entity`, `@Table`, `@Id`, `@Column`.
- [ ] **Persistence context:** Manages entity states — transient, persistent, detached, removed.
- [ ] **Entity lifecycle:** From creation to deletion.

### 🧩 Practical Tasks 7.4

1. **JPA setup:**  
   Create a Maven/Gradle project with `spring-boot-starter-data-jpa` or standalone Hibernate.

2. **Entity creation:**  
   Create an entity `Student` mapped to `students` table.

3. **CRUD operations:**  
   Save, read, update, and delete using JPA’s `EntityManager` or Spring Data `JpaRepository`.

4. **Mapping fields:**  
   Use annotations like `@Column(nullable = false)` and `@GeneratedValue`.

5. **Lifecycle logging:**  
   Print entity state changes with logs or debugger.

---

## 7.5 Relationships in JPA

- [ ] **One-to-One (`@OneToOne`)** — Example: `User` ↔ `Profile`.
- [ ] **One-to-Many (`@OneToMany`)** — Example: `Teacher` ↔ `Students`.
- [ ] **Many-to-One (`@ManyToOne`)** — Example: `Student` ↔ `Group`.
- [ ] **Many-to-Many (`@ManyToMany`)** — Example: `Student` ↔ `Course`.
- [ ] **Cascade types and fetch strategies:** `CascadeType.ALL`, `FetchType.LAZY`, `FetchType.EAGER`.

### 🧩 Practical Tasks 7.5

1. **One-to-Many:**  
   Create `Teacher` with multiple `Student`s using `@OneToMany`.

2. **Many-to-Many:**  
   Create `Student` ↔ `Course` relation with a join table.

3. **Cascade example:**  
   Delete a teacher and automatically delete related students.

4. **Lazy loading:**  
   Access lazy-loaded field and observe proxy behavior.

5. **Bidirectional:**  
   Implement both sides of the relationship (`mappedBy`).

---

## 7.6 Queries with JPA and JPQL

- [ ] **JPQL (Java Persistence Query Language):** Object-oriented SQL.
- [ ] **Query creation:** `entityManager.createQuery("SELECT s FROM Student s")`.
- [ ] **Named queries:** Reusable queries with `@NamedQuery`.
- [ ] **Native queries:** Execute raw SQL via `@Query(nativeQuery = true)`.
- [ ] **Criteria API:** Build queries dynamically.

### 🧩 Practical Tasks 7.6

1. **Basic query:**  
   Retrieve all students using JPQL.

2. **Filter:**  
   Get students older than 18.

3. **Named query:**  
   Add `@NamedQuery` to your entity and execute it.

4. **Native query:**  
   Run raw SQL query to retrieve table size.

5. **Criteria API:**  
   Build a dynamic search query for student name and age.

---

## 7.7 Transactions and Entity States

- [ ] **Entity states:** New, managed, detached, removed.
- [ ] **Transactional management:** `@Transactional` in Spring.
- [ ] **Dirty checking:** Automatic persistence of changed entities.
- [ ] **Rollback behavior:** Automatic rollback on exceptions.
- [ ] **Optimistic vs pessimistic locking.**

### 🧩 Practical Tasks 7.7

1. **Transactional method:**  
   Annotate a service method with `@Transactional` and update multiple entities.

2. **Rollback test:**  
   Throw an exception mid-transaction and confirm data is rolled back.

3. **Dirty checking:**  
   Modify entity fields and verify updates occur automatically.

4. **Detached entity:**  
   Detach entity and try to modify it — check persistence result.

5. **Optimistic lock:**  
   Add `@Version` field to handle concurrent updates.

---

## 7.8 Hibernate Advanced Features

- [ ] **Caching:** First-level (Session) and second-level (EHCache, Redis).
- [ ] **Batch fetching and joins:** Optimize N+1 query issues.
- [ ] **Inheritance mapping:** `@Inheritance(strategy = ...)`.
- [ ] **DTO projections:** Map query results to DTOs.
- [ ] **Interceptors and event listeners.**

### 🧩 Practical Tasks 7.8

1. **Caching:**  
   Enable Hibernate second-level cache and compare query counts.

2. **N+1 problem:**  
   Demonstrate and fix N+1 queries with `join fetch`.

3. **Inheritance:**  
   Create base `User` entity and subclasses `Admin` and `Customer`.

4. **DTO projection:**  
   Fetch only specific fields into a DTO class.

5. **Event listener:**  
   Add a listener that logs entity save events.

---

## 7.9 Database Migrations (Flyway/Liquibase)

- [ ] **Migration tools:** Track and version your database schema.
- [ ] **Flyway:** Simple SQL-based migrations (`V1__init.sql`, etc.).
- [ ] **Liquibase:** XML/YAML/SQL changelogs for complex control.
- [ ] **Integration with Spring Boot:** Automatic execution on startup.
- [ ] **Best practices:** One migration file per feature or release.

### 🧩 Practical Tasks 7.9

1. **Flyway setup:**  
   Add `flyway` dependency and create an initial migration file.

2. **Table migration:**  
   Add a new column `email` to `students` via migration script.

3. **Data migration:**  
   Populate sample data in `V2__data_seed.sql`.

4. **Rollback simulation:**  
   Delete a migration file and check Flyway validation failure.

5. **Liquibase alternative:**  
   Try Liquibase for one migration to compare syntax.

---

## 🧠 Summary Practice Tasks

1. **Student management system:**  
   Full CRUD with JPA, relationships, and Flyway migrations.

2. **Bank account model:**  
   Implement accounts, transactions, and rollback-safe transfers.

3. **Library app:**  
   Manage books, authors, and borrowers using Hibernate relationships.

4. **ORM optimization:**  
   Demonstrate N+1 problem and fix using `join fetch`.

5. **Versioned schema:**  
   Manage schema evolution with multiple Flyway migrations.

---

✅ **End of Section 7 — Working with Databases, JDBC, JPA, and Hibernate**  
Next: [8. Spring Framework and Spring Boot →](./8_spring_and_spring_boot.md)
