# Shared Memory Programming (pthreads)

Shared memory programming allows multiple threads to communicate efficiently, enabling parallel execution of tasks within a single process. The pthreads (POSIX threads) library provides a standard way to manage threads in multi-threaded applications.

## Key Concepts

- **Shared memory helps programs communicate faster.**  
  In a multi-threaded environment, threads share a common memory space, which allows for quick data exchange without the overhead of inter-process communication.

- **Programs may use one or more processors, and as a result, a process may have several threads.**  
  Modern computing architectures support multi-core processors, which can execute multiple threads simultaneously, improving performance and efficiency.

- **Threads are referred to as lightweight processes.**  
  Unlike traditional processes, which have separate memory and resources, threads operate within the same process and share resources, making them lightweight and efficient.

- **Threads are shared lightweight processes.**  
  This means a single process can be divided into multiple threads that run concurrently, reducing the overhead of creating and managing separate processes.

- **Threading achieves parallelism.**  
  Parallelism allows multiple tasks to be executed simultaneously, improving computational efficiency. This is crucial in high-performance applications such as gaming, scientific computing, and data processing.

- **Real-world examples of threading:**  
  - Web browsers: Each browser tab runs as a separate thread, ensuring responsiveness even when multiple pages are open.
  - Word processors: Applications like Microsoft Word use threading to handle background tasks such as spell checking and auto-saving while allowing users to continue working seamlessly.

## Conclusion

