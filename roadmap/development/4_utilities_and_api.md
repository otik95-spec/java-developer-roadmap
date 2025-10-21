# 4️⃣ Working with Utilities and Core APIs

---

## 4.1 Working with Strings

- [ ] **String basics:** Creating and concatenating strings.
- [ ] **Immutability:** Understanding that strings cannot be modified once created.
- [ ] **Common methods:** `length()`, `charAt()`, `substring()`, `indexOf()`, `equals()`, `contains()`, `replace()`, `toUpperCase()`, `toLowerCase()`.
- [ ] **StringBuilder / StringBuffer:** Mutable alternatives for string concatenation.
- [ ] **String formatting:** `String.format()` and text blocks (Java 15+).

### 🧩 Practical Tasks 4.1

1. **Basic operations:**  
   Create a string and demonstrate concatenation, substring, and case conversion.

2. **Character count:**  
   Count how many times a character appears in a sentence.

3. **Palindrome check:**  
   Write a program that checks if a word or phrase is a palindrome.

4. **Using `StringBuilder`:**  
   Build a sentence from separate words using `StringBuilder`.

5. **Formatting output:**  
   Use `String.format()` to print:  
   `Name: John, Age: 25, Balance: 1234.56 USD`.

---

## 4.2 The Java Collections Framework (JCF)

- [ ] **Purpose:** Unified architecture for storing and manipulating groups of objects.
- [ ] **Main interfaces:** `Collection`, `List`, `Set`, `Queue`, and `Map`.
- [ ] **Implementations:** `ArrayList`, `LinkedList`, `HashSet`, `TreeSet`, `HashMap`, `LinkedHashMap`.
- [ ] **Iterators:** Traversing collections using `Iterator` and enhanced `for`.
- [ ] **Comparator and Comparable:** Sorting and custom comparison logic.

### 🧩 Practical Tasks 4.2

1. **List practice:**  
   Create a list of names, add/remove elements, and print them in reverse order.

2. **Set usage:**  
   Store unique words from a sentence and print them alphabetically.

3. **Map operations:**  
   Create a dictionary where key = word and value = translation. Print all pairs.

4. **Sorting:**  
   Create a list of integers and sort it using both natural order and a custom comparator.

5. **Frequency counter:**  
   Count how many times each word appears in a text using `Map<String, Integer>`.

---

## 4.3 Date and Time API

- [ ] **Legacy vs modern API:** `java.util.Date` vs `java.time` (Java 8+).
- [ ] **Core classes:** `LocalDate`, `LocalTime`, `LocalDateTime`, `Instant`.
- [ ] **Formatting and parsing:** `DateTimeFormatter`.
- [ ] **Duration and Period:** Calculate time differences.
- [ ] **Time zones:** `ZoneId` and `ZonedDateTime`.

### 🧩 Practical Tasks 4.3

1. **Current date/time:**  
   Display the current date, time, and date-time.

2. **Formatting:**  
   Format the current date as `yyyy-MM-dd HH:mm:ss`.

3. **Date difference:**  
   Calculate how many days remain until your next birthday.

4. **Time zone:**  
   Print the current time in three different time zones.

5. **Parsing:**  
   Parse a string date `"2025-10-12"` into `LocalDate` and print it.

---

## 4.4 File I/O (Input and Output)

- [ ] **Working with files:** Creating, reading, writing, and deleting files.
- [ ] **Core classes:** `File`, `FileReader`, `FileWriter`, `BufferedReader`, `BufferedWriter`.
- [ ] **`try-with-resources`:** Automatic resource management.
- [ ] **NIO API:** `Files`, `Paths`, and `Files.lines()` for modern file access.
- [ ] **Serialization:** Writing and reading objects using `ObjectOutputStream` and `ObjectInputStream`.

### 🧩 Practical Tasks 4.4

1. **File creation:**  
   Create a file named `notes.txt` and write several lines to it.

2. **File reading:**  
   Read and print all lines from `notes.txt`.

3. **Append mode:**  
   Add a new line at the end of the same file without overwriting it.

4. **Count words in file:**  
   Read a text file and count how many words it contains.

5. **Object serialization:**  
   Save a `Person` object to a file and read it back.

