# Day 15: Statistic

---

# Hypothesis Testing

Hypothesis Testing is a statistical method used to make decisions or draw conclusions about a population based on sample data.

---

## Types of Hypotheses

### 1. Simple Hypothesis

A hypothesis that specifies the population parameter completely.

**Example:**
H₀: μ = 50

---

### 2. Composite Hypothesis

A hypothesis that does not specify the parameter completely.

**Example:**
H₁: μ ≠ 50

---

### 3. Null Hypothesis (H₀)

* Assumes no effect, no difference, or no relationship.
* Considered true until sufficient evidence suggests otherwise.

**Example:**
H₀: The average salary is ₹50,000.

---

### 4. Alternative Hypothesis (H₁ or Ha)

* Opposes the null hypothesis.
* Represents the claim being tested.

**Example:**
H₁: The average salary is not ₹50,000.

---

## P-Value

The probability of obtaining results as extreme as the observed results, assuming the null hypothesis is true.

### Decision Rule

* **P-value ≤ Significance Level (α):** Reject H₀
* **P-value > Significance Level (α):** Fail to Reject H₀

Common significance level:

α = 0.05 (5%)

---

## Critical Region

The range of values that leads to rejection of the null hypothesis.

### Regions

1. Acceptance Region
2. Rejection (Critical) Region

If the test statistic falls inside the critical region → Reject H₀.

---

# Process of Hypothesis Testing

1. Define Null Hypothesis (H₀)
2. Define Alternative Hypothesis (H₁)
3. Choose Significance Level (α)
4. Select Appropriate Test
5. Calculate Test Statistic
6. Find P-value or Critical Value
7. Make Decision
8. Draw Conclusion

---

# Applications of Hypothesis Testing

* Business decision making
* Product quality testing
* Medical research
* Market analysis
* A/B testing
* Manufacturing process improvement
* Data analytics and machine learning validation

---

# Types of Hypothesis Tests

## Parametric Tests

Used when data follows a normal distribution and meets specific assumptions.

### Z-Test

Used when:

* Sample size is large (n > 30)
* Population variance is known

### Student's t-Test

Used when:

* Sample size is small
* Population variance is unknown

### Paired t-Test

Used to compare two related samples.

**Example:**
Before vs After training scores.

### One-Way ANOVA

Used to compare means of three or more groups.

**Example:**
Comparing sales performance across multiple regions.

---

## Non-Parametric Tests

Used when data does not satisfy parametric assumptions.

### Chi-Square Test (χ²)

Used to test:

* Independence of variables
* Goodness of fit

**Example:**
Checking whether customer preference depends on gender.

---
