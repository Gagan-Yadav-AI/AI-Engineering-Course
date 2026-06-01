# Day 1 – BASIC FOUNDATION

## Foundation Notes

---

# 1. TYPES OF DATA

Data is a collection of facts, observations, or information that can be processed to gain insights.

---

## A. Types of Data by Structure

| Type                     | Definition                                                    | Example                     |
| ------------------------ | ------------------------------------------------------------- | --------------------------- |
| **Structured Data**      | Data organized in rows and columns with a fixed format.       | Excel, SQL Database         |
| **Semi-Structured Data** | Data with some organizational properties but no fixed schema. | JSON, XML, HTML             |
| **Unstructured Data**    | Data without a predefined format.                             | Images, Videos, PDFs, Audio |

### Visual Representation

```text
DATA
│
├── Structured
│   ├── Tables
│   └── Databases
│
├── Semi-Structured
│   ├── JSON
│   └── XML
│
└── Unstructured
    ├── Images
    ├── Videos
    └── Audio
```

---

## B. Types of Data by Nature

### 1. Quantitative (Numerical Data)

Data represented by numbers.

#### Types

| Type           | Definition        | Example                     |
| -------------- | ----------------- | --------------------------- |
| **Discrete**   | Countable values  | Number of Students          |
| **Continuous** | Measurable values | Height, Weight, Temperature |

---

### 2. Qualitative (Categorical Data)

Data represented by categories or labels.

#### Types

| Type        | Definition               | Example           |
| ----------- | ------------------------ | ----------------- |
| **Nominal** | Categories without order | Gender, Color     |
| **Ordinal** | Categories with order    | Low, Medium, High |

---

# 2. DATA ANALYTICS

Data Analytics is the process of examining, transforming, and analyzing data to discover useful information and support decision-making.

---

## Types of Data Analytics

### 1. Descriptive Analytics

**Question Answered:** What happened?

**Purpose:** Summarizes historical data.

**Examples**

* Monthly Sales Report
* Website Traffic Summary
* KPI Dashboard

---

### 2. Diagnostic Analytics

**Question Answered:** Why did it happen?

**Purpose:** Finds root causes of events.

**Examples**

* Why did sales decrease?
* Why did customer complaints increase?

---

### 3. Predictive Analytics

**Question Answered:** What is likely to happen?

**Purpose:** Forecasts future outcomes using historical data.

**Examples**

* Sales Forecasting
* Customer Churn Prediction
* Demand Forecasting

---

### 4. Prescriptive Analytics

**Question Answered:** What should we do?

**Purpose:** Suggests best actions to achieve desired outcomes.

**Examples**

* Product Recommendations
* Route Optimization
* Dynamic Pricing

---

## Analytics Flow

```text
Descriptive
     ↓
Diagnostic
     ↓
Predictive
     ↓
Prescriptive
```

---

# 3. DATA MINERS

A Data Miner is a professional who extracts valuable patterns, trends, and insights from large datasets.

---

## Types of Data Miners

### Business Data Miner

* Focuses on business problems
* Supports decision-making

### Statistical Data Miner

* Uses statistical techniques
* Identifies patterns and trends

### Machine Learning Miner

* Builds predictive models
* Uses AI algorithms

### Text Data Miner

* Extracts insights from text
* Used in sentiment analysis

### Web Data Miner

* Analyzes website traffic
* Studies user behavior

### Social Media Miner

* Analyzes social media data
* Tracks trends and customer opinions

---

# 4. DATA ENGINEERING

Data Engineering focuses on designing, building, and maintaining systems that collect, store, and process data.

---

## Core Concepts in Data Engineering

---

### 1. Data Pipeline

A sequence of processes that moves data from source to destination.

```text
Source
   ↓
Ingestion
   ↓
Transformation
   ↓
Storage
   ↓
Analytics
```

**Example:** Sales Data → ETL → Data Warehouse

---

### 2. Data Warehouse

A centralized repository for structured data optimized for reporting and analytics.

**Examples**

* Snowflake
* Amazon Redshift
* Google BigQuery

---

### 3. Data Lake

Stores raw structured, semi-structured, and unstructured data.

**Examples**

* AWS S3
* Azure Data Lake

---

### 4. Data Lakehouse

Combines features of Data Lake and Data Warehouse.

### Benefits

✔ Flexibility of Data Lake

✔ Performance of Data Warehouse

✔ Supports AI & Analytics

---

### 5. Batch vs Streaming Processing

| Feature    | Batch Processing | Streaming Processing |
| ---------- | ---------------- | -------------------- |
| Processing | Large chunks     | Real-time            |
| Speed      | Slow             | Fast                 |
| Example    | Daily Reports    | Live Stock Market    |

---

# 5. BIG DATA

Big Data refers to datasets too large or complex for traditional data processing systems.

---

## 5 V's of Big Data

| V            | Meaning                   |
| ------------ | ------------------------- |
| **Volume**   | Massive amount of data    |
| **Velocity** | Speed of data generation  |
| **Variety**  | Different data formats    |
| **Veracity** | Data quality and accuracy |
| **Value**    | Useful insights obtained  |