---

## 4.5 Regular Expressions (Regex)

- [ ] **Pattern matching:** Using `Pattern` and `Matcher` classes.
- [ ] **Basic syntax:** Character classes, quantifiers, anchors, groups.
- [ ] **Useful patterns:** Email, phone number, postal code, etc.
- [ ] **Replacing:** Using `replaceAll()` and `replaceFirst()`.
- [ ] **Validation examples:** Data input validation.

### 🧩 Practical Tasks 4.5

1. **Match email:**  
   Write a regex that validates an email address.

2. **Extract numbers:**  
   Extract all digits from a given text.

3. **Find words:**  
   Count how many words start with a capital letter.

4. **Replace:**  
   Replace all spaces with underscores.

5. **Validate phone:**  
   Create a regex for validating phone numbers in format `+1-123-456-7890`.

---

## 4.6 Wrapper Classes and Autoboxing

- [ ] **Wrapper classes:** Converting primitives to objects (`Integer`, `Double`, etc.).
- [ ] **Autoboxing and unboxing:** Automatic conversion between primitives and wrappers.
- [ ] **Parsing and conversion:** `Integer.parseInt()`, `Double.valueOf()`, etc.
- [ ] **Comparison pitfalls:** Difference between `==` and `.equals()`.

### 🧩 Practical Tasks 4.6

1. **Boxing demo:**  
   Create a list of `Integer` and add primitive ints — observe autoboxing.

2. **Parsing input:**  
   Read numeric input as a `String` and convert it to an integer.

3. **Equality check:**  
   Compare `Integer a = 1000` and `Integer b = 1000` using both `==` and `.equals()`.

4. **Wrapper methods:**  
   Use `Integer.MAX_VALUE`, `Double.MIN_VALUE`, and similar constants.

5. **Conversion practice:**  
   Convert between string, integer, and double formats.

---

## 4.7 Math and Random Utilities

- [ ] **Math class:** Common methods like `abs()`, `pow()`, `sqrt()`, `round()`, `max()`, `min()`.
- [ ] **Random number generation:** Using `Math.random()` and `Random` class.
- [ ] **SecureRandom:** For cryptographically strong random values.
- [ ] **BigDecimal:** For precise monetary calculations.

### 🧩 Practical Tasks 4.7

1. **Basic math:**  
   Calculate the area of a triangle using Heron’s formula.

2. **Random generator:**  
   Generate 10 random integers between 1 and 100.

3. **BigDecimal practice:**  
   Add, subtract, and multiply two currency amounts.

4. **Round off:**  
   Round a double to 2 decimal places.

5. **SecureRandom:**  
   Generate a random 6-digit PIN code.

---

## 4.8 System, Runtime, and Environment Classes

- [ ] **System properties:** Read values like `user.name`, `os.name`.
- [ ] **Runtime:** Execute system commands, measure performance.
- [ ] **Environment variables:** Access system environment variables.
- [ ] **Garbage collection:** Trigger using `System.gc()`.
- [ ] **Exit codes:** `System.exit(status)` usage.

### 🧩 Practical Tasks 4.8

1. **System info:**  
   Print OS name, user name, and Java version.

2. **Execution time:**  
   Measure how long a loop takes to execute using `System.currentTimeMillis()`.

3. **Runtime command:**  
   Use `Runtime.getRuntime().exec("ping google.com")` and print output.

4. **Environment variables:**  
   Print all available environment variables.

5. **GC test:**  
   Create many short-lived objects and trigger garbage collection.

---

## 🧠 Summary Practice Tasks

1. **Text file analyzer:**  
   Read a text file and print word count, line count, and unique word frequency.

2. **Contacts list:**  
   Use a `Map<String, String>` to store names and phone numbers. Implement add/search/remove options.

3. **Temperature logger:**  
   Generate random daily temperatures for a month and compute average, max, and min.

4. **Expense tracker:**  
   Use `BigDecimal` to manage a list of expenses stored in a file.

5. **Regex validator:**  
   Create a form validation program (name, email, phone) using regex patterns.

---

✅ **End of Section 4 — Working with Utilities and Core APIs**  
Next: [5. Advanced Java Programming →](5_advanced_programming.md)
