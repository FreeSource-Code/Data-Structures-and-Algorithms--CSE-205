
# 📘 Arrays: Memory, Operations, and Sorting Algorithms (With Examples)

## 🧾 1. What is an Array?

An **array** is a data structure that stores a **fixed-size sequence** of elements of the **same type** in **contiguous memory**.

### ✅ Properties:
- Same data type
- Fixed size
- Contiguous memory
- Accessed using index

### 🔹 Example (C++):
```cpp
int arr[5] = {10, 20, 30, 40, 50};
cout << arr[0]; // 10
```

⏱ Access Time: O(1)

---

## 🧾 2. Linear Arrays

A **linear array** is a one-dimensional array with elements stored linearly and accessed using a single index.

```cpp
int arr[3] = {5, 10, 15};
```

---

## 🧠 3. Memory Representation

```
Address(arr[i]) = Base Address + (i × Size of each element)
```

### Example:
- Base = 1000, int size = 4 bytes
- arr[2] → 1000 + 2×4 = 1008

---

## 🔁 4. Array Operations

### ✅ A. Traversal

```cpp
for(int i = 0; i < n; i++) {
    cout << arr[i];
}
```
⏱ Time: O(n)

---

### ✅ B. Insertion

Insert 25 at index 2 in [10, 20, 30, 40]:

```
Before: [10, 20, 30, 40]
After : [10, 20, 25, 30, 40]
```

⏱ Time: O(n)

---

### ✅ C. Deletion

Delete index 1 in [10, 20, 30, 40]:

```
Before: [10, 20, 30, 40]
After : [10, 30, 40]
```

⏱ Time: O(n)

---

### ✅ D. Searching

#### Linear Search
```cpp
for(int i = 0; i < n; i++) {
    if(arr[i] == key) return i;
}
```
⏱ Time: O(n)

#### Binary Search (Sorted array)
```cpp
int low = 0, high = n-1;
while(low <= high) {
    int mid = (low + high)/2;
    if(arr[mid] == key) return mid;
    else if(arr[mid] < key) low = mid + 1;
    else high = mid - 1;
}
```
⏱ Time: O(log n)

---

### ✅ E. Merging Arrays

```cpp
for(int i = 0; i < n; i++) C[i] = A[i];
for(int j = 0; j < m; j++) C[n + j] = B[j];
```
⏱ Time: O(n + m)

---

## 📊 5. Time Complexity of Array Operations

| Operation   | Time Complexity |
|-------------|------------------|
| Traversal   | O(n)             |
| Insertion   | O(n)             |
| Deletion    | O(n)             |
| Searching   | O(n) / O(log n)  |
| Merging     | O(n + m)         |

---

## 🧾 6. Sorting Algorithms

### 🔷 A. Bubble Sort

```cpp
for(int i = 0; i < n-1; i++) {
    for(int j = 0; j < n-i-1; j++) {
        if(arr[j] > arr[j+1]) swap(arr[j], arr[j+1]);
    }
}
```
⏱ Best: O(n), Worst: O(n²), Space: O(1), Stable: ✅

---

### 🔷 B. Insertion Sort

```cpp
for(int i = 1; i < n; i++) {
    int key = arr[i];
    int j = i - 1;
    while(j >= 0 && arr[j] > key) {
        arr[j + 1] = arr[j];
        j--;
    }
    arr[j + 1] = key;
}
```
⏱ Best: O(n), Worst: O(n²), Space: O(1), Stable: ✅

---

### 🔷 C. Selection Sort

```cpp
for(int i = 0; i < n-1; i++) {
    int min_idx = i;
    for(int j = i+1; j < n; j++) {
        if(arr[j] < arr[min_idx]) min_idx = j;
    }
    swap(arr[i], arr[min_idx]);
}
```
⏱ Best/Worst: O(n²), Space: O(1), Stable: ❌

---

## 📊 7. Sorting Algorithms Comparison

| Algorithm      | Best Case | Worst Case | Stable | Space |
|----------------|-----------|------------|--------|--------|
| Bubble Sort    | O(n)      | O(n²)      | ✅     | O(1)   |
| Insertion Sort | O(n)      | O(n²)      | ✅     | O(1)   |
| Selection Sort | O(n²)     | O(n²)      | ❌     | O(1)   |
