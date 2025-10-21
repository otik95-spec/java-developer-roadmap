# 5️⃣ Advanced Java Programming

---

## 5.1 Lambda Expressions

- [ ] **Definition:** Anonymous functions introduced in Java 8.
- [ ] **Syntax:** `(parameters) -> expression` or `(parameters) -> { statements }`.
- [ ] **Functional interfaces:** Interfaces with a single abstract method (`@FunctionalInterface`).
- [ ] **Common ones:** `Runnable`, `Comparator`, `Function`, `Predicate`, `Consumer`, `Supplier`.
- [ ] **Benefits:** Cleaner code, less boilerplate, easier to use with Streams and Collections.

### 🧩 Practical Tasks 5.1

1. **Simple lambda:**  
   Replace an anonymous class implementing `Runnable` with a lambda.

2. **Math operation:**  
   Create a `Calculator` interface with one method `int operate(int a, int b)` and implement addition and subtraction using lambdas.

3. **Predicate filter:**  
   Create a list of integers and use a `Predicate<Integer>` lambda to print only even numbers.

4. **Consumer example:**  
   Use a `Consumer<String>` to print each element in a list of names.

5. **Method reference:**  
   Replace a lambda with a method reference like `System.out::println`.

---

## 5.2 Stream API

- [ ] **Introduction:** Process collections declaratively.
- [ ] **Pipeline:** `stream() → intermediate operations → terminal operation`.
- [ ] **Intermediate operations:** `filter()`, `map()`, `sorted()`, `distinct()`, `limit()`.
- [ ] **Terminal operations:** `forEach()`, `collect()`, `reduce()`, `count()`, `anyMatch()`.
- [ ] **Parallel streams:** Using `parallelStream()` for concurrent processing.

### 🧩 Practical Tasks 5.2

1. **Stream basics:**  
   Create a list of integers and use streams to filter even numbers, square them, and collect results into a new list.

2. **Strings and lengths:**  
   Given a list of strings, print only those with length > 3.

3. **Aggregation:**  
   Find the average value of a list of doubles using `mapToDouble().average()`.

4. **Grouping:**  
   Group employees by department using `Collectors.groupingBy()`.

5. **Parallel stream:**  
   Use `parallelStream()` to sum a large list of numbers and compare performance.

---

## 5.3 Optional Class

- [ ] **Purpose:** Avoid `NullPointerException` and express optional values.
- [ ] **Creation:** `Optional.of()`, `Optional.ofNullable()`, `Optional.empty()`.
- [ ] **Access methods:** `isPresent()`, `ifPresent()`, `orElse()`, `orElseGet()`, `orElseThrow()`.
- [ ] **Chaining:** Combine Optionals with map/filter.

### 🧩 Practical Tasks 5.3

1. **Null handling:**  
   Wrap a possibly null value with `Optional.ofNullable()`.

2. **Default value:**  
   Use `orElse()` to return a fallback when no value is present.

3. **Conditional action:**  
   Use `ifPresent()` to print a message only if a value exists.

4. **Chaining:**  
   Chain map/filter/orElse to transform an optional string to uppercase or return “empty”.

5. **Safe get:**  
   Use `orElseThrow()` to throw a custom exception when Optional is empty.

---

## 5.4 Functional Programming Concepts

- [ ] **Pure functions:** No side effects.
- [ ] **Immutability:** Data not modified after creation.
- [ ] **Higher-order functions:** Accept or return functions.
- [ ] **Composition:** Combine small functions into larger ones.
- [ ] **Streams + lambdas:** Declarative style of functional programming.

### 🧩 Practical Tasks 5.4

1. **Pure function:**  
   Implement a function that calculates tax without modifying inputs.

2. **Composition:**  
   Combine two `Function<String, String>` lambdas: one uppercases a string, the other adds “!!!”.

3. **Map transformation:**  
   Use `Stream.map()` to apply a function to all elements of a list.

4. **Predicate chaining:**  
   Combine two predicates: one checks if number > 0, another if even.

5. **Supplier usage:**  
   Use a `Supplier<UUID>` to generate random IDs.

---

## 5.5 Records (Java 16+)

- [ ] **Definition:** Immutable data carriers replacing boilerplate POJOs.
- [ ] **Syntax:** `public record Point(int x, int y) {}`.
- [ ] **Automatic methods:** `equals()`, `hashCode()`, `toString()`.
- [ ] **Custom constructors and validation:** Define compact constructors.
- [ ] **When to use:** DTOs, API responses, simple immutable data.

### 🧩 Practical Tasks 5.5

1. **Simple record:**  
   Create a record `Point(int x, int y)` and print it.