---

### Big Data Visualization

```text
           BIG DATA
                │
 ┌──────────────┼──────────────┐
 │              │              │
Volume      Velocity      Variety
 │              │              │
 └──────────────┼──────────────┘
                │
          Veracity
                │
             Value
```

---

# 6. DATA SIZE UNITS

## Decimal System (Storage Manufacturers)

| Unit | Value       |
| ---- | ----------- |
| 1 KB | 1,000 Bytes |
| 1 MB | 1,000 KB    |
| 1 GB | 1,000 MB    |
| 1 TB | 1,000 GB    |
| 1 PB | 1,000 TB    |
| 1 EB | 1,000 PB    |

---

## Binary System (Computers)

| Unit  | Value       |
| ----- | ----------- |
| 1 KiB | 1,024 Bytes |
| 1 MiB | 1,024 KiB   |
| 1 GiB | 1,024 MiB   |
| 1 TiB | 1,024 GiB   |
| 1 PiB | 1,024 TiB   |
| 1 EiB | 1,024 PiB   |

---

## Quick Comparison

| Decimal | Binary |
| ------- | ------ |
| KB      | KiB    |
| MB      | MiB    |
| GB      | GiB    |
| TB      | TiB    |

---

# 7. ROLES OF ANALYTICS IN AN ORGANIZATION

Analytics helps organizations make data-driven decisions.

---

## Top 10 Roles

| Role                   | Responsibility                  |
| ---------------------- | ------------------------------- |
| Data Analyst           | Analyze data and create reports |
| Data Scientist         | Build ML models                 |
| Data Engineer          | Build data infrastructure       |
| Business Analyst       | Solve business problems         |
| Data Architect         | Design data systems             |
| ML Engineer            | Deploy ML models                |
| BI Developer           | Build dashboards                |
| Database Administrator | Manage databases                |
| Data Steward           | Ensure data quality             |
| Analytics Manager      | Lead analytics teams            |

---

# 8. CRISP-DM MODEL

(Cross Industry Standard Process for Data Mining)

A standard framework used in analytics and machine learning projects.

---

## Six Phases

```text
1. Business Understanding
          ↓
2. Data Understanding
          ↓
3. Data Preparation
          ↓
4. Modeling
          ↓
5. Evaluation
          ↓
6. Deployment
```

---

## Phase Details

| Phase                  | Purpose                  |
| ---------------------- | ------------------------ |
| Business Understanding | Define business goals    |
| Data Understanding     | Explore and collect data |
| Data Preparation       | Clean and transform data |
| Modeling               | Build models             |
| Evaluation             | Validate performance     |
| Deployment             | Deliver solution         |

---

# 9. DOMAIN ANALYSIS

Domain Analysis is the study of the business area before starting analytics work.

---

## Why Domain Analysis?

✔ Understand business objectives

✔ Understand KPIs

✔ Identify stakeholders

✔ Understand constraints

✔ Define project scope

---

## Example Domains

| Domain     | Example                |
| ---------- | ---------------------- |
| Banking    | Loan Prediction        |
| Healthcare | Disease Analysis       |
| Retail     | Sales Forecasting      |
| Telecom    | Customer Churn         |
| E-commerce | Product Recommendation |
| Finance    | Fraud Detection        |

---

# 10. EXPLORATORY DATA ANALYSIS (EDA)

EDA is the process of exploring and understanding data before building models.

---

## Objectives of EDA

✔ Understand data structure

✔ Detect missing values

✔ Find outliers

✔ Discover patterns

✔ Identify relationships

---

## Common EDA Techniques

### Univariate Analysis

Analysis of one variable.

Examples:

* Histogram
* Box Plot

---

### Bivariate Analysis

Analysis of two variables.

Examples:

* Scatter Plot
* Correlation

---

### Multivariate Analysis

Analysis of multiple variables.

Examples:

* Heatmaps
* Pair Plots

---

## EDA Workflow

```text
Collect Data
      ↓
Clean Data
      ↓
Understand Data
      ↓
Visualize Data
      ↓
Find Patterns
      ↓
Generate Insights
```

---

# DAY 1 SUMMARY

```text
DATA
 │
 ├── Types of Data
 │
 ├── Data Analytics
 │      ├─ Descriptive
 │      ├─ Diagnostic
 │      ├─ Predictive
 │      └─ Prescriptive
 │
 ├── Data Miners
 │
 ├── Data Engineering
 │      ├─ Pipeline
 │      ├─ Warehouse
 │      ├─ Lake
 │      ├─ Lakehouse
 │      └─ Batch vs Streaming
 │
 ├── Big Data (5 V's)
 │
 ├── Data Size Units
 │
 ├── Analytics Roles
 │
 ├── CRISP-DM
 │
 ├── Domain Analysis
 │
 └── Exploratory Data Analysis
```

This format is GitHub-ready Markdown and will render cleanly with headings, tables, boxes, and diagrams similar to your reference notes.
