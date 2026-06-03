## Day 14: Statistics


---

## 1. Outliers & Distribution Anomalies

An **outlier** is a data point that differs significantly from the rest of the dataset. They can be caused by experimental error, faulty measurements, or genuine, rare anomalies.

### Detecting Outliers

* **Z-Score Method:** Measures how many standard deviations a data point is from the mean.
* **IQR Method (Interquartile Range):** Uses the middle 50% of the data.
* $\text{Lower Bound} = Q1 - 1.5 \times IQR$
* $\text{Upper Bound} = Q3 + 1.5 \times IQR$



### Handling Outliers

1. **Trimming/Dropping:** Removing the outlier rows completely (use only if data is corrupted).
2. **Capping/Winsorization:** Replacing outliers with the maximum or minimum acceptable boundary values.
3. **Transformation:** Applying mathematical operations (like log) to reduce the impact of extreme values.

---

## 2. Core Statistical Theorems & Functions

### Central Limit Theorem (CLT)

The CLT states that regardless of the original distribution of the population, the **sampling distribution of the sample mean** will approach a normal distribution as the sample size ($n$) becomes large (typically $n \ge 30$).

> **Why it matters:** It allows us to perform hypothesis testing and make inferences about a population mean even if the underlying data is skewed.

### Probability Density Function (PDF) vs. Cumulative Distribution Function (CDF)

| Feature | Probability Density Function (PDF) | Cumulative Distribution Function (CDF) |
| --- | --- | --- |
| **Definition** | Represents the probability of a continuous random variable falling within a particular range. | Represents the probability that a random variable is less than or equal to a specific value. |
| **Formula Context** | Area under the curve between two points $a$ and $b$ gives the probability. | $F(x) = P(X \le x)$ |
| **Output** | Shows the "density" or likelihood of specific values. | Cumulative probability starting from 0 and ending at 1 (or 100%). |

### Standard Normal Distribution & Z-Score

A **Normal Distribution** is a symmetric, bell-shaped curve characterized by its mean ($\mu$) and standard deviation ($\sigma$).

The **Standard Normal Distribution** is a special case where:

* $\text{Mean }(\mu) = 0$
* $\text{Standard Deviation }(\sigma) = 1$

#### The Z-Score Formula

To convert any normal distribution into a standard normal distribution, we calculate the Z-score for each data point:

$$Z = \frac{x - \mu}{\sigma}$$

* **Outliers in Z-Score:** In a standard normal distribution, **99.7%** of the data falls within 3 standard deviations. Therefore, any data point with a **$Z\text{-score} > 3$ or $Z\text{-score} < -3$** is generally flagged as an outlier.

### Quantile-Quantile (Q-Q) Plots

A **Q-Q Plot** is a visual tool used to determine if a dataset follows a specific theoretical distribution (usually a normal distribution).

* **How to read it:** It plots the quantiles of your sample data against the quantiles of a theoretical distribution.
* If the points fall roughly along a **straight diagonal line ($y = x$)**, the data is normally distributed. Deviations from the line indicate skewness or heavy tails.

---

## 3. Correcting Distortion in Normal Distribution

Many machine learning algorithms (like Linear Regression and Logistic Regression) perform better when features are normally distributed. If your data is skewed, you can use mathematical transformations to correct the distortion.

```
[Right/Positively Skewed Data] ---> Apply Transformation ---> [Normally Distributed Data]

```

### Transformation Techniques

* **Log Transformation:** * Formula: $y = \log(x)$
* Best Use: Strongly **right-skewed** data. It compresses the long tail of large values. *Note: Cannot be applied to zero or negative values.*


* **Square Root Transformation:** * Formula: $y = \sqrt{x}$
* Best Use: Mildly **right-skewed** data. Gentler than log transformation.


* **Reciprocal Transformation:** * Formula: $y = \frac{1}{x}$
* Best Use: Significantly reverses the data relationship; useful when dealing with rates or ratios.


* **Box-Cox Transformation:** * A parametric transformation that automatically finds the optimal power parameter ($\lambda$) to transform data into a normal distribution.
* Formula:

$$y = \begin{cases} \frac{x^\lambda - 1}{\lambda} & \text{if } \lambda \neq 0 \\ \log(x) & \text{if } \lambda = 0 \end{cases}$$


* *Constraint:* Requires all data values to be strictly strictly positive ($x > 0$).



---

## 4. Measures of Distance & Metrics

Distance metrics are crucial for distance-based machine learning models like **K-Nearest Neighbors (KNN)**, **K-Means Clustering**, and **Support Vector Machines (SVM)**.

### The Distance Formulas

#### 1. Euclidean Distance

The straight-line distance between two points in a Euclidean space (derived from the Pythagorean theorem).


$$d = \sqrt{\sum_{i=1}^{n} (x_i - y_i)^2}$$

#### 2. Manhattan Distance (City Block / Taxicab)

The distance measured along axes at right angles. It calculates the absolute differences between coordinates.


$$d = \sum_{i=1}^{n} |x_i - y_i|$$

#### 3. Minkowski Distance

A generalized metric framework that encompasses both Euclidean and Manhattan distances.


$$d = \left( \sum_{i=1}^{n} |x_i - y_i|^p \right)^{\frac{1}{p}}$$

* If **$p = 1$**: It becomes **Manhattan Distance**.
* If **$p = 2$**: It becomes **Euclidean Distance**.

### Use Cases of Distance Metrics

* **Euclidean:** Default metric for most spatial data or continuous features where straight-line paths matter. Highly sensitive to magnitude and outliers.
* **Manhattan:** Preferred when dealing with **high-dimensional data** or when features represent grid-like attributes (e.g., city pathways, chessboards).
* **Minkowski:** Used when you want to tune the distance metric as a hyperparameter ($p$) to fit your specific dataset performance.

---

## 5. Covariance

**Covariance** measures the directional relationship between two random variables. It tells you whether two variables increase or decrease together.

### Formula

$$\text{Cov}(X, Y) = \frac{\sum (X_i - \bar{X})(Y_i - \bar{Y})}{n - 1}$$

### Interpreting Covariance Values

* **Positive Covariance ($>0$):** Indicates that when variable $X$ increases, variable $Y$ tends to increase as well.
* **Negative Covariance ($<0$):** Indicates that when variable $X$ increases, variable $Y$ tends to decrease.
* **Zero Covariance ($=0$):** Indicates that there is no linear relationship between the two variables.

> ⚠️ **Limitation:** Covariance only indicates the **direction** of the relationship, not the strength. Because it depends on the scale of the data, you cannot easily compare the covariance of two different asset pairs. (To find the strength, we normalize it to get the **Correlation Coefficient**).

---
