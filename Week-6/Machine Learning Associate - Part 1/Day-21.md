# Day 21 | Machine Learning Associate

# NumPy, Data Structures & Arrays

## 📌 Introduction to NumPy

**NumPy (Numerical Python)** is a powerful Python library used for numerical computing. It provides fast and efficient operations on arrays and mathematical data.

### Why Use NumPy?

* Faster than Python lists
* Supports multidimensional arrays
* Performs mathematical and statistical operations efficiently
* Widely used in Data Science, Machine Learning, and AI

---

# 📌 Data Structure

A **data structure** is a way of organizing and storing data so it can be accessed and modified efficiently.

### Common Data Structures in Python

* List
* Tuple
* Set
* Dictionary
* NumPy Array

Example:

```python
numbers = [10, 20, 30, 40]
```

---

# 📌 Array

An **array** is a collection of elements of the same data type stored in contiguous memory locations.

Example:

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

Output:

```
[1 2 3 4 5]
```

---

# 📌 Types of Arrays Based on Dimensions

## 1. Scalar (0-D Array)

A scalar contains only **one value**.

```python
scalar = np.array(10)

print(scalar)
print(scalar.ndim)
```

Output:

```
10
0
```

---

## 2. Vector (1-D Array)

A vector contains values arranged in a single dimension.

```python
vector = np.array([1, 2, 3, 4])

print(vector)
print(vector.ndim)
```

Output:

```
[1 2 3 4]
1
```

---

## 3. Matrix (2-D Array)

A matrix consists of rows and columns.

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(matrix)
print(matrix.ndim)
```

Output:

```
[[1 2 3]
 [4 5 6]]
2
```

---

## 4. Tensor (3-D or Higher)

A tensor is an array with three or more dimensions.

```python
tensor = np.array([
    [[1, 2], [3, 4]],
    [[5, 6], [7, 8]]
])

print(tensor.ndim)
```

Output:

```
3
```

---

# 📌 Importing NumPy

The standard way to import NumPy is:

```python
import numpy as np
```

Now all NumPy functions can be accessed using `np`.

Example:

```python
arr = np.array([10, 20, 30])

print(arr)
```

---

# 📌 NumPy Functions

## 1. shape

Returns the dimensions of an array.

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(arr.shape)
```

Output:

```
(2, 3)
```

Meaning:

* 2 rows
* 3 columns

---

## 2. size

Returns the total number of elements.

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(arr.size)
```

Output:

```
6
```

---

## 3. dtype

Returns the data type of array elements.

```python
arr = np.array([1, 2, 3])

print(arr.dtype)
```

Output:

```
int64
```

Example with float:

```python
arr = np.array([1.5, 2.5])

print(arr.dtype)
```

Output:

```
float64
```

---

## 4. arange()

Creates evenly spaced values within a given range.

Syntax:

```python
np.arange(start, stop, step)
```

Example:

```python
arr = np.arange(1, 10)

print(arr)
```

Output:

```
[1 2 3 4 5 6 7 8 9]
```

Example with step:

```python
arr = np.arange(0, 20, 2)

print(arr)
```

Output:

```
[ 0  2  4  6  8 10 12 14 16 18]
```

---

## 5. reshape()

Changes the shape of an array without changing its data.

Example:

```python
arr = np.arange(1, 13)

new_arr = arr.reshape(3, 4)

print(new_arr)
```

Output:

```
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]]
```

Note:
The total number of elements must remain the same.

```
12 elements → (3 × 4)
```

---

## 6. linspace()

Creates evenly spaced numbers between two values.

Syntax:

```python
np.linspace(start, stop, num)
```

Example:

```python
arr = np.linspace(0, 10, 5)

print(arr)
```

Output:

```
[ 0.   2.5  5.   7.5 10. ]
```

Example:

```python
np.linspace(1, 5, 9)
```

Output:

```
[1.  1.5 2.  2.5 3.  3.5 4.  4.5 5. ]
```

---

# 📌 Quick Summary Table

| Concept              | Description                  | Example                   |
| -------------------- | ---------------------------- | ------------------------- |
| `import numpy as np` | Imports NumPy                | `import numpy as np`      |
| `np.array()`         | Creates an array             | `np.array([1,2,3])`       |
| `shape`              | Returns dimensions           | `(2,3)`                   |
| `size`               | Returns total elements       | `6`                       |
| `dtype`              | Returns data type            | `int64`                   |
| `arange()`           | Creates values with a step   | `np.arange(0,10,2)`       |
| `reshape()`          | Changes array shape          | `arr.reshape(3,4)`        |
| `linspace()`         | Creates evenly spaced values | `np.linspace(0,10,5)`     |
| Scalar               | 0-D single value             | `np.array(10)`            |
| Vector               | 1-D array                    | `np.array([1,2,3])`       |
| Matrix               | 2-D array                    | `np.array([[1,2],[3,4]])` |
| Tensor               | 3-D or higher array          | `np.array([[[1],[2]]])`   |

## 🚀 Key Takeaways

* **NumPy** is the foundation for numerical computing in Python.
* **Arrays** are more efficient than Python lists for mathematical operations.
* **Scalars, vectors, matrices, and tensors** represent data with increasing dimensions.
* Essential NumPy functions include:

  * `shape` → dimensions
  * `size` → total elements
  * `dtype` → data type
  * `arange()` → range of values
  * `reshape()` → change array dimensions
  * `linspace()` → evenly spaced values within an interval
