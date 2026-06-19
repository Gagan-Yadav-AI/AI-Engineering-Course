# Day 24 | Machine Learning Associate

```python
import pandas as pd
```

---

# 📂 Reading a CSV File

```python
df = pd.read_csv("data.csv")
```

Example:

```python
import pandas as pd

df = pd.read_csv("students.csv")
print(df)
```

---

# 🔹 `head()`

Displays the first 5 rows by default.

```python
df.head()
```

Display first 10 rows:

```python
df.head(10)
```

**Output**

| Name | Age | Marks |
| ---- | --- | ----- |
| Ram  | 20  | 85    |
| Ravi | 21  | 90    |
| ...  | ... | ...   |

---

# 🔹 `tail()`

Displays the last 5 rows by default.

```python
df.tail()
```

Display last 3 rows:

```python
df.tail(3)
```

---

# 🔹 `shape`

Returns the number of rows and columns.

```python
df.shape
```

Output:

```python
(100, 5)
```

Meaning:

* 100 rows
* 5 columns

---

# 🔹 `info()`

Displays dataset information.

```python
df.info()
```

Shows:

* Number of rows
* Number of columns
* Column names
* Data types
* Non-null values
* Memory usage

---

# 🔹 `describe()`

Provides statistical summary for numerical columns.

```python
df.describe()
```

Returns:

* Count
* Mean
* Standard deviation
* Minimum
* 25%
* 50% (Median)
* 75%
* Maximum

---

# 🔹 `isnull().sum()`

Checks missing values in each column.

```python
df.isnull().sum()
```

Example Output:

```
Name      0
Age       2
Marks     1
dtype: int64
```

---

# 🔹 `groupby()`

Groups data based on a column.

Example:

```python
df.groupby("Department")["Salary"].mean()
```

Group by multiple columns:

```python
df.groupby(["Department", "Gender"]).sum()
```

Useful for:

* Average
* Sum
* Count
* Max
* Min

---

# 🔹 `unique()`

Returns unique values from a column.

```python
df["City"].unique()
```

Example Output:

```
['Delhi', 'Mumbai', 'Bangalore']
```

Count unique values:

```python
df["City"].nunique()
```

---

# 🔹 `str.contains()`

Checks whether a string exists inside a column.

```python
df[df["Name"].str.contains("Ram")]
```

Case insensitive:

```python
df[df["Name"].str.contains("ram", case=False)]
```

---

# 🔹 `drop()`

Removes rows or columns.

## Drop a column

```python
df.drop("Age", axis=1)
```

## Drop multiple columns

```python
df.drop(["Age", "Marks"], axis=1)
```

## Drop a row

```python
df.drop(0)
```

Permanent deletion:

```python
df.drop("Age", axis=1, inplace=True)
```

---

# 🔹 `sort_values()`

Sorts data.

Ascending order:

```python
df.sort_values("Marks")
```

Descending order:

```python
df.sort_values("Marks", ascending=False)
```

Sort by multiple columns:

```python
df.sort_values(["Department", "Salary"])
```

---

# 🔹 `dtypes`

Displays data type of each column.

```python
df.dtypes
```

Example:

```
Name      object
Age       int64
Marks     float64
```

---

# 📊 Data Visualization with Matplotlib

Import:

```python
import matplotlib.pyplot as plt
```

## Line Plot

```python
plt.plot(df["Marks"])
plt.show()
```

## Bar Chart

```python
plt.bar(df["Name"], df["Marks"])
plt.show()
```

## Histogram

```python
plt.hist(df["Marks"])
plt.show()
```

---

# 📈 Data Visualization with Seaborn

Import:

```python
import seaborn as sns
```

## Scatter Plot

```python
sns.scatterplot(x="Age", y="Marks", data=df)
plt.show()
```

## Bar Plot

```python
sns.barplot(x="Department", y="Salary", data=df)
plt.show()
```

## Box Plot

```python
sns.boxplot(x="Gender", y="Salary", data=df)
plt.show()
```

## Heatmap

```python
sns.heatmap(df.corr(numeric_only=True), annot=True)
plt.show()
```

---

# 🎯 Quick Revision Table

| Function         | Purpose                                    |
| ---------------- | ------------------------------------------ |
| `pd.read_csv()`  | Read CSV file                              |
| `head()`         | Show first rows                            |
| `tail()`         | Show last rows                             |
| `shape`          | Number of rows and columns                 |
| `info()`         | Dataset information                        |
| `describe()`     | Statistical summary                        |
| `isnull().sum()` | Count missing values                       |
| `groupby()`      | Group data for analysis                    |
| `unique()`       | Show unique values                         |
| `str.contains()` | Search text in a column                    |
| `drop()`         | Remove rows or columns                     |
| `sort_values()`  | Sort data                                  |
| `dtypes`         | Display data types                         |
| `matplotlib`     | Create basic plots                         |
| `seaborn`        | Create advanced statistical visualizations |

---


The most commonly used Pandas functions in data science projects are:

* `read_csv()`
* `head()`
* `tail()`
* `shape`
* `info()`
* `describe()`
* `isnull().sum()`
* `groupby()`
* `unique()`
* `drop()`
* `sort_values()`
* `dtypes`
