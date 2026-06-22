# Day 23 | Machine Learning Associate

## 1. What is Pandas?

**Pandas** is a Python library used for:

* Data analysis
* Data manipulation
* Data cleaning
* Reading and writing datasets

### Import Pandas

```python
import pandas as pd
```

---

# 2. Series

A **Series** is a one-dimensional labeled array.

### Syntax

```python
pd.Series(data, index=index_names)
```

### Example using List

```python
import pandas as pd

s = pd.Series([10, 20, 30, 40])

print(s)
```

Output:

```
0    10
1    20
2    30
3    40
dtype: int64
```

---

## Series from List

```python
s = pd.Series(["Apple", "Banana", "Orange"])

print(s)
```

---

## Series from NumPy Array

```python
import numpy as np

arr = np.array([5, 10, 15, 20])

s = pd.Series(arr)

print(s)
```

---

## Series from Dictionary

```python
data = {
    "Math": 90,
    "Science": 85,
    "English": 88
}

s = pd.Series(data)

print(s)
```

Output:

```
Math       90
Science    85
English    88
dtype: int64
```

---

# 3. Accessing Data from Series

## By Position

```python
print(s[0])
print(s[1])
```

---

## By Label

```python
data = {
    "A": 100,
    "B": 200
}

s = pd.Series(data)

print(s["A"])
```

---

# 4. Changing Index Names in Series

```python
s = pd.Series(
    [100, 200, 300],
    index=["Math", "Science", "English"]
)

print(s)
```

Output:

```
Math       100
Science    200
English    300
```

---

# 5. DataFrame

A **DataFrame** is a two-dimensional table with rows and columns.

### Syntax

```python
pd.DataFrame(data)
```

---

## DataFrame from List

```python
data = [
    [1, "Gagan", 22],
    [2, "Rahul", 23]
]

df = pd.DataFrame(data)

print(df)
```

---

## DataFrame from NumPy Array

```python
import numpy as np

arr = np.array([
    [10, 20],
    [30, 40]
])

df = pd.DataFrame(arr)

print(df)
```

---

## DataFrame from Dictionary

```python
data = {
    "Name": ["Gagan", "Rahul"],
    "Age": [22, 23],
    "City": ["Bangalore", "Delhi"]
}

df = pd.DataFrame(data)

print(df)
```

---

# 6. Accessing Data from DataFrame

## Single Column (Returns Series)

```python
print(df["Name"])
```

Output:

```
0    Gagan
1    Rahul
Name: Name, dtype: object
```

---

## Multiple Columns (Returns DataFrame)

```python
print(df[["Name", "Age"]])
```

Output:

```
    Name  Age
0  Gagan   22
1  Rahul   23
```

---

# 7. Changing Row Names (Index)

```python
df.index = ["Student1", "Student2"]

print(df)
```

Output:

```
          Name  Age       City
Student1 Gagan  22  Bangalore
Student2 Rahul  23      Delhi
```

---

# 8. Changing Column Names

```python
df.columns = ["Student Name", "Student Age", "Location"]

print(df)
```

Output:

```
         Student Name  Student Age  Location
Student1      Gagan            22  Bangalore
Student2      Rahul            23      Delhi
```

---

# 9. Changing Both Row and Column Names

```python
df.index = ["S1", "S2"]

df.columns = ["Name", "Age", "City"]

print(df)
```

Output:

```
      Name  Age       City
S1   Gagan   22  Bangalore
S2   Rahul   23      Delhi
```

---

# 10. Accessing a Single Row

Using `.loc`

```python
print(df.loc["S1"])
```

Or by integer position using `.iloc`

```python
print(df.iloc[0])
```

---

# 11. Accessing Multiple Rows

Using `.loc`

```python
print(df.loc[["S1", "S2"]])
```

Using `.iloc`

```python
print(df.iloc[0:2])
```

---

# 12. Accessing a Single Column

```python
print(df["Name"])
```

or

```python
print(df.loc[:, "Name"])
```

---

# 13. Accessing Multiple Columns

```python
print(df[["Name", "Age"]])
```

or

```python
print(df.loc[:, ["Name", "Age"]])
```

---

# 14. Reading a CSV File

## Syntax

```python
pd.read_csv("filename.csv")
```

### Example

```python
import pandas as pd

df = pd.read_csv("students.csv")

print(df)
```

---

## Read First 5 Rows

```python
df.head()
```

---

## Read Last 5 Rows

```python
df.tail()
```

---

## Display Column Names

```python
df.columns
```

---

## Display Row Index

```python
df.index
```

---

## Display Shape (Rows, Columns)

```python
df.shape
```

---

## Display Data Types

```python
df.dtypes
```

---

## Display Summary Information

```python
df.info()
```

---

## Display Statistical Summary

```python
df.describe()
```
