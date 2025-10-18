# 3️⃣ Java Language Mechanisms

---

## 3.1 The `static`, `final`, and `var` Keywords

- [ ] **`static`:** Belongs to a class, not an instance.
- [ ] **`final`:** Prevents modification of variables, methods, or classes.
- [ ] **`var` (Java 10+):** Local variable type inference.
- [ ] **Constants:** Declaring immutable class-level values (`public static final`).
- [ ] **Static initialization blocks:** Run once when the class is loaded.

### 🧩 Practical Tasks 3.1

1. **Static counter:**  
   Add a static field `instanceCount` to a class and increment it in the constructor.  
   Verify it tracks all instances created.

2. **Constants:**  
   Create a class `MathConstants` with constants `PI`, `E`, and `G`. Use them in calculations.

3. **Final behavior:**  
   Create a `final` variable, method, and class. Try modifying or extending them. Observe compiler errors.

4. **Static block:**  
   Add a static block that prints a message before any instance is created.

5. **`var` usage:**  
   Declare a few local variables with `var` and see how Java infers their types.

---

## 3.2 Generics

- [ ] **Generics motivation:** Type safety and code reusability.
- [ ] **Parameterized types:** `List<String>`, `Map<Integer, String>`.
- [ ] **Generic classes:** `class Box<T>` and `Box<Integer>`.
- [ ] **Generic methods:** `<T> void print(T value)`.
- [ ] **Wildcards:** `?`, `? extends`, and `? super`.
- [ ] **Type erasure:** Compile-time enforcement and runtime behavior.

### 🧩 Practical Tasks 3.2

1. **Generic class:**  
   Implement `Box<T>` with methods `setValue(T)` and `getValue()`.

2. **Generic method:**  
   Write a method `<T> void printArray(T[] array)` that prints all elements.

3. **Wildcard example:**  
   Write a method `sumNumbers(List<? extends Number> list)` that calculates total.

4. **Practice inheritance:**  
   Create `List<Integer>` and `List<Double>` and pass them to your wildcard method.

5. **Type safety test:**  
   Compare using `ArrayList` without generics vs. `ArrayList<String>`.

---

## 3.3 Exception Handling

- [ ] **Exceptions:** What they are and why they exist.
- [ ] **Try-catch-finally:** Handling runtime errors safely.
- [ ] **Checked vs unchecked exceptions:** `IOException` vs `NullPointerException`.
- [ ] **Throwing exceptions:** `throw` and `throws`.
- [ ] **Custom exceptions:** Create your own subclass of `Exception`.

### 🧩 Practical Tasks 3.3

1. **Divide by zero:**  
   Handle `ArithmeticException` when dividing integers.

2. **File not found:**  
   Read a non-existent file and handle `IOException`.

3. **Custom exception:**  
   Create `NegativeAmountException` and throw it if a withdrawal amount is negative.

4. **Finally block:**  
   Demonstrate code in `finally` always executes.

5. **Multiple catch:**  
   Catch both `IOException` and `NumberFormatException` in one example.

---

## 3.4 Inner and Nested Classes

- [ ] **Inner classes:** Defined inside another class and can access its members.
- [ ] **Static nested classes:** Belong to the outer class but don’t access instance members.
- [ ] **Anonymous classes:** Create quick implementations without naming them.
- [ ] **Local classes:** Defined inside methods.
- [ ] **Use cases:** Grouping helper logic within related classes.

### 🧩 Practical Tasks 3.4

1. **Member inner class:**  
   Create `Outer` with an inner class `Inner` that prints a private field of the outer class.

2. **Static nested:**  
   Create a static nested class with a `static` method accessible without an instance.

3. **Anonymous class:**  
   Implement `Runnable` anonymously and print "Running from anonymous class!".

4. **Local class:**  
   Define a small class inside a method and use it immediately.

5. **GUI-like example:**  
   Create an interface `ButtonClickListener` and use an anonymous class to implement it.

---

## 3.5 Enumerations (`enum`)

