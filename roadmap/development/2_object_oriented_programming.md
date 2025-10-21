# 2️⃣ Object-Oriented Programming in Java

---

## 2.1 Introduction to OOP Concepts

- [ ] **Object and class:** Understanding the difference between a class (template) and an object (instance).
- [ ] **Core OOP principles:** Encapsulation, inheritance, polymorphism, and abstraction.
- [ ] **OOP benefits:** Modularity, reusability, maintainability, and extensibility.

### 🧩 Practical Tasks 2.1

1. **Real-world example:**  
   Describe three real-world objects (e.g., Car, Book, Person) in terms of fields and methods.  
   Example: `Car` → fields: brand, speed, fuel; methods: drive(), refuel(), brake().

2. **Class-to-object thinking:**  
   Choose one of your examples and sketch its structure in pseudocode (without implementing yet).

---

## 2.2 Creating Classes and Objects

- [ ] **Declaring a class:** Syntax, naming conventions, and structure.
- [ ] **Creating objects:** Using the `new` keyword and constructors.
- [ ] **Accessing members:** Fields and methods through the dot operator (`object.field`).
- [ ] **Constructors:** Default and parameterized constructors.
- [ ] **The `this` keyword:** Referring to the current object.

### 🧩 Practical Tasks 2.2

1. **Simple class:**  
   Create a `Car` class with fields: `brand`, `year`, and `speed`. Add a method `displayInfo()`.

2. **Constructor practice:**  
   Add a constructor to set initial values for all fields.

3. **Modify object:**  
   Create two `Car` objects and print their data. Then change the speed of one and print it again.

4. **Use of `this`:**  
   Add a method `accelerate(int value)` that increases `speed` using `this.speed += value;`.

---

## 2.3 Encapsulation

- [ ] **Private fields:** Restrict access to internal data.
- [ ] **Getters and setters:** Controlled access to private variables.
- [ ] **Data validation:** Add checks inside setters to prevent invalid data.
- [ ] **Encapsulation benefits:** Maintain consistency and protect class invariants.

### 🧩 Practical Tasks 2.3

1. **Encapsulate:**  
   Make all fields in `Car` private and add getters and setters.

2. **Validation:**  
   Prevent setting a negative speed. Print a warning instead.

3. **Access control:**  
   Try accessing fields directly from `main()` — confirm compiler error and fix it using accessors.

4. **`toString()`:**  
   Override `toString()` to print the object in a readable format.

---

## 2.4 Inheritance

- [ ] **Inheritance basics:** Use `extends` to derive a subclass from a superclass.
- [ ] **Protected members:** Allow access in subclasses.
- [ ] **Method overriding:** Redefine behavior in a child class.
- [ ] **`super` keyword:** Call parent constructors or methods.
- [ ] **Class hierarchy:** Building multi-level inheritance trees.

### 🧩 Practical Tasks 2.4

1. **Vehicle hierarchy:**  
   Create a superclass `Vehicle` with fields `speed` and `capacity`.  
   Extend it with `Car` and `Bicycle` classes, adding specific fields (e.g. `doors`, `type`).

2. **Constructor chaining:**  
   Add constructors calling `super(...)` for inherited fields.

3. **Overriding:**  
   Add a `move()` method in `Vehicle` and override it in `Car` and `Bicycle`.

4. **Test hierarchy:**  
   Create objects of each type and call `move()`. Observe the differences.

---

## 2.5 Polymorphism

- [ ] **Definition:** One interface, multiple implementations.
- [ ] **Overriding vs overloading:** Redefine vs. redefine with new parameters.
- [ ] **Dynamic binding:** Runtime method resolution.
- [ ] **Upcasting and downcasting:** Working with parent references and specific behavior.
- [ ] **`instanceof`:** Check object type before casting.

### 🧩 Practical Tasks 2.5

1. **Method overloading:**  
   Create a `Calculator` class with several `add()` methods for `int`, `double`, and arrays.

2. **Method overriding:**  
   Continue using your `Vehicle` hierarchy — override `move()` in each subclass.

