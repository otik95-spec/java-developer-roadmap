# 6️⃣ Concurrent and Asynchronous Programming in Java

---

## 6.1 Introduction to Concurrency

- [ ] **Definition:** Concurrency means performing multiple tasks simultaneously.
- [ ] **Threads:** Basic unit of execution in Java.
- [ ] **Processes vs threads:** Understanding differences and when to use each.
- [ ] **Main thread:** Every Java program starts with one main thread.
- [ ] **Thread states:** `NEW`, `RUNNABLE`, `BLOCKED`, `WAITING`, `TERMINATED`.

### 🧩 Practical Tasks 6.1

1. **Thread info:**  
   Print current thread name using `Thread.currentThread().getName()`.

2. **Simple thread:**  
   Create a class extending `Thread` that prints numbers 1–5.

3. **Runnable interface:**  
   Implement a `Runnable` that prints messages and start it via `new Thread(runnable).start()`.

4. **Multiple threads:**  
   Start 3 threads simultaneously and observe interleaved output.

5. **Sleep & join:**  
   Use `Thread.sleep()` and `join()` to control execution order.

---

## 6.2 Thread Lifecycle and Management

- [ ] **Thread creation:** `Thread`, `Runnable`, `Callable`, and lambdas.
- [ ] **Lifecycle control:** Start, sleep, interrupt, join.
- [ ] **Daemon threads:** Background tasks like GC or monitoring.
- [ ] **Thread priority:** `setPriority()` — rarely used but useful in some cases.

### 🧩 Practical Tasks 6.2

1. **Interrupt handling:**  
   Create a thread that runs an infinite loop and exits when interrupted.

2. **Daemon example:**  
   Run a daemon thread that prints timestamps every second until the main thread finishes.

3. **Callable:**  
   Use `Callable<Integer>` and `Future` to return computation results.

4. **Thread naming:**  
   Assign custom names to multiple threads and print them.

5. **Lifecycle test:**  
   Observe thread state transitions with `getState()`.

---

## 6.3 Synchronization

- [ ] **Race condition:** When multiple threads modify shared data concurrently.
- [ ] **Synchronized keyword:** Prevents concurrent access to code blocks or methods.
- [ ] **Locks:** `ReentrantLock`, `tryLock()`, and `unlock()`.
- [ ] **Volatile:** Guarantees visibility but not atomicity.
- [ ] **Atomic classes:** `AtomicInteger`, `AtomicBoolean`, etc.

### 🧩 Practical Tasks 6.3

1. **Race condition demo:**  
   Create two threads incrementing a shared counter — demonstrate incorrect results without synchronization.

2. **Synchronized fix:**  
   Fix the above issue using `synchronized` block or method.

3. **Lock usage:**  
   Replace `synchronized` with `ReentrantLock` and experiment with `tryLock()`.

4. **Volatile example:**  
   Use a `volatile` flag to stop a running thread safely.

5. **Atomic variable:**  
   Replace normal counter with `AtomicInteger`.

---

## 6.4 Inter-Thread Communication

- [ ] **wait() / notify():** Basic mechanism for coordinating threads.
- [ ] **Producer-consumer problem:** Common concurrency example.
- [ ] **BlockingQueue:** Simplified approach with built-in synchronization.
- [ ] **Semaphore and CountDownLatch:** Coordination tools for thread control.

### 🧩 Practical Tasks 6.4

1. **Wait/notify:**  
   Create a producer-consumer system using shared buffer with `wait()` and `notify()`.

2. **BlockingQueue:**  
   Re-implement the same using `ArrayBlockingQueue`.

3. **CountDownLatch:**  
   Wait for 3 worker threads to complete before continuing.

4. **Semaphore:**  
   Allow only 2 threads to access a shared resource simultaneously.

5. **CyclicBarrier:**  
   Coordinate 3 threads to reach a synchronization point.

---

## 6.5 Executors and Thread Pools

- [ ] **Executor framework:** Manage threads efficiently.
- [ ] **Types:** `FixedThreadPool`, `CachedThreadPool`, `SingleThreadExecutor`, `ScheduledThreadPool`.
- [ ] **Submitting tasks:** `execute()` and `submit()`.
- [ ] **Future and Callable:** Get async results.
- [ ] **Shutdown:** Properly terminate executors.

### 🧩 Practical Tasks 6.5

1. **Fixed thread pool:**  
   Submit 5 tasks to a pool of 2 threads and observe task scheduling.

2. **Callable + Future:**  
   Calculate factorial asynchronously and get result with `future.get()`.

3. **Scheduled executor:**  
   Print a message every 2 seconds using `scheduleAtFixedRate()`.

