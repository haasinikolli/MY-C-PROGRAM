# HASH TABLE IMPLEMENTATION AND PERFORMANCE ANALYSIS USING C

## Data Structures and Algorithms (DAA) Project

### 1. Project Overview

This project implements a Hash Table using the C programming language. A hash table is a data structure used to store and retrieve data efficiently using a hash function.

The main objective of this project is to understand how hash tables work and how collisions can be handled using different collision resolution techniques.

This project implements two collision resolution techniques:

1. **Separate Chaining**
2. **Open Addressing – Linear Probing**

It also demonstrates the basic operations of a hash table, including insertion, searching, deletion and displaying elements.

### 2. Problem Statement

Implement a hash table with collision resolution strategies such as Separate Chaining and Open Addressing. Analyze the average-case and worst-case time complexities of Search, Insert and Delete operations under different load factors. Evaluate the performance of the techniques and identify real-world applications where hash tables are useful.

### 3. Objectives

- To understand the working of hash tables.
- To implement a hash function using C.
- To handle collisions using Separate Chaining.
- To implement Open Addressing using Linear Probing.
- To perform insertion, searching and deletion operations.
- To display the contents of the hash table.
- To understand the effect of collisions on performance.
- To study the time complexity of hash table operations.

### 4. Technologies Used

| Component | Technology |
|---|---|
| Programming Language | C |
| Compiler | GCC |
| Data Structure | Hash Table |
| Collision Resolution | Chaining and Linear Probing |
| IDE | Any C-compatible code editor |
| Platform | Windows / Linux / macOS |

### 5. Hash Function

The project uses the modulo division method to calculate the hash index.

**Formula:**

`h(key) = key % table_size`

The table size used in the implementation is 11.

**Example:**

- Key = 22
- Table size = 11
- Hash index = 22 % 11 = 0

Similarly:

- Key = 33
- Table size = 11
- Hash index = 33 % 11 = 0

Both keys are mapped to the same index. This situation is called a collision.

### 6. Collision Resolution Techniques

#### A. Separate Chaining

Separate Chaining handles collisions by maintaining a linked list at each index of the hash table.

When multiple keys produce the same hash index, they are stored in the linked list associated with that index.

**Example:**

If keys 22 and 33 produce index 0, they are stored as:

`Index 0 → 33 → 22 → NULL`

**Advantages:**
- Multiple keys can be stored at the same index.
- Deletion is straightforward.
- The table can store more elements than its number of indexes.

#### B. Open Addressing – Linear Probing

Linear Probing resolves collisions by searching for the next available position in the hash table.

**Formula:**

`h(key, i) = (h(key) + i) % table_size`

Here:
- key = element to be inserted
- i = number of attempts
- table_size = total number of positions

If the calculated position is occupied, the program checks the next position until an empty slot is found.

The implementation uses a special deleted marker called a **Tombstone** to support deletion without interrupting future searches.

### 7. Operations Implemented

| Operation | Description |
|---|---|
| Insert | Adds a new key to the hash table |
| Search | Checks whether a particular key exists |
| Delete | Removes a key from the hash table |
| Display | Displays all hash table elements |

The program provides a menu-driven interface through which users can select either Separate Chaining or Linear Probing.

### 8. Time Complexity Analysis

The following table shows the theoretical time complexity under a well-distributed hash function and suitable load conditions.

| Operation | Separate Chaining – Average | Linear Probing – Average | Worst Case |
|---|---|---|---|
| Insert | O(1) expected | O(1) expected at low load | O(n) |
| Search | O(1 + α) expected | O(1) expected at low load | O(n) |
| Delete | O(1 + α) expected | O(1) expected at low load | O(n) |

Here, `α` represents the load factor.

**Load Factor Formula:**

`α = Number of stored elements / Table size`

A higher load factor generally increases the possibility of collisions and can reduce performance.

### 9. Real-World Applications

Hash tables are widely used in computer science and software development.

1. **Database Management:** Helps retrieve records efficiently using indexed keys.
2. **Caching Systems:** Stores frequently accessed information for faster retrieval.
3. **Compiler Design:** Uses symbol tables to store variable names and their associated information.
4. **Password Verification:** Hashing techniques are used in secure password storage systems.
5. **Dictionaries and Sets:** Supports fast lookup and membership checking.
6. **Search Engines:** Hash-based structures can support efficient indexing and lookup operations.

### 10. Advantages

- Provides fast data retrieval in average cases.
- Supports efficient insertion and deletion.
- Handles collisions using two different techniques.
- Demonstrates practical applications of linked lists and arrays.
- Provides a simple menu-driven interface.

### 11. Conclusion

This project demonstrates the implementation of hash tables using the C programming language.

Both Separate Chaining and Linear Probing are implemented to handle collisions. The program performs insertion, searching, deletion and display operations.

Through this project, we understand how hash functions work, why collisions occur, how collision resolution techniques solve the problem, and how load factor affects the efficiency of hash tables.

Hash tables are important data structures because they provide efficient data storage and retrieval in many real-world applications.

### 12. How to Run the Project

**Step 1:** Clone or download this repository.

**Step 2:** Open the project folder in a terminal.

**Step 3:** Compile the C program using GCC.

```bash
gcc main.c -o hash_table
```

**Step 4:** Run the program.

For Windows:

```bash
hash_table.exe
```

For Linux/macOS:

```bash
./hash_table
```

### 13. Project File Structure

```text
MY-C-PROGRAM/
│
├── main.c
└── README.md
```

### 14. GitHub Repository

**Source Code:** https://github.com/haasinikolli/MY-C-PROGRAM

**Programming Language:** C

**Subject:** Data Structures and Algorithms (DAA)

**Project Topic:** Hash Table Implementation and Performance Analysis

---

**Developed as part of the Data Structures and Algorithms (DAA) academic project.**
