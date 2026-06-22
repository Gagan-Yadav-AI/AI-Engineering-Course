# Day 22 | Machine Learning Associate

# NumPy Notes – Arrays and Basic Operations

## 1. `np.zeros()`

Creates an array filled with zeros.

```python
import numpy as np

a = np.zeros((2, 3))
print(a)
```

**Output:**

```
[[0. 0. 0.]
 [0. 0. 0.]]
```

---

## 2. `np.ones()`

Creates an array filled with ones.

```python
a = np.ones((3, 2))
print(a)
```

**Output:**

```
[[1. 1.]
 [1. 1.]
 [1. 1.]]
```

---

## 3. Identity Matrix (`np.eye()`)

Creates a square matrix with 1s on the diagonal and 0s elsewhere.

```python
a = np.eye(4)
print(a)
```

**Output:**

```
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
```

---

## 4. `np.random.rand()`

Generates random numbers between **0 and 1**.

```python
a = np.random.rand(2, 3)
print(a)
```

Example:

```
[[0.45 0.78 0.12]
 [0.34 0.56 0.90]]
```

---

## 5. `np.random.randn()`

Generates random numbers from a **standard normal distribution**
(mean = 0, standard deviation = 1).

```python
a = np.random.randn(3, 2)
print(a)
```

Example:

```
[[ 0.23 -1.45]
 [ 0.87  0.11]
 [-0.56  1.29]]
```

---

## 6. `np.random.randint()`

Generates random integers within a specified range.

```python
a = np.random.randint(1, 10, size=(2, 3))
print(a)
```

Example:

```
[[3 7 1]
 [9 2 5]]
```

---

# Statistical Functions

## 7. Maximum (`max`)

```python
a = np.array([5, 8, 2, 10])

print(np.max(a))
```

Output:

```
10
```

---

## 8. Minimum (`min`)

```python
print(np.min(a))
```

Output:

```
2
```

---

## 9. Mean (`mean`)

```python
print(np.mean(a))
```

Output:

```
6.25
```

Formula:

```
Mean = Sum of values / Number of values
```

---

## 10. Standard Deviation (`std`)

```python
print(np.std(a))
```

Measures how spread out the data is from the mean.

* Low standard deviation → values are close to the mean.
* High standard deviation → values are widely spread.

---

# Algebra Operations

Suppose:

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
```

## Addition

```python
print(a + b)
```

Output:

```
[5 7 9]
```

---

## Subtraction

```python
print(a - b)
```

Output:

```
[-3 -3 -3]
```

---

## Multiplication (Element-wise)

```python
print(a * b)
```

Output:

```
[4 10 18]
```

---

## Division

```python
print(a / b)
```

Output:

```
[0.25 0.4 0.5]
```

---

## Power

```python
print(a ** 2)
```

Output:

```
[1 4 9]
```

---

# Dot Product (`np.dot()`)

Multiplies corresponding elements and adds the results.

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print(np.dot(a, b))
```

Calculation:

```
(1×4) + (2×5) + (3×6)
= 4 + 10 + 18
= 32
```

Output:

```
32
```

For matrices:

```python
A = np.array([[1, 2],
              [3, 4]])

B = np.array([[5, 6],
              [7, 8]])

print(np.dot(A, B))
```

---

# Broadcasting

Broadcasting allows NumPy to perform operations on arrays of different shapes when compatible.

```python
a = np.array([[1],
              [2],
              [3]])

b = np.array([10, 20, 30])

print(a + b)
```

Output:

```
[[11 21 31]
 [12 22 32]
 [13 23 33]]
```

The smaller array is automatically expanded to match the larger one.

---

# Accessing Data

## 1. Indexing

### 1D Array

```python
a = np.array([10, 20, 30, 40])

print(a[2])
```

Output:

```
30
```

---

### 2D Array

```python
a = np.array([[1, 2],
              [3, 4]])

print(a[1, 0])
```

Output:

```
3
```

---

# 2. Slicing

### 1D Slicing

```python
a = np.array([10, 20, 30, 40, 50])

print(a[1:4])
```

Output:

```
[20 30 40]
```

---

### 2D Slicing

```python
a = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])

print(a[0:2, 1:3])
```

Output:

```
[[2 3]
 [5 6]]
```

---

# 3. Logical Indexing (Boolean Masking)

Select elements based on conditions.

```python
a = np.array([5, 10, 15, 20, 25])

print(a[a > 10])
```

Output:

```
[15 20 25]
```

Another example:

```python
print(a[a % 2 == 0])
```

Output:

```
[10 20]
```

---

# Quick Revision Table

| Function              | Purpose                             | Example                        |
| --------------------- | ----------------------------------- | ------------------------------ |
| `np.zeros()`          | Create array of zeros               | `np.zeros((2,3))`              |
| `np.ones()`           | Create array of ones                | `np.ones((2,3))`               |
| `np.eye()`            | Identity matrix                     | `np.eye(3)`                    |
| `np.random.rand()`    | Random values (0–1)                 | `np.random.rand(2,2)`          |
| `np.random.randn()`   | Random normal values                | `np.random.randn(2,2)`         |
| `np.random.randint()` | Random integers                     | `np.random.randint(1,10,5)`    |
| `np.max()`            | Largest value                       | `np.max(arr)`                  |
| `np.min()`            | Smallest value                      | `np.min(arr)`                  |
| `np.mean()`           | Average                             | `np.mean(arr)`                 |
| `np.std()`            | Standard deviation                  | `np.std(arr)`                  |
| `np.dot()`            | Dot product / matrix multiplication | `np.dot(a,b)`                  |
| Indexing              | Access a single element             | `arr[0]`                       |
| Slicing               | Access multiple elements            | `arr[1:4]`                     |
| Logical Indexing      | Filter with conditions              | `arr[arr > 10]`                |
| Broadcasting          | Automatic shape expansion           | `arr + 5` or `matrix + vector` |
