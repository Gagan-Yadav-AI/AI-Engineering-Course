# Day 14: Statistics

## 1. Introduction to Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is the crucial first step in data analysis. It involves analyzing datasets to summarize their main characteristics, often using visual methods, before diving into formal modeling.

* **Univariate Analysis:** Analyzing a **single variable** at a time to understand its distribution, central tendency, and spread.
* **Bivariate Analysis:** Analyzing the relationship between **two variables** to find correlations, patterns, or dependencies.

---

## 2. Measures of Central Tendency

Measures of central tendency provide a single value that represents the "center" or "typical value" of a dataset.

| Measure | Definition | Best Used For | Limitation |
| --- | --- | --- | --- |
| **Mean** | The arithmetic average of all data points. | Symmetric data without outliers (e.g., test scores). | Highly sensitive to extreme outliers. |
| **Median** | The middle value when data is sorted in ascending order. | Skewed data or data with outliers (e.g., income, house prices). | Doesn't use all data points explicitly. |
| **Mode** | The value(s) that appear most frequently in a dataset. | Categorical data (e.g., favorite color, car models). | Can be bi-modal, multi-modal, or have no mode at all. |

### Key Equations

* **Mean ($\mu$ or $\bar{x}$):** 
$$\bar{x} = \frac{\sum_{i=1}^{n} x_i}{n}$$


* **Median Formula (for grouped/continuous data):**

$$Median = L + \left( \frac{\frac{n}{2} - CF}{f} \right) \times h$$



*(Where $L$ = lower limit of median class, $CF$ = cumulative frequency, $f$ = frequency, $h$ = class width)*

---

## 3. Measures of Spread & Data Variability

Variability describes how scattered or spread out the data points are from each other and from the center.

### A. Range

The simplest measure of spread, calculated as the difference between the maximum and minimum values.


$$Range = X_{max} - X_{min}$$

### B. Percentiles & Interquartile Range (IQR)

* **Percentile:** A measure indicating the value below which a given percentage of observations fall (e.g., the 85th percentile is the value higher than 85% of the data).
* **Quartiles:** Divides the data into four equal parts:
* **Q1 (25th Percentile):** Median of the lower half.
* **Q2 (50th Percentile):** The Median itself.
* **Q3 (75th Percentile):** Median of the upper half.


* **Interquartile Range (IQR):** The distance between the 75th and 25th percentiles. It measures the spread of the middle 50% of the data and is highly robust to outliers.

$$IQR = Q_3 - Q_1$$



### C. Variance & Standard Deviation

* **Variance ($\sigma^2$ or $s^2$):** The average of the squared differences from the Mean. Squaring prevents positive and negative deviations from canceling each other out.
* **Standard Deviation ($\sigma$ or $s$):** The square root of the variance. It brings the unit of measurement back to the original scale of the data.

#### Math Formulations (Sample vs. Population)

| Type | Population | Sample |
| --- | --- | --- |
| **Variance** | $$\sigma^2 = \frac{\sum (x_i - \mu)^2}{N}$$

 | $$s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1}$$

 |
| **Standard Deviation** | $$\sigma = \sqrt{\frac{\sum (x_i - \mu)^2}{N}}$$

 | $$s = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n - 1}}$$

 |

> **Note on Bessel's Correction:** In the sample formulas, we divide by $n - 1$ instead of $n$. This corrects the bias in estimating the population parameters from a smaller sample.

---

## 4. Probability Distributions

A probability distribution is a mathematical function that describes the likelihood of obtaining the possible values that a random variable can take.

### Core Types of Distributions

1. **Discrete Distributions:** Used for variables with countable outcomes (e.g., rolling a die, number of customer complaints).
* *Examples:* Binomial, Poisson, Bernoulli distributions.


2. **Continuous Distributions:** Used for variables that can take any value within a given range/interval (e.g., height, weight, time).
* *Examples:* Normal, Uniform, Exponential distributions.



---

## 5. The Normal (Gaussian) Distribution

The Normal Distribution is a continuous probability distribution that is perfectly symmetrical around its center, creating a classic bell-shaped curve.

### Key Properties

* $\text{Mean} = \text{Median} = \text{Mode}$
* The curve is perfectly symmetric around the center.
* The total area under the curve is exactly $1$ (or 100%).

### The Empirical Rule (68-95-99.7 Rule)

In a perfect normal distribution, data falls within standard deviations of the mean in a highly predictable pattern:

* **$\mu \pm 1\sigma$** contains approximately **68.2%** of the data.
* **$\mu \pm 2\sigma$** contains approximately **转换95.4%** of the data.
* **$\mu \pm 3\sigma$** contains approximately **99.7%** of the data.

---

## 6. Distortions in Normal Distribution

Real-world data is rarely perfectly normal. We measure these imperfections using **Skewness** and **Kurtosis**.

### A. Skewness (Asymmetry)

Skewness measures the lack of symmetry in a distribution dataset.

* **Left / Negative Skew:** The left tail is longer. The mass of the distribution is concentrated on the right.
* *Relationship:* $\text{Mean} < \text{Median} < \text{Mode}$


* **Symmetrical (Zero Skew):** Perfect bell curve.
* *Relationship:* $\text{Mean} = \text{Median} = \text{Mode}$


* **Right / Positive Skew:** The right tail is longer. The mass of the distribution is concentrated on the left.
* *Relationship:* $\text{Mode} < \text{Median} < \text{Mean}$



[Image comparing negative skew, no skew, and positive skew curves with markers for mean median mode]

### B. Kurtosis (Tailedness)

Kurtosis measures the "tailedness" or the thickness of the tails of a distribution, indicating the presence of extreme values (outliers).

* **Mesokurtic (Kurtosis $\approx$ 3):** Normal distribution baseline.
* **Leptokurtic (Kurtosis $>$ 3):** Heavy tails and a sharp, high peak. This indicates a high presence of extreme outliers.
* **Platykurtic (Kurtosis $<$ 3):** Light tails and a flat, broad peak. Data is spread out evenly with fewer extreme outliers.

[Image showing leptokurtic mesokurtic and platykurtic distributions side by side]

---


---

Good luck pushing this to your GitHub repository! Let me know if you want to dive deeper into any specific math derivations or Python visualizations next.