3. **Polymorphism test:**  
   Store `Vehicle`, `Car`, and `Bicycle` objects in an array of type `Vehicle[]`.  
   Call `move()` for each element and see how Java determines which one to run.

4. **Type check:**  
   Use `instanceof` to print each object’s type before calling `move()`.

---

## 2.6 Abstraction

- [ ] **Abstract classes:** Classes that cannot be instantiated but may contain both abstract and concrete methods.
- [ ] **Interfaces:** Define a contract that classes must implement.
- [ ] **`implements` keyword:** Linking a class to one or multiple interfaces.
- [ ] **Default methods:** Implemented methods in interfaces (Java 8+).
- [ ] **Functional interface:** Interface with exactly one abstract method.

### 🧩 Practical Tasks 2.6

1. **Abstract class:**  
   Create an abstract class `Shape` with an abstract method `double area()`.

2. **Implementations:**  
   Create subclasses `Circle` and `Rectangle` that implement `area()`.

3. **Interface example:**  
   Create an interface `Movable` with a method `move()`.  
   Implement it in `Car` and `Bicycle`.

4. **Interface + inheritance:**  
   Combine inheritance and interface in one example.  
   For instance, `ElectricCar extends Car implements Chargeable`.

---

## 2.7 Composition and Aggregation

- [ ] **Composition:** One object “owns” another (lifecycle dependency).
- [ ] **Aggregation:** Objects are linked but independent.
- [ ] **Usage scenarios:** Model real relationships like “Person has an Address” or “Car has an Engine.”

### 🧩 Practical Tasks 2.7

1. **Composition:**  
   Create classes `Engine` and `Car`.  
   A `Car` object contains an `Engine` field. Initialize it in the constructor.

2. **Aggregation:**  
   Create a `Teacher` and a `School` where multiple teachers belong to the same school.

3. **Lifecycle:**  
   Test that deleting a `Car` implies deleting its `Engine`, but not deleting a `Teacher` when `School` is removed.

---

## 2.8 Static and Instance Members

- [ ] **Instance vs static:** Fields and methods belonging to an object vs. a class.
- [ ] **Static blocks:** Initialization before class usage.
- [ ] **Static constants:** `public static final` fields for global constants.
- [ ] **Static methods:** Utility behavior that doesn’t depend on object state.

### 🧩 Practical Tasks 2.8

1. **Static counter:**  
   Add a static field `count` in `Car` to track how many cars are created.

2. **Static utility:**  
   Create a `MathUtil` class with static methods `min(int, int)` and `max(int, int)`.

3. **Constant:**  
   Add a `public static final double PI = 3.14159` constant to `MathUtil` and use it for circle area calculation.

---

## 2.9 Packages and Access Modifiers

- [ ] **Packages:** Organize classes by topic (e.g. `com.company.model`).
- [ ] **Importing:** Using classes from other packages.
- [ ] **Access levels:** `public`, `protected`, `private`, and package-private.
- [ ] **Package structure:** Folder hierarchy matches package names.

### 🧩 Practical Tasks 2.9

1. **Organize classes:**  
   Move your `Car`, `Vehicle`, and `Bicycle` into a package `transport`.

2. **Import:**  
   In a separate `Main` class, import and use them.

3. **Access control:**  
   Experiment with access modifiers to understand visibility across packages.

---

## 🧠 Summary Practice Tasks

1. **Library system:**  
   Create classes `Book`, `Author`, and `Library`.  
   Each library contains a list of books, each book has an author.  
   Implement methods to add books, display all, and find by author.

2. **Bank account:**  
   Create `Account` class with deposit, withdraw, and balance methods.  
   Add validation to prevent overdraft.

3. **Inheritance + interface:**  
   Model a `Device` class with subclasses `Phone` and `Laptop`,  
   and an interface `Chargeable` with a `charge()` method.

4. **Zoo management:**  
   Abstract class `Animal` with `makeSound()`.  
   Implement `Dog`, `Cat`, and `Bird`, each overriding behavior.  
   Store them in a list and call `makeSound()` polymorphically.

---

✅ **End of Section 2 — Object-Oriented Programming in Java**  
Next: [3. Java Language Mechanisms →](3_language_mechanics.md)
