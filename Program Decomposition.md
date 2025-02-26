# Program Decomposition

## General Ideas:
Program decomposition refers to breaking down a program into smaller parts to improve parallelism and efficiency. The key aspects of program decomposition include:
focusing on breaking down a program into smaller, manageable tasks that can be executed concurrently. This allows for efficient utilization of multi-core processors and distributed systems.It Increases the Throughput and reduces CPU idle Time.This serves as a basis of Parallelism.

1. **Identify parallelizable code:** Recognizing which portions of the code can be executed in parallel without dependency issues.
2. **Mapping tasks to multiple processes:** Assigning different parts of the code to run concurrently across multiple processors.
3. **Distributing input, output, and intermediate data:** Ensuring that data is shared efficiently among processes to avoid bottlenecks.
4. **Managing access to shared resources:** Implementing mechanisms like locks or synchronization to prevent race conditions when multiple processes access shared data.
5. **Synchronizing processes:** Ensuring that different parts of the program execute in the correct sequence and do not interfere with one another.

---

# Code Decomposition

## Key Concepts:
Code decomposition involves dividing a computational task into smaller sub-tasks, some of which can be executed in parallel to improve performance. The major concepts in code decomposition are:

- **Decomposition:** The process of breaking down a program into smaller components to be executed separately.
- **Task:** The fundamental unit of decomposition, representing a segment of code that can be executed independently or in parallel.

### Granularity
- **Granularity:** Refers to the size and number of tasks created during decomposition.
- **Fine-grained decomposition:** A large number of small tasks, which can maximize parallelism but may introduce high communication overhead.
- **Coarse-grained decomposition:** A smaller number of large tasks, reducing overhead but limiting concurrency.

### Concurrency
- **Degree of concurrency:** Represents the maximum number of tasks that can be executed simultaneously in the system.

### Importance in Computing
Efficient program and code decomposition are crucial for optimizing parallel computing, reducing execution time, and improving resource utilization. They are widely applied in fields like high-performance computing, distributed systems, and cloud computing.

---
# Recursive Decomposition

## Introduction
Recursive decomposition is a method for inducing concurrency in problems that can be solved using the **divide-and-conquer strategy**. This technique involves breaking a problem into a set of independent subproblems. Each subproblem is then solved recursively by further dividing it into smaller subproblems, followed by combining their results.

The divide-and-conquer approach naturally facilitates concurrency, as different subproblems can be solved concurrently, leading to efficient problem-solving and improved performance.

## Example: Quicksort
Quicksort is a classic example of the divide-and-conquer approach. It sorts an array by recursively partitioning it based on a pivot element.

### Steps of the Quicksort Algorithm:
1. **Choose a Pivot**: Select a pivot element, `x`, from the array.
2. **Partitioning**: Divide the array into two subsequences:
   - `A₀`: Elements smaller than `x`
   - `A₁`: Elements greater than or equal to `x`
3. **Recursive Sorting**: Recursively apply the Quicksort algorithm on `A₀` and `A₁`.
4. **Combine Results**: The recursion terminates when each subsequence contains only a single element, leading to a fully sorted array.

### Key Characteristics of Quicksort:
- **Divide Step**: Selecting a pivot and partitioning the array.
- **Conquer Step**: Recursively sorting the two partitions.
- **Combine Step**: No explicit combining is needed as partitioning naturally organizes elements in sorted order.

## Example: MergeSort
MergeSort is another divide-and-conquer sorting algorithm that follows a more structured approach by dividing the array into equal halves and merging them after sorting.

### Steps of the MergeSort Algorithm:
1. **Divide**: Split the array into two equal halves.
2. **Conquer**:
   - Recursively sort both halves.
   - The computations can be represented as a binary tree structure.
   - Each process receives an array segment from its parent (except the root/master process).
3. **Merge**:
   - After sorting the halves, they are merged together in a sorted manner.
   - Child processes send their sorted halves back to the parent.
   - The parent merges the sorted halves and sends the result upwards in the tree until the entire array is sorted.

### Key Characteristics of MergeSort:
- **Guaranteed O(n log n) Complexity**: Unlike Quicksort, which has a worst-case O(n²) complexity, MergeSort maintains a consistent O(n log n) performance.
- **Stable Sort**: Maintains the relative order of equal elements.
- **Better for Large Datasets**: Particularly useful when sorting linked lists and large datasets due to its predictable runtime and stability.

## Comparison of Quicksort and MergeSort
| Feature        | Quicksort                  | MergeSort                 |
|--------------|--------------------------|--------------------------|
| Strategy     | Partitioning around a pivot | Dividing into equal halves and merging |
| Complexity (Average) | O(n log n) | O(n log n) |
| Complexity (Worst) | O(n²) | O(n log n) |
| Stability | Not stable | Stable |
| In-Place Sorting | Yes (No extra space) | No (Uses extra space) |
| Best Use Case | Small to medium datasets | Large datasets, linked lists |