- [ ] **Defining enums:** Fixed set of constants with type safety.
- [ ] **Using enums in switch:** Replace magic numbers and strings with enums.
- [ ] **Enum methods:** `values()`, `ordinal()`, and `valueOf()`.
- [ ] **Fields and constructors in enums:** Add custom data and behavior.
- [ ] **Enum best practices:** Grouping related constants logically.

### 🧩 Practical Tasks 3.5

1. **Basic enum:**  
   Create an enum `Day` with constants `MONDAY`...`SUNDAY` and print them all.

2. **Enum in switch:**  
   Use a `switch` statement to print a message depending on the day.

3. **Enum with fields:**  
   Create enum `Season` with average temperature field and a getter.

4. **Custom method:**  
   Add a method to `Season` that prints advice like “Wear a jacket” for winter.

5. **Enum inside class:**  
   Create a `Task` class that contains an enum `Status` (`NEW`, `IN_PROGRESS`, `DONE`).

---

## 3.6 Annotations

- [ ] **Purpose:** Metadata that provides information to the compiler or runtime.
- [ ] **Built-in annotations:** `@Override`, `@Deprecated`, `@SuppressWarnings`.
- [ ] **Custom annotations:** Create your own with `@interface`.
- [ ] **Annotation parameters:** Define values inside annotations.
- [ ] **Retention policies:** `SOURCE`, `CLASS`, and `RUNTIME`.

### 🧩 Practical Tasks 3.6

1. **@Override:**  
   Override a superclass method and annotate it properly.

2. **@Deprecated:**  
   Mark an old method as deprecated and explain how the IDE warns about it.

3. **@SuppressWarnings:**  
   Suppress a compiler warning for unchecked operations.

4. **Custom annotation:**  
   Create `@Author(name = "John Doe")` and apply it to a class.

5. **Reflection usage:**  
   Retrieve and print your custom annotation value using reflection.

---

## 3.7 The `Object` Class and Its Methods

- [ ] **Inheritance root:** Every class implicitly extends `Object`.
- [ ] **Important methods:**
    - `toString()`
    - `equals()`
    - `hashCode()`
    - `clone()`
    - `getClass()`
- [ ] **Contract between `equals()` and `hashCode()`.**
- [ ] **Override properly:** Maintain consistency and avoid bugs in collections.

### 🧩 Practical Tasks 3.7

1. **`toString()` override:**  
   Override `toString()` in one of your classes for readable output.

2. **`equals()` and `hashCode()`:**  
   Compare objects by fields (e.g., `name`, `age`). Ensure they work in `HashSet`.

3. **`clone()`:**  
   Make a class implement `Cloneable` and test shallow vs deep cloning.

4. **`getClass()`:**  
   Print runtime class information for any object.

5. **Equality test:**  
   Compare two different instances with the same field values — test reference vs logical equality.

---

## 3.8 Immutability

- [ ] **Immutable class:** Fields cannot change after object creation.
- [ ] **Rules:** All fields `private final`, no setters, defensive copying in constructors.
- [ ] **Examples:** `String`, wrapper types (`Integer`, `Double`).
- [ ] **Benefits:** Thread safety and predictability.

### 🧩 Practical Tasks 3.8

1. **Immutable class:**  
   Create an immutable `Person` class with `name` and `age`.

2. **Try to mutate:**  
   Attempt to change fields — verify it’s impossible.

3. **Defensive copy:**  
   In a class with mutable fields (like a list), return a copy instead of direct reference.

4. **Compare with mutable:**  
   Implement a mutable version and note the difference in behavior.

---

## 🧠 Summary Practice Tasks

1. **Bank simulation:**  
   Use enums for account types, custom exceptions for invalid operations, and generics for transaction storage.

2. **Task manager:**  
   Implement `Task` with enum `Status`, custom annotation `@Author`, and override `equals()`.

3. **Generic repository:**  
   Create a generic class `Repository<T>` that can store any entity type and print all items.

4. **Reflection experiment:**  
   Use annotations, `getClass()`, and reflection to display metadata for an object.

5. **Immutability practice:**  
   Create immutable `Coordinates` used in a `Map` class that can’t be modified after creation.

---

✅ **End of Section 3 — Java Language Mechanisms**  
Next: [4. Working with Utilities and Core APIs →](./4_utilities_and_api.md)