Shared memory programming using pthreads is a powerful technique for developing efficient, multi-threaded applications. By leveraging threads, programs can optimize CPU utilization, reduce execution time, and improve overall system performance.
![image](https://github.com/user-attachments/assets/7abc2b72-dfe7-4fd7-9612-b4da9c021df3)

![image](https://github.com/user-attachments/assets/137dc411-e1c1-4faa-8e69-6acb7e1b0e96)

# PThreads (POSIX Threads)
 The POSIX thread libraries are a C/C++ thread API based on standards. It enables the creation of a new concurrent process flow. It works well on multi-processor or multi-core systems, where the process flow may be scheduled to execute on another processor, increasing speed through parallel or distributed processing.
 To utilise the PThread interfaces, we must include the header pthread.h at the start of the CPP script.
 ```
   #include <pthread.h>
```

PThreads is a highly concrete multithreading system that is the UNIX system’s default standard. PThreads is an abbreviation for POSIX threads, and POSIX is an abbreviation for Portable Operating System Interface for Unix/Linux

* It is an IEEE standard for Unix-like OS.
* It is a library which can be linked with C program.
* It specifies an API for multi-threaded programming.
* It forms the basic building block for many parallel libraries like:
OpenMP, Intel thread building block.
* They are needed to implement algorithms that have irregular
decomposition and communication

## **POSIX Thread (pthread) System Calls**
Threads are lightweight processes that run concurrently within a program. The **pthread** library in C provides various system calls to create, manage, and terminate threads.

---

### **1. Creating a Thread**
#### **Function:**
```c
int pthread_create(pthread_t *thread, const pthread_attr_t *attr, void *(*start_routine)(void*), void *arg);
```
#### **Explanation:**
- `pthread_create()` is used to create a new thread.
- It returns **0** on success and a **negative value** on failure.
- **Arguments:**
  - `pthread_t *thread`: A pointer to the thread ID (used for identifying the thread later).
  - `const pthread_attr_t *attr`: Specifies thread attributes (can be NULL for default attributes).
  - `void *(*start_routine)(void*)`: Function that the thread will execute.
  - `void *arg`: Argument passed to the `start_routine` function.

---

### **2. Exiting a Thread**
#### **Function:**
```c
void pthread_exit(void *value_ptr);
```
#### **Explanation:**
- Used to terminate a thread without stopping the entire process.
- **Argument:**
  - `void *value_ptr`: Pointer to a return value (can be NULL).
- When a thread calls `pthread_exit()`, it stops execution and returns the specified value to the joining thread.

---

### **3. Joining a Thread**
#### **Function:**
```c
int pthread_join(pthread_t thread, void **value_ptr);
```
#### **Explanation:**
- The calling thread waits for a specified thread to terminate before continuing.
- **Arguments:**
  - `pthread_t thread`: The thread ID of the thread to wait for.
  - `void **value_ptr`: A pointer to the return value of the terminated thread (can be NULL).
- This function **blocks execution** until the specified thread completes.

---

### **4. POSIX Thread Synchronization**
Synchronization mechanisms such as **mutexes** are used to prevent race conditions when multiple threads access shared resources.

#### **Locking a Mutex**
##### **Function:**
```c
int pthread_mutex_lock(pthread_mutex_t *mutex);
```
##### **Explanation:**
- This function **checks if the mutex is locked**. If not, it locks the mutex and allows the calling thread to proceed.
- If the mutex is already locked, the calling thread **blocks** until the mutex is unlocked.
- Used before a thread enters its **critical section**.

#### **Try-Locking a Mutex**
##### **Function:**
```c
int pthread_mutex_trylock(pthread_mutex_t *mutex);
```
##### **Explanation:**
- Similar to `pthread_mutex_lock`, but **does not block**.
- Returns:
  - `0` if the mutex was **unlocked** and successfully locked.
  - A **non-zero** value if the mutex was already locked.

#### **Unlocking a Mutex**
##### **Function:**
```c
int pthread_mutex_unlock(pthread_mutex_t *mutex);
```
##### **Explanation:**
- Unlocks a previously locked mutex.
- Should be **called after a thread leaves its critical section** to allow other threads to proceed.

---

### **Summary**
1. **`pthread_create()`** → Creates a new thread.
2. **`pthread_exit()`** → Terminates a thread without affecting other threads.
3. **`pthread_join()`** → Waits for a thread to finish execution.
4. **`pthread_mutex_lock()`** → Locks a mutex.
5. **`pthread_mutex_trylock()`** → Attempts to lock a mutex without blocking.
6. **`pthread_mutex_unlock()`** → Unlocks a mutex.

## PThread Limitation
* Although the Pthreads implementations can, and usually co, vary in ways not specified by
the standard.
* Because of this, a program that runs fine on one platform, may fail or produce wrong results on another platform.
* For example, the maximum number of threads permitted, and the
default thread stack size are two important limits to consider when
designing your program.

# The Pthreads API

## Introduction
The POSIX Threads (Pthreads) API provides a standardized interface for creating and managing threads in Unix-based operating systems. Threads allow for concurrent execution within a program, improving efficiency and performance.

## Classification of Pthreads API
The Pthreads API can be informally divided into **four major groups**:

1. **Thread Management**
2. **Mutexes**
3. **Condition Variables**
4. **Synchronization**

## Detailed Explanation of Each Component

### 1. Thread Management
Thread management functions handle:
- Creating new threads
- Terminating threads
- Joining threads (waiting for them to complete)
- Detaching threads (allowing them to run independently)

**Key functions:**
- `pthread_create()`: Creates a new thread.
- `pthread_exit()`: Terminates the calling thread.
- `pthread_join()`: Waits for a thread to finish execution.
- `pthread_detach()`: Marks a thread as detached, so its resources are automatically freed upon termination.

### 2. Mutexes
Mutexes (short for mutual exclusion) are used to prevent multiple threads from simultaneously accessing shared resources, ensuring data integrity.

**Key functions:**
- `pthread_mutex_init()`: Initializes a mutex.
- `pthread_mutex_lock()`: Locks a mutex to prevent other threads from accessing shared resources.
- `pthread_mutex_unlock()`: Unlocks a mutex, allowing other threads to proceed.
- `pthread_mutex_destroy()`: Destroys a mutex when it is no longer needed.

### 3. Condition Variables
Condition variables enable threads to wait for specific conditions to be met before proceeding. They facilitate synchronized communication among threads that share a mutex.

**Key functions:**
- `pthread_cond_init()`: Initializes a condition variable.
- `pthread_cond_wait()`: Makes a thread wait until a specific condition is met.
- `pthread_cond_signal()`: Signals a single waiting thread to proceed.
- `pthread_cond_broadcast()`: Signals all waiting threads to proceed.
- `pthread_cond_destroy()`: Destroys a condition variable.

### 4. Synchronization
Synchronization mechanisms manage read/write locks and barriers to coordinate thread execution efficiently.

**Key functions:**
- `pthread_rwlock_init()`: Initializes a read-write lock.
- `pthread_rwlock_rdlock()`: Acquires a read lock.
- `pthread_rwlock_wrlock()`: Acquires a write lock.
- `pthread_rwlock_unlock()`: Releases a read/write lock.
- `pthread_rwlock_destroy()`: Destroys a read-write lock.
- `pthread_barrier_init()`: Initializes a barrier for thread synchronization.
- `pthread_barrier_wait()`: Makes threads wait until a barrier condition is met.
- `pthread_barrier_destroy()`: Destroys a barrier.

## Use Cases & Examples
### Example 1: Creating and Joining Threads
```c
#include <pthread.h>
#include <stdio.h>
#include <stdlib.h>

void *print_message(void *arg) {
    printf("Thread is running!\n");
    return NULL;
}

int main() {
    pthread_t thread;
    pthread_create(&thread, NULL, print_message, NULL);
    pthread_join(thread, NULL);
    return 0;
}
```

### Example 2: Using Mutexes to Prevent Race Conditions
```c
#include <pthread.h>
#include <stdio.h>

pthread_mutex_t lock;
int counter = 0;

void *increment_counter(void *arg) {
    pthread_mutex_lock(&lock);
    counter++;
    printf("Counter: %d\n", counter);
    pthread_mutex_unlock(&lock);
    return NULL;
}

int main() {
    pthread_t t1, t2;
    pthread_mutex_init(&lock, NULL);
    pthread_create(&t1, NULL, increment_counter, NULL);
    pthread_create(&t2, NULL, increment_counter, NULL);
    pthread_join(t1, NULL);
    pthread_join(t2, NULL);
    pthread_mutex_destroy(&lock);
    return 0;
}
```

## Summary & Key Takeaways
- **Thread management** helps in creating, terminating, and joining threads.
- **Mutexes** ensure that shared resources are accessed by only one thread at a time.
- **Condition variables** allow threads to wait and proceed based on specific conditions.
- **Synchronization** mechanisms, such as read/write locks and barriers, coordinate thread execution.

Using the Pthreads API effectively can significantly enhance a program’s performance and responsiveness in multi-threaded environments.