## Conclusion
Recursive decomposition is a powerful technique used in various algorithms, particularly in sorting. Both Quicksort and MergeSort leverage the divide-and-conquer strategy to achieve efficient sorting, with each having distinct advantages. Understanding these methods helps in choosing the right algorithm based on specific use cases, such as memory constraints, dataset size, and stability requirements.
![image](https://github.com/user-attachments/assets/64df38c7-c7e5-4e1d-922d-425a2eb8591d)

# Data Decomposition

Data decomposition is a powerful and widely used technique for achieving concurrency in algorithms that operate on large data structures. The goal of decomposition is to break down computations into smaller, independent tasks that can be executed concurrently, thus improving efficiency and performance.

## Steps in Data Decomposition

The decomposition of computations is generally performed in two steps:

1. **Partitioning the Data**: 
   - The first step involves dividing the data on which computations are performed into smaller, non-overlapping partitions. This ensures that different computational tasks operate on distinct portions of the data.

2. **Partitioning the Computation into Tasks**: 
   - Once the data is partitioned, the next step is to divide the computations into tasks based on this partitioning. Each task processes a specific partition of the data, and the operations performed by these tasks are usually similar. 
   - For instance, in matrix computations such as matrix multiplication, each submatrix undergoes similar types of arithmetic operations. Some specialized operations, like **LU factorization**, are also performed on chosen subsets of data.

The effectiveness of data decomposition depends on choosing a partitioning strategy that maximizes concurrency while minimizing inter-task dependencies.

---

## Partitioning Output Data

In certain computational problems, the output itself can be naturally decomposed. 
- In such cases, each element of the output can be computed independently of others, based solely on a function of the input.
- This enables an automatic decomposition of the problem into tasks where each task is assigned the work of computing a portion of the output.
- This type of partitioning is particularly beneficial in **parallel computing**, where different processing units can compute different output elements simultaneously.

---

## Example: Matrix Multiplication using Block Matrix Decomposition

A common example of data decomposition is matrix multiplication, which can be efficiently implemented using block matrices.

![image](https://github.com/user-attachments/assets/0d85c743-ff86-4830-89fc-5f7d1670e3e6)
![image](https://github.com/user-attachments/assets/263f858c-ef61-4109-a874-121b3fc03bcc)






This approach is called **block matrix operations**, where matrix computations are performed at a block level instead of element-wise operations. This formulation significantly enhances performance, especially when implemented on parallel processing architectures such as GPUs or distributed computing frameworks.

---

## Advantages of Data Decomposition

- **Increased Parallelism**: By breaking computations into independent tasks, multiple processors can execute them concurrently, reducing overall execution time.
- **Scalability**: Efficient data partitioning allows for better utilization of computational resources, making the approach scalable for large datasets.
- **Improved Cache Efficiency**: Smaller data partitions fit better into memory caches, reducing latency in memory access and improving overall efficiency.
- **Better Load Balancing**: Assigning tasks based on data partitions helps in distributing the computational load evenly across processing units.

---

## Conclusion

Data decomposition is a fundamental strategy in parallel computing, enabling efficient execution of large-scale computations by partitioning data and computations. The technique is widely used in numerical computations, matrix operations, and distributed computing frameworks to achieve concurrency and scalability. The block matrix decomposition method exemplifies how data decomposition can be effectively applied to matrix-matrix multiplication, paving the way for optimized performance in high-performance computing systems.


# Exploratory Decomposition and the 15-Puzzle Problem

Exploratory decomposition is used to decompose problems whose underlying computations correspond to a search of a space for solutions.  
In **exploratory decomposition**, we partition the search space into smaller parts and search each one of these parts concurrently, until the desired solutions are found.  

For an example of exploratory decomposition, consider the **15-puzzle problem**.

## Example: The 15-Puzzle Problem

The **15-puzzle** consists of 15 tiles numbered 1 through 15 and one blank tile placed in a **4 × 4 grid**.  
A tile can be moved into the blank position from a position adjacent to it, thus creating a blank in the tile's original position.  

Depending on the configuration of the grid, **up to four moves are possible**:
- **Up**
- **Down**
- **Left**
- **Right**

The **initial and final configurations** of the tiles are specified.  
The objective is to determine any sequence or a shortest **sequence of moves that transforms the initial configuration to the final configuration**.  

The figure below illustrates:
- A sample **initial configuration**.
- The **final configuration**.
- A **sequence of moves** leading from the initial to the final configuration.

---

## Figure: 15-Puzzle Problem Instance

The figure shows:
1. **(a) Initial configuration**
2. **(b), (c) Intermediate moves**
3. **(d) Final configuration**

### Configurations:

#### (a) Initial Configuration:
```
1  2  3  4
5  6  ⬜  8
9  10  7  11
13 14 15 12
```

#### (b) First Move:
```
1  2  3  4
5  6  7  8
9  10 ⬜ 11
13 14 15 12
```

#### (c) Second Move:
```
1  2  3  4
5  6  7  8
9  10 11 ⬜
13 14 15 12
```

#### (d) Final Configuration:
```
1  2  3  4
5  6  7  8
9  10 11 12
13 14 15 ⬜
```
---

This transformation shows the sequence of moves required to solve the **15-puzzle problem** efficiently.
![image](https://github.com/user-attachments/assets/415331ed-31f9-4357-be09-05fc439e9b2d)
# Speculative Decomposition

## Overview
Speculative decomposition is a technique used in parallel computing where a program may take one of many possible computationally significant branches based on the output of previous computations. This allows for tasks to be executed speculatively before the required inputs are fully available.

## Concept
In speculative decomposition:
- While one task is performing the computation whose output determines the next computation, other tasks can concurrently start computations for potential next stages.
- This is similar to evaluating multiple branches of a switch statement in parallel before the necessary input for the switch is available.
- As one task works to resolve the switch, other tasks pick up multiple branches of the switch in parallel.
- Once the correct input is determined, the computation corresponding to the correct branch is used, while all other computations are discarded.
- This leads to a reduction in parallel runtime compared to serial execution by overlapping computations.

## Benefits and Challenges
### Benefits
- **Reduced Execution Time:** The parallel run time is often smaller than the serial run time since computations are performed speculatively in advance.
- **Efficient Utilization of Resources:** Allows tasks to be scheduled in parallel, reducing idle processor time.
- **Increased Throughput:** When multiple speculative stages exist, they can collectively improve the speedup.

### Challenges
- **Wasted Computation:** Some computations may be discarded if the anticipated outcome of a switch is incorrect.
- **Optimization Complexity:** A formulation must balance between performing useful speculative computation and avoiding excessive waste.
- **Rollback Mechanism:** If the anticipated branch is incorrect, rollback mechanisms must be implemented to revert to the correct path efficiently.

## Optimized Speculative Decomposition
A more optimized form of speculative decomposition reduces wasted computation by:
- Prioritizing only the most promising branches for speculative execution.
- Rolling back computations only if the speculative assumption turns out to be incorrect.
- Selecting branches that are more likely to be taken based on probabilistic analysis.

## Application
A common application of speculative decomposition is **discrete event simulation**, where multiple future states of a system are explored in parallel. This enables faster simulation and analysis, making it particularly useful in fields such as network modeling, computational finance, and systems engineering.

## Conclusion
Speculative decomposition is a powerful parallel computing technique that enhances performance by leveraging speculative execution. By balancing useful computation with waste minimization strategies, it can significantly improve efficiency in scenarios where computational outcomes depend on preceding tasks.

## Example 
 Decision Trees , Topological Sort and *Switch cases*

 # Functional Decomposition (as its mention in in ppt)

## Definition
Functional decomposition is the process of breaking down a complex function, system, or problem into smaller, more manageable parts or tasks. This technique allows for better organization, easier debugging, and enhanced modularity in software development and system design.

## Key Concepts
1. **Breaking down functionality**: Large functions or processes are split into smaller, independent functions that can be developed, tested, and maintained separately.
2. **Task partitioning**: Each sub-function is responsible for a specific task, reducing dependencies and improving code reusability.
3. **Improved readability and maintenance**: Smaller functions make the system easier to understand, modify, and extend.

## Example: Database Functions
Functional decomposition can be applied in database management systems by dividing database-related operations into distinct functional units:

1. **Data Insertion**: A function responsible for adding records to the database.
2. **Data Retrieval**: A function dedicated to fetching data based on queries.
3. **Data Updating**: A function that modifies existing records in the database.
4. **Data Deletion**: A function that handles removing records from the database.

By structuring a database system in this way, each function operates independently, making debugging, testing, and scaling more efficient.

## Benefits of Functional Decomposition
- **Modularity**: Code can be reused across different projects.
- **Scalability**: Easy to add new functionalities without affecting existing ones.
- **Debugging Efficiency**: Issues can be isolated to specific functions.
- **Collaborative Development**: Multiple developers can work on different components simultaneously.

## Conclusion
Functional decomposition is an essential software engineering practice that enhances code quality, maintainability, and efficiency. It is widely used in various domains, including database management, software development, and system architecture.


