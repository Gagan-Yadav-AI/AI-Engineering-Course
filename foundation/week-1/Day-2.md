# Day 2 – BASIC FOUNDATION

## Data Science & Data Preparation

---

# 1. DATA SCIENCE

## What is Data Science?

**Data Science** is the field of extracting meaningful insights, patterns, and knowledge from data using statistics, programming, machine learning, and domain expertise to support decision-making.

### Simple Definition

> Data Science is the process of turning raw data into useful information that helps solve real-world problems.

---

## Why Data Science?

Organizations generate huge amounts of data every day. Data Science helps to:

✔ Make better business decisions

✔ Predict future outcomes

✔ Identify hidden patterns

✔ Automate processes

✔ Improve customer experience

✔ Reduce risks and costs

---

## Real-World Examples

| Industry      | Use Case                  |
| ------------- | ------------------------- |
| E-commerce    | Product Recommendations   |
| Banking       | Fraud Detection           |
| Healthcare    | Disease Prediction        |
| Telecom       | Customer Churn Prediction |
| Retail        | Sales Forecasting         |
| Manufacturing | Predictive Maintenance    |

---

## Core Components of Data Science

```text
                    DATA SCIENCE
                          │
      ┌───────────────────┼───────────────────┐
      │                   │                   │
 Statistics         Programming      Domain Knowledge
      │                   │                   │
      └───────────────────┼───────────────────┘
                          │
                  Machine Learning
                          │
                     Insights
```

---

# 2. DATA SCIENCE WORKFLOW

Data Science projects follow a structured process from identifying a problem to deploying a solution.

---

## Data Science Lifecycle

```text
1. Business Understanding
           ↓
2. Data Collection
           ↓
3. Data Understanding
           ↓
4. Data Preparation
           ↓
5. Modeling
           ↓
6. Evaluation
           ↓
7. Deployment & Monitoring
```

---

# 3. DATA SCIENCE WORKFLOW – PHASES

---

## 1. Business Understanding

### Objective

Understand the business problem and project goals.

### Key Activities

* Define objectives
* Identify stakeholders
* Understand business requirements
* Define success criteria

### Example

**Problem:** An online store wants to reduce customer churn.

**Goal:** Predict customers likely to leave.

### Output

✔ Business Problem Statement

✔ Success Metrics

✔ Project Scope

---

## 2. Data Collection

### Objective

Gather data from various sources.

### Data Sources

| Source        | Example           |
| ------------- | ----------------- |
| Databases     | SQL Server, MySQL |
| APIs          | Weather API       |
| Excel Files   | Sales Reports     |
| Websites      | Web Scraping      |
| Sensors       | IoT Devices       |
| Cloud Storage | AWS S3            |

### Output

✔ Raw Data

✔ Data Inventory

---

## 3. Data Understanding

### Objective

Explore the collected data and understand its characteristics.

### Activities

* Data Profiling
* Check Data Types
* Identify Missing Values
* Detect Outliers
* Understand Relationships

### Example Questions

* How many records exist?
* Which columns contain missing values?
* What patterns exist?

### Output

✔ Initial Data Assessment

✔ Data Quality Report

---

## 4. Data Preparation

### Objective

Transform raw data into a clean and usable format for analysis and modeling.

### Importance

Data preparation usually consumes **60–80% of project time** because model quality depends heavily on data quality.

### Activities

* Cleaning
* Transformation
* Integration
* Feature Engineering
* Data Formatting

### Output

✔ Clean Dataset

✔ Model-Ready Data

---

## 5. Modeling

### Objective

Build predictive or analytical models using prepared data.

### Common Techniques

| Category       | Examples          |
| -------------- | ----------------- |
| Regression     | Linear Regression |
| Classification | Decision Tree     |
| Clustering     | K-Means           |
| Deep Learning  | Neural Networks   |

### Output

✔ Trained Model

✔ Model Metrics

---

## 6. Evaluation

### Objective

Measure model performance and verify business requirements.

### Questions to Ask

* Is the model accurate?
* Does it solve the business problem?
* Can it be improved?

### Common Metrics

| Model Type     | Metrics                     |
| -------------- | --------------------------- |
| Classification | Accuracy, Precision, Recall |
| Regression     | MAE, RMSE, R²               |

### Output

✔ Evaluation Report

✔ Model Validation

---

## 7. Deployment & Monitoring

### Objective

Deploy the model into production and continuously monitor performance.

### Deployment Methods

* Web Applications
* Mobile Applications
* APIs
* Dashboards

### Monitoring Activities

* Performance Tracking
* Error Monitoring
* Data Drift Detection
* Model Retraining

### Output

✔ Production Model

✔ Monitoring Dashboard

---

# 4. DATA PREPARATION

## What is Data Preparation?

Data Preparation is the process of collecting, cleaning, transforming, and organizing raw data into a format suitable for analysis and machine learning.

### Simple Definition

> Data Preparation converts messy data into clean, structured, and reliable data.

---

## Why Data Preparation is Important?

### Poor Data → Poor Results

```text
Raw Data
   ↓
Data Preparation
   ↓
Quality Data
   ↓
Better Analysis
   ↓
Better Decisions
```

### Benefits

✔ Improved Accuracy

✔ Better Model Performance

✔ Reduced Errors

✔ Faster Analysis

✔ Reliable Insights

---

# 5. DATA PREPARATION STAGES

Data Preparation consists of several important stages.

---

## Stage 1: Data Collection

Gather data from multiple sources.

### Examples

* Databases
* Excel Files
* APIs
* Cloud Storage

### Output

Raw Data

---

## Stage 2: Data Cleaning

Identify and correct errors in data.

### Common Tasks

| Issue                | Example                           |
| -------------------- | --------------------------------- |
| Missing Values       | Blank Salary                      |
| Duplicate Records    | Same Customer Twice               |
| Incorrect Data       | Negative Age                      |
| Typographical Errors | "Banglore" instead of "Bangalore" |

### Output

Clean Data

---

## Stage 3: Data Integration

Combine data from different sources.

### Example

```text
Customer Data
      +
Order Data
      +
Payment Data
      ↓
Integrated Dataset
```

### Output

Unified Dataset

---

## Stage 4: Data Transformation

Convert data into a suitable format.

### Activities

* Standardization
* Normalization
* Aggregation
* Encoding Categories

### Example

| Before      | After                |
| ----------- | -------------------- |
| Male/Female | 0/1                  |
| 2025-06-01  | Standard Date Format |

### Output

Transformed Data

---

## Stage 5: Feature Engineering

Create new useful features from existing data.

### Examples

| Existing Data | New Feature   |
| ------------- | ------------- |
| Date of Birth | Age           |
| Order Date    | Day of Week   |
| Sales Data    | Profit Margin |

### Output

Enhanced Dataset

---

## Stage 6: Data Reduction

Reduce data volume while preserving important information.

### Techniques

* Feature Selection
* Sampling
* Dimensionality Reduction

### Benefits

✔ Faster Processing

✔ Reduced Storage

✔ Better Model Performance

### Output

Optimized Dataset

---

## Stage 7: Data Validation

Verify data quality before analysis.

### Validation Checks

✔ Completeness

✔ Accuracy

✔ Consistency

✔ Uniqueness

✔ Validity

### Output

Final Prepared Dataset

---

# DATA PREPARATION FLOW

```text
Data Collection
        ↓
Data Cleaning
        ↓
Data Integration
        ↓
Data Transformation
        ↓
Feature Engineering
        ↓
Data Reduction
        ↓
Data Validation
        ↓
Ready for Analysis & Modeling
