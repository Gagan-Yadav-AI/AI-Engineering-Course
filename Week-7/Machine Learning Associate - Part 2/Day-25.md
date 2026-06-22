# Day-25 | Machine Learning Associate

## What is Matplotlib?

Matplotlib is a Python visualization library used for creating graphs and charts. It is widely used in Data Science, Machine Learning, and Data Analysis.

```python
import matplotlib.pyplot as plt
```

---

# 1️⃣ Line Plot

Used to show trends over time.

```python
x = [1,2,3,4,5]
y = [10,20,15,25,30]

plt.plot(x,y)
plt.show()
```

---

# 2️⃣ Bar Chart

Used to compare categories.

```python
subjects = ["Python","SQL","Excel"]
marks = [90,80,85]

plt.bar(subjects,marks)
plt.show()
```

---

# 3️⃣ Scatter Plot

Used to identify relationships between variables.

```python
x = [1,2,3,4,5]
y = [10,20,15,25,30]

plt.scatter(x,y)
plt.show()
```

---

# 4️⃣ Pie Chart

Used to show percentage distribution.

```python
labels = ["Python","SQL","Excel"]
sizes = [50,30,20]

plt.pie(sizes,labels=labels,autopct='%1.1f%%')
plt.show()
```

---

# 5️⃣ Histogram

Used to view frequency distribution.

```python
marks = [10,20,30,40,50,60,70,80,90]

plt.hist(marks)
plt.show()
```

### Output Example

```
Frequency
|
|      █
|      █ █
|    █ █ █
|  █ █ █ █
+------------
 10 20 30 ...
```

---

# 6️⃣ Box Plot

Used to identify outliers and data spread.

```python
data = [10,20,30,40,50,100]

plt.boxplot(data)
plt.show()
```

### Output Example

```
      ●  <- Outlier
      |
|-----|-----|
```

---

# 7️⃣ Horizontal Bar Chart

```python
plt.barh(subjects, marks)
plt.show()
```

---

# 8️⃣ Stack Plot

```python
days = [1,2,3,4,5]
study = [2,3,4,3,5]
sleep = [8,7,6,8,7]

plt.stackplot(days, study, sleep)
plt.show()
```

---

# 9️⃣ Area Plot

```python
plt.fill_between(x,y)
plt.show()
```

---

# 🔟 Stem Plot

```python
plt.stem([1,2,3,4],[10,20,15,25])
plt.show()
```

---

# 1️⃣1️⃣ Error Bar Plot

```python
x=[1,2,3]
y=[10,20,30]
err=[1,2,1]

plt.errorbar(x,y,yerr=err)
plt.show()
```

---

# 1️⃣2️⃣ Violin Plot

```python
data = [10,20,30,40,50]

plt.violinplot(data)
plt.show()
```

---

# 1️⃣3️⃣ Hexbin Plot

```python
plt.hexbin(x,y)
plt.show()
```

---

# 1️⃣4️⃣ Step Plot

```python
plt.step(x,y)
plt.show()
```

---

# 1️⃣5️⃣ Event Plot

```python
plt.eventplot([1,2,3,4,5])
plt.show()
```

---

# 1️⃣6️⃣ Polar Plot

```python
import numpy as np

theta = np.linspace(0, 2*np.pi, 100)

plt.polar(theta, theta)
plt.show()
```

---

# 1️⃣7️⃣ Contour Plot

```python
plt.contour(Z)
plt.show()
```

---

# 1️⃣8️⃣ Filled Contour Plot

```python
plt.contourf(Z)
plt.show()
```

---

# 1️⃣9️⃣ Multiple Line Plot

```python
x=[1,2,3,4]

sales=[10,20,30,40]
profit=[5,10,15,20]

plt.plot(x,sales,label='Sales')
plt.plot(x,profit,label='Profit')

plt.legend()
plt.show()
```

---

# 2️⃣0️⃣ 3D Surface Plot

```python
from mpl_toolkits.mplot3d import Axes3D
```

Common 3D plots:

* 3D Line Plot
* 3D Scatter Plot
* 3D Surface Plot
* 3D Wireframe Plot
* 3D Bar Plot

---

# Most Important for Data Science

✅ Line Plot
✅ Bar Chart
✅ Scatter Plot
✅ Histogram
✅ Box Plot
✅ Pie Chart

Master these six plots first—they cover most beginner Machine Learning, Pandas, and interview use cases.


Line Plot

Trend over ordered values

x	y
1	10
2	20
3	15
4	25
5	30

Bar Chart

Category comparison

subject	marks
Python	90
SQL	80
Excel	85

Scatter Plot

Relationship between variables

x	y
1	10
2	20
3	15
4	25
5	30

Pie Chart

Percentage distribution

skill	share
Python	50
SQL	30
Excel	20
