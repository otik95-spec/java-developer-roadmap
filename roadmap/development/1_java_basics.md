# 1️⃣ Java Programming Basics

---

## 1.1 Environment Setup

- [+] **Install JDK:** Download and install the Java Development Kit (JDK) of the appropriate version.
- [+] **Configure environment variables:** Add paths (`JAVA_HOME`, `PATH`) to use JDK from the command line.
- [+] **Install IDE:** Choose and install an Integrated Development Environment (IDE), such as IntelliJ IDEA, for comfortable coding.
- [+] **First program (Hello World):** Verify your setup by creating and running a simple **Hello World** program.

### 🧩 Practical Tasks 1.1

1. **Hello World in a text editor:**  
   Create a file `Hello.java` in a text editor containing a program that prints "Hello World".  
   Compile it using `javac Hello.java` and run it with `java Hello` from the terminal.

2. **Hello World in IDE:**  
   Create a class with a `main` method in your IDE that prints "Hello World" to the console.  
   Run the program to verify it works.

---

## 1.2 Program Structure and Basic Syntax

- [ ] **Structure of a Java program:** Understanding the concept of a class and the `main` method. Syntax rules: curly braces, semicolons, and case sensitivity.
- [ ] **First Java program:** Create and run the Hello World program, reviewing each line of code.
- [ ] **Comments:** Use single-line (`//`) and multi-line (`/* ... */`) comments to document your code.

### 🧩 Practical Tasks 1.2

1. **Simple greeting:** Write a program that prints your own greeting, e.g. `Hello, my name is <Your Name>!`
2. **Multi-line output:** Create a program that prints several lines of text (e.g. a poem or quote) with proper formatting.
3. **Comments:** Add comments explaining each line of your code and confirm that they don’t affect execution.
4. **Display quotes:** Print `He said "Java is fun"` — ensure the quotes displays correctly (use `\"`).
5. **Error check:** Intentionally break your code (e.g. remove a brace or rename `main`) and compile it. Note the error message, then fix it.

---

## 1.3 Variables and Data Types

- [ ] **Primitive data types:** Overview of types (`int`, `double`, `char`, `boolean`, etc.), their ranges, and memory size.
- [ ] **Declaring and initializing variables:** Naming conventions, value assignment, and `var` keyword.
- [ ] **Constants (`final`):** Creating immutable values and naming conventions.
- [ ] **Type casting:** Implicit and explicit conversions, data loss during casting.

### 🧩 Practical Tasks 1.3

1. **Print variables:** Declare variables of various types and print them in one line, then line by line.
2. **Circle area:** Calculate the area of a circle with `double radius = 5.0` using `area = Math.PI * radius * radius`.
3. **Casting:** Try assigning a `double` to an `int` variable — fix it with explicit casting.
4. **Constants:** Declare `final int MAX_VALUE = 100`, then try changing it and observe the compiler error.
5. **Swap values:** Swap two integers `a = 5`, `b = 8` using a temporary variable.

---

## 1.4 Input and Output

- [ ] **Console output:** Use `System.out.print()` and `System.out.println()`, string concatenation for messages.
- [ ] **Console input:** Use the `Scanner` class (`java.util.Scanner`) with methods `nextInt()`, `nextDouble()`, `nextLine()`.
- [ ] **Interactive programs:** Request user input and display calculated results.

### 🧩 Practical Tasks 1.4

1. **Personal greeting:** Ask for the user’s name and greet them: `Hello, <name>! Welcome to Java.`
2. **Sum of two numbers:** Read two integers and display their sum: `5 + 7 = 12`.
3. **Temperature converter:** Convert Celsius to Fahrenheit using `F = (9.0/5) * C + 32`.
4. **Rectangle area:** Ask for sides of a rectangle, then print its area and perimeter.
5. **Time converter:** Convert total seconds to hours, minutes, and seconds.

---

## 1.5 Operators and Expressions

- [ ] **Arithmetic operators:** `+`, `-`, `*`, `/`, `%`, order of operations, parentheses.
- [ ] **Increment/decrement:** `++`, `--`, prefix vs postfix.
- [ ] **Assignment operators:** `=`, `+=`, `-=`, `*=`, `/=`.
- [ ] **Comparison and logical operators:** `==`, `!=`, `>`, `<`, `>=`, `<=`, and `&&`, `||`, `!`.
- [ ] **Expression building:** Combine operators, understand precedence and type conversions.

### 🧩 Practical Tasks 1.5

1. **Rectangle math:** Compute area and perimeter from width and height.
2. **Currency converter:** Convert EUR to USD given `rate = 1.16`.
3. **Days and weeks:** Given `int days = 16`, compute full weeks and remaining days.
4. **Assignment operations:** Perform chained operations starts from `int x = 5`.
5. **Average value:** Calculate integer and floating-point averages for `a=7, b=11, c=2`.

---

## 1.6 Conditional Statements

- [ ] **`if` and `else`:** Execute code blocks conditionally.
- [ ] **Comparison and logic:** Use conditions (`<`, `>`, `==`, `&&`, `||`, `!`) for decision-making.
- [ ] **Chained and nested conditions:** `if ... else if ... else`.
- [ ] **Ternary operator (`?:`):** Simplify basic conditions.
- [ ] **`switch`:** Multi-branch control structure for values like `int`, `char`, or `String`.

### 🧩 Practical Tasks 1.6

1. **Positive or negative:** Determine if a number is positive, negative, or zero.
2. **Even or odd:** Check if an integer is even or odd using `% 2`.
3. **Maximum of three:** Find the largest of three numbers.
4. **Days of the week (switch):** Map numbers 1–7 to weekday names.
5. **Leap year:** Check if a year is leap.

---

## 1.7 Loops

- [ ] **`while` loop:** Repeats while a condition is true.
- [ ] **`do...while`:** Executes at least once.
- [ ] **`for` loop:** Counter-controlled iteration.
- [ ] **Nested loops:** Loops inside loops.
- [ ] **`break` and `continue`:** Interrupt or skip iterations.

### 🧩 Practical Tasks 1.7

1. **Numbers (while):** Print all numbers from 1 to N.
2. **Sum 1..N:** Compute sum of numbers from 1 to N using `for`.
3. **Factorial:** Calculate `n!` with a loop.
4. **Multiplication table:** Print table for a given integer.
5. **Triangle of stars:** Print a triangle pattern of height H using nested loops.

---

## 1.8 Arrays

- [ ] **Array declaration:** Create arrays, define size and type.
- [ ] **Initialization and defaults:** Default values for array types.
- [ ] **Access elements:** Indexing, `length`, `ArrayIndexOutOfBoundsException`.
- [ ] **Array operations:** Sum, average, min, max.
- [ ] **Multidimensional arrays:** Matrices and nested loops.

### 🧩 Practical Tasks 1.8

1. **Array output:** Print elements in order and reverse.
2. **Min and max:** Find smallest and largest element.
3. **Average:** Compute mean and count elements greater than average.
4. **Linear search:** Search for a name in a string array.
5. **Array reversal:** Reverse array `{3, 1, 4, 1, 5, 9}`.

---

## 🧠 Summary Practice Tasks

1. **Continuous input (min/max):** Accept integers until `0` entered; print min and max.
2. **Array analysis:** Input array size, fill with numbers, and print all above-average values.
3. **Prime check:** Determine if a number is prime.
4. **Matrix row sums:** Compute row/column sums of a 3×3 matrix.
5. **Fibonacci series:** Print the first N Fibonacci numbers.

---

✅ **End of Section 1 — Java Programming Basics**  
Next: [2. Object-Oriented Programming in Java →](2_object_oriented_programming.md)
