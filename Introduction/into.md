
# 📘 Basic Data Structures, Concepts, and Complexity Analysis

## 🧾 1. What is Basic Data Structures?

A **Data Structure** is a way to store, organize, and manage data so that it can be used efficiently.

### 🔹 Common Basic Data Structures:

| Structure    | Description                               | Example Usage        |
|--------------|-------------------------------------------|-----------------------|
| Array        | Fixed-size collection of similar data     | Store student marks  |
| Linked List  | Elements connected using pointers         | Music playlist       |
| Stack        | LIFO – Last In First Out                  | Undo operation       |
| Queue        | FIFO – First In First Out                 | Print queue          |
| Tree         | Hierarchical structure                    | File system          |
| Graph        | Network of nodes and edges                | Social networks      |

### 🧠 Example (C++):
```cpp
int arr[5] = {10, 20, 30, 40, 50};
arr[0] = 10;
arr[4] = 50; // Access Time: O(1)
```

---

## 🧾 2. What is Basic Concepts and Notations?

### 🔸 Key Concepts:

- **Data**: Raw values (e.g., `10`, `"apple"`, `false`)
- **Data Types**:  
  - `int` → 10  
  - `float` → 10.5  
  - `char` → 'A'  
  - `bool` → true / false  
- **Abstract Data Types (ADT)**: Logical models like Stack, Queue
- **Algorithm**: A set of steps to solve a problem

### 🔸 Common Operations:

| Operation   | Description                  |
|-------------|------------------------------|
| Insertion   | Add data                     |
| Deletion    | Remove data                  |
| Traversal   | Visit each element           |
| Searching   | Find a specific item         |
| Sorting     | Arrange in a specific order  |

---

## 🧾 3. Complexity Analysis

### ✅ A. Time Complexity

Measures the number of operations depending on input size `n`.

| Type      | Example Code                       | Time Complexity |
|-----------|------------------------------------|-----------------|
| Linear    | `for(i = 0; i < n; i++)`           | O(n)            |
| Constant  | `arr[0]`                           | O(1)            |

### ✅ B. Space Complexity

Measures how much memory is used.

```cpp
int arr[n]; // Space = O(n)
```

### ✅ C. Time-Space Trade-Off

Using more memory (space) to reduce time.

**Example:**  
Memoization – stores past results to avoid recomputation.

---

## 📐 Asymptotic Notations

| Notation   | Symbol | Description           | Case        |
|------------|--------|------------------------|-------------|
| Big O      | O(n)   | Upper Bound (Max Time) | Worst Case  |
| Omega      | Ω(n)   | Lower Bound (Min Time) | Best Case   |
| Theta      | Θ(n)   | Tight Bound            | Avg Case    |

---

## ✅ Practical Example: Linear Search

```cpp
int linearSearch(int arr[], int n, int key) {
   for (int i = 0; i < n; i++) {
       if (arr[i] == key) return i;
   }
   return -1;
}
```

| Case        | Time Complexity |
|-------------|------------------|
| Best Case   | Ω(1)             |
| Worst Case  | O(n)             |
| Average     | Θ(n)             |