4. **Shutdown handling:**  
   Gracefully stop a thread pool with `shutdown()` and `awaitTermination()`.

5. **Cached pool:**  
   Use `newCachedThreadPool()` for dynamic scaling and test with 100 tasks.

---

## 6.6 Concurrent Collections

- [ ] **Thread-safe collections:** `ConcurrentHashMap`, `CopyOnWriteArrayList`, `BlockingQueue`.
- [ ] **When to use:** Multi-threaded environments with shared data.
- [ ] **Performance vs synchronization:** Trade-offs in concurrent containers.
- [ ] **Iterating safely:** Avoid `ConcurrentModificationException`.

### 🧩 Practical Tasks 6.6

1. **ConcurrentMap:**  
   Use `ConcurrentHashMap` to count word frequency from multiple threads.

2. **CopyOnWriteArrayList:**  
   Add/remove elements from multiple threads and print final size.

3. **BlockingQueue:**  
   Simulate a simple task queue processed by worker threads.

4. **Concurrent set:**  
   Create a thread-safe set using `ConcurrentHashMap.newKeySet()`.

5. **Iteration safety:**  
   Iterate over concurrent collection while other threads modify it.

---

## 6.7 CompletableFuture (Async Programming)

- [ ] **Purpose:** Asynchronous programming without explicit threads.
- [ ] **Creating tasks:** `supplyAsync()`, `runAsync()`.
- [ ] **Chaining:** `thenApply()`, `thenAccept()`, `thenCompose()`, `thenCombine()`.
- [ ] **Error handling:** `exceptionally()` and `handle()`.
- [ ] **Combining futures:** Merge multiple async operations.

### 🧩 Practical Tasks 6.7

1. **Async computation:**  
   Use `CompletableFuture.supplyAsync()` to perform a background calculation.

2. **Chaining tasks:**  
   Chain transformations — e.g., read data → transform → print result.

3. **Combine futures:**  
   Run two independent tasks and combine their results using `thenCombine()`.

4. **Exception handling:**  
   Simulate a failure and handle it with `exceptionally()`.

5. **Parallel API calls:**  
   Launch 3 async calls (simulated with `sleep()`) and merge their results.

---

## 6.8 Parallel Streams

- [ ] **Parallel processing:** Use multiple cores automatically.
- [ ] **When to use:** CPU-bound operations with large datasets.
- [ ] **Limitations:** Avoid shared mutable state.
- [ ] **ForkJoinPool:** Underlying mechanism for parallel streams.

### 🧩 Practical Tasks 6.8

1. **Parallel computation:**  
   Use `parallelStream()` to calculate sum of 1..1_000_000.

2. **Performance test:**  
   Compare runtime of sequential vs parallel stream for large dataset.

3. **Side effects:**  
   Demonstrate issues with shared mutable variables in parallel streams.

4. **Custom pool:**  
   Configure `ForkJoinPool` with custom parallelism level.

5. **Nested streams:**  
   Experiment with nested parallel operations and observe performance.

---

## 6.9 Virtual Threads (Java 21+)

- [ ] **Definition:** Lightweight threads managed by JVM, not OS.
- [ ] **Benefits:** Handle thousands of concurrent tasks efficiently.
- [ ] **Usage:** `Thread.ofVirtual().start(...)`.
- [ ] **Compatibility:** Works with existing APIs (e.g., `Executors.newVirtualThreadPerTaskExecutor()`).
- [ ] **Best practices:** Avoid blocking operations on shared resources.

### 🧩 Practical Tasks 6.9

1. **Basic virtual thread:**  
   Create and start a virtual thread printing its name.

2. **Multiple virtual threads:**  
   Launch 1000 virtual threads performing small tasks.

3. **Executor:**  
   Use `Executors.newVirtualThreadPerTaskExecutor()` to handle async tasks.

4. **Comparison:**  
   Compare performance with classic thread pool.

5. **Blocking test:**  
   Simulate a blocking I/O call in a virtual thread and measure impact.

---

## 🧠 Summary Practice Tasks

1. **Bank system:**  
   Multiple threads withdraw and deposit from shared accounts using synchronization.

2. **Web scraper:**  
   Use `ExecutorService` and `CompletableFuture` to fetch multiple URLs concurrently.

3. **Parallel data processing:**  
   Process large data sets using parallel streams with performance comparison.

4. **Real-time logger:**  
   Use `BlockingQueue` to implement async logging service.

5. **Virtual-thread demo:**  
   Build a demo comparing 1000 classic threads vs 1000 virtual threads.

---

✅ **End of Section 6 — Concurrent and Asynchronous Programming in Java**  
Next: [7. Working with Databases, JDBC, JPA, and Hibernate →](./7_databases_jdbc_jpa_hibernate.md)
