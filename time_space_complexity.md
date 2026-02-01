# Time & Space Complexity

*(Big-O, Big-Ω, Big-Θ)*


## 1️⃣ Why Time & Space Complexity Matters (Real Life)

**Real-time example**
Imagine **Zomato searching restaurants**:

* 10 restaurants → fast
* 1,000,000 restaurants → slow if logic is bad

**DSA is about writing code that scales**

---

## 2️⃣ Time Complexity (How fast code runs)

Time complexity measures **how runtime grows when input size (n) increases**.

We **ignore machine speed** and count **operations**.

---

### 🔹 Big-O (Worst Case) – Most Important

> “What is the **maximum time** my algorithm can take?”

#### Example:

```python
def find_element(arr, target):
    for x in arr:
        if x == target:
            return True
    return False
```

* Worst case: element **not present**
* Checks all `n` elements

**Time Complexity: O(n)**

> “Big-O represents the worst-case time complexity.”

---

### 🔹 Big-Ω (Best Case)

> “What is the **minimum time** my algorithm can take?”

Same code:

```python
arr = [10, 20, 30, 40]
target = 10
```

* Found at **first index**
* Only 1 operation

**Time Complexity: Ω(1)**

> “Big-Omega represents the best-case time complexity.”

---

### 🔹 Big-Θ (Average / Tight Bound)

> “When best & worst cases are **same order**”

Example:

```python
def print_all(arr):
    for x in arr:
        print(x)
```

* Always runs `n` times

**Θ(n)**

> “Big-Theta represents the tight bound where best and worst cases are the same.”

---

## 3️⃣ Space Complexity (Memory used)

Includes:

* Variables
* Data structures
* Recursion stack

---

### Example 1: Constant Space

```python
def sum_two(a, b):
    return a + b
```

**Space: O(1)**

---

### Example 2: Extra Space

```python
def copy_array(arr):
    new_arr = []
    for x in arr:
        new_arr.append(x)
    return new_arr
```

**Space: O(n)**

---

### Example 3: Recursion Space

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
```

* Recursion stack = `n` calls

**Space: O(n)**

---

## 4️⃣ Common Time Complexities (Must Memorize)

| Complexity | Meaning        | Example                |
| ---------- | -------------- | ---------------------- |
| O(1)       | Constant       | Access array index     |
| O(log n)   | Very fast      | Binary search          |
| O(n)       | Linear         | Loop                   |
| O(n log n) | Efficient sort | Merge sort             |
| O(n²)      | Slow           | Nested loops           |
| O(2ⁿ)      | Very slow      | Recursion without memo |
| O(n!)      | Worst          | Permutations           |

**Golden Rule**:

> Avoid **O(n²)** when **n is large**

---

## Interview Memory Trick

### Single Loop?

➡️ **O(n)**

### Loop inside loop?

➡️ **O(n²)**

### Divide by half?

➡️ **O(log n)**

### Recursion?

➡️ **Check depth (stack space)**

---

## Typical Interview Question

*What is the time complexity of this code?*

```python
for i in range(n):
    for j in range(n):
        print(i, j)
```

**Answer**:

* Two nested loops
* Runs `n × n` times

**O(n²)**

---

## 7️⃣ One-Line Interview Answer Template

You can say this confidently 

> “The time complexity is O(n) because the loop runs n times, and the space complexity is O(1) since no extra data structure is used.”

---