2. **Equality check:**  
   Compare two identical `Point` objects and print the result.

3. **Validation:**  
   Add a compact constructor that throws an exception for negative coordinates.

4. **Nested record:**  
   Create `record Rectangle(Point a, Point b)` and compute area.

5. **Integration:**  
   Replace a DTO class in your previous code with a record.

---

## 5.6 Sealed Classes (Java 17+)

- [ ] **Purpose:** Restrict which classes can extend or implement a class/interface.
- [ ] **Syntax:** `public sealed class Shape permits Circle, Rectangle {}`.
- [ ] **Permitted subclasses:** Must be `final`, `sealed`, or `non-sealed`.
- [ ] **Use cases:** Controlled inheritance, domain modeling, pattern matching.

### 🧩 Practical Tasks 5.6

1. **Sealed hierarchy:**  
   Create a sealed class `Shape` permitting `Circle` and `Square`.

2. **Subclass implementation:**  
   Implement both permitted subclasses and override `area()`.

3. **Non-sealed class:**  
   Add a `non-sealed` subclass and extend it further.

4. **Pattern matching (Java 21+):**  
   Use `instanceof` pattern matching with sealed classes.

5. **Forbidden subclass:**  
   Try to extend `Shape` outside permitted classes — observe compiler error.

---

## 5.7 Reflection API

- [ ] **Purpose:** Inspect and modify code behavior at runtime.
- [ ] **Core classes:** `Class`, `Field`, `Method`, `Constructor`.
- [ ] **Access modifiers:** Use `setAccessible(true)` to bypass restrictions.
- [ ] **Practical uses:** Frameworks, dependency injection, annotations, testing.
- [ ] **Performance considerations:** Reflection is slower and should be used wisely.

### 🧩 Practical Tasks 5.7

1. **Class info:**  
   Print all methods and fields of a class using reflection.

2. **Field modification:**  
   Modify a private field value at runtime.

3. **Dynamic method call:**  
   Invoke a method by name using reflection.

4. **Constructor usage:**  
   Create an object dynamically via `getConstructor()` and `newInstance()`.

5. **Annotation read:**  
   Retrieve custom annotation data from a class.

---

## 5.8 Modules (Java 9+)

- [ ] **Modular system:** Organize code into explicit modules.
- [ ] **`module-info.java`:** Defines exported packages and dependencies.
- [ ] **Exports/imports:** `exports`, `requires`, `opens`.
- [ ] **Benefits:** Improved encapsulation and startup performance.

### 🧩 Practical Tasks 5.8

1. **Create module:**  
   Create a simple module `com.example.utils` and export a package.

2. **Use another module:**  
   Create a second module `com.example.app` that requires the first.

3. **Encapsulation test:**  
   Try accessing a non-exported class — see compiler error.

4. **Reflection access:**  
   Use `opens` to make a package accessible to reflection.

5. **Multi-module project:**  
   Build a small two-module project in IntelliJ or CLI.

---

## 5.9 Pattern Matching and Switch Expressions (Java 14+)

- [ ] **Pattern matching:** Simplifies type checks and casting.
- [ ] **`instanceof` pattern matching:** `if (obj instanceof String s)` — direct use of variable.
- [ ] **Switch expressions:** Use `yield` to return values.
- [ ] **Arrow syntax:** Cleaner and safer `switch` statements.
- [ ] **Use cases:** Replace complex `if-else` logic.

### 🧩 Practical Tasks 5.9

1. **Instanceof pattern:**  
   Simplify type checking with pattern variables.

2. **Switch expression:**  
   Convert an old-style `switch` to the new arrow syntax.

3. **Yield value:**  
   Use a `switch` expression to assign a message based on a day of the week.

4. **Combined patterns:**  
   Match multiple constants with `case MONDAY, FRIDAY ->`.

5. **Null handling:**  
   Add a default branch to handle `null` safely.

---

## 🧠 Summary Practice Tasks

1. **Employee manager:**  
   Use Streams, lambdas, and Optional to manage employees — filtering, grouping, and salary averaging.

2. **Generic repository:**  
   Use generics + reflection to build a lightweight repository storing any entity type.

3. **Finance app:**  
   Use BigDecimal, records, and Streams to track expenses and monthly summaries.

4. **Math engine:**  
   Implement a functional-style calculator using lambdas and method references.

5. **Module-based CLI app:**  
   Build a small modular console app that demonstrates sealed classes and records.

---

✅ **End of Section 5 — Advanced Java Programming**  
Next: [6. Concurrent and Asynchronous Programming in Java →](6_concurrency_and_async.md)
