Data Analytics — Week 1
Basic Foundations
Types of Data · Analytics Types · Data Engineering · Big Data · Roles · CRISP-DM · EDA
Types of Data
Analytics Types
Data Mining
Data Engineering
Big Data 5Vs
Data Size Units
Roles in Analytics
CRISP-DM
Domain Analysis
EDA
01
Types of Data
Data can be classified in two major ways: by structure (how it is organized/stored) and by nature (what kind of values it holds).
A. By Structure
Structured
Data organized in a fixed format with rows and columns — like a spreadsheet or database table.
Example: Customer table with name, age, city columns
Semi-structured
Data that has some organizational properties but doesn't fit neatly into rows/columns. Has tags or markers.
Example: JSON, XML, email headers
Unstructured
Data with no predefined format. Most data in the world is unstructured and harder to analyze directly.
Example: Videos, images, audio, social media posts
B. By Nature
Quantitative (Numerical)
Data that can be measured and expressed as numbers. Answers "how many" or "how much".
Type	Description	Example
Discrete	Countable whole numbers	No. of students: 30
Continuous	Any value in a range	Height: 5.7 ft
Qualitative (Categorical)
Data that represents categories or labels. Answers "what type" or "which group".
Type	Description	Example
Nominal	No natural order	Colors: red, blue
Ordinal	Has natural order	Rating: Good > Average
02
Types of Data Analytics
The four types form a progression — from understanding the past to shaping the future. Each answers a different business question.
1
Descriptive
"What happened?"
2
Diagnostic
"Why did it happen?"
3
Predictive
"What will happen?"
4
Prescriptive
"What should we do?"
1. Descriptive Analytics
Summarizes historical data
Uses past data to describe what has already occurred. It is the most common form — dashboards, reports, and charts.
Example: Monthly sales report showing ₹5L revenue in April
2. Diagnostic Analytics
Finds root causes
Drills deeper into descriptive data to find WHY something happened. Involves data drilling, correlation, and cause analysis.
Example: Sales dropped in April → why? Festive season ended
3. Predictive Analytics
Forecasts future outcomes
Uses statistical models and machine learning to predict future events based on patterns in historical data.
Example: Predict next month's sales will be ₹4.8L using ML model
4. Prescriptive Analytics
Recommends best action
The most advanced type — suggests specific actions to take. Uses optimization, simulation, and AI to guide decisions.
Example: "Offer 20% discount in May to recover lost sales"
Complexity increases from Descriptive → Prescriptive. Most organizations use all four together.
03
Data Mining
Definition
Data Mining is the process of discovering hidden patterns, correlations, and useful insights from large datasets using statistical, mathematical, and computational techniques.
Example: A bank mines transaction data to detect fraud by spotting unusual spending patterns.
Common Data Mining Techniques
Classification
Assigns data into predefined categories. Ex: spam vs not spam email.
Clustering
Groups similar data points together without labels. Ex: customer segments.
Association
Finds items that co-occur. Ex: "People who buy bread also buy butter."
Regression
Predicts a numerical value. Ex: predict house price from area.
Anomaly Detection
Identifies unusual patterns. Ex: fraud detection in banking.
Summarization
Creates compact descriptions of data. Ex: average age of customers = 32.
04
Data Engineering — Core Concepts
Data Engineering is the practice of designing and building systems that collect, store, and process data at scale for analysis.
1. Data Pipeline
Automated flow of data from source to destination
A series of steps that move, transform, and load (ETL) data from one system to another automatically.
Source
DB / API / File
→
Extract
Pull data
→
Transform
Clean/Format
→
Load
Store it
→
Destination
Warehouse
Example: Daily sales data from POS system → cleaned → loaded into warehouse for reporting
2. Data Warehouse
Structured repository for analysis
A centralized storage system that stores large amounts of structured, processed historical data optimized for querying and reporting.
Example: Amazon Redshift, Google BigQuery, Snowflake
3. Data Lake
Raw data storage of all formats
A massive storage repository that holds raw data in its original format — structured, semi-structured, and unstructured — until needed.
Example: AWS S3, Azure Data Lake — stores logs, images, CSVs together
4. Data Lakehouse
Best of both Data Lake + Data Warehouse
A modern architecture that combines the flexibility of a data lake (storing raw data) with the structure and query performance of a data warehouse.
Example: Databricks Delta Lake, Apache Iceberg
Warehouse vs Lake vs Lakehouse — Quick Comparison
Feature	Data Warehouse	Data Lake	Data Lakehouse
Data Type	Structured only	All types (raw)	All types
Data State	Processed	Raw/unprocessed	Both
Query Speed	Fast	Slow	Fast
Cost	High	Low	Medium
Best For	BI Reports	ML / Data Science	Both use cases
5. Batch vs Streaming Processing
Batch Processing
Data is collected over time and processed all at once in chunks (a "batch"). Simple and cost-effective but not real-time.
Example: Generating end-of-day payroll reports every night
Streaming Processing
Data is processed continuously in real-time as it arrives. More complex but enables immediate insights.
Example: UPI fraud detection — every transaction checked instantly
05
Big Data — The 5 V's
Big Data refers to extremely large datasets that traditional software cannot process efficiently. It is characterized by the 5 V's:
V
Volume
The enormous amount of data generated — terabytes to petabytes
V
Velocity
The speed at which data is generated and processed — real-time or near real-time
V
Variety
Different types of data — text, images, videos, logs, JSON
V
Veracity
The accuracy and reliability of data — incomplete or noisy data is a big challenge
V
Value
The usefulness of data — only valuable if it leads to actionable insights
Real-world example: WhatsApp generates 100 billion messages/day (Volume), in real-time (Velocity), as text/images/video (Variety). Not all are clean (Veracity). Businesses extract marketing insights from it (Value).
06
Data Size Units
Decimal System (SI — base 10)
Unit	Symbol	Value
Kilobyte	KB	1,000 bytes (10³)
Megabyte	MB	1,000 KB = 10⁶ bytes
Gigabyte	GB	1,000 MB = 10⁹ bytes
Terabyte	TB	1,000 GB = 10¹² bytes
Petabyte	PB	1,000 TB = 10¹⁵ bytes
Exabyte	EB	1,000 PB = 10¹⁸ bytes
Zettabyte	ZB	1,000 EB = 10²¹ bytes
Yottabyte	YB	1,000 ZB = 10²⁴ bytes
Used by storage manufacturers and internet speed measurements
Binary System (IEC — base 2)
Unit	Symbol	Value
Kibibyte	KiB	1,024 bytes (2¹⁰)
Mebibyte	MiB	1,024 KiB = 2²⁰ bytes
Gibibyte	GiB	1,024 MiB = 2³⁰ bytes
Tebibyte	TiB	1,024 GiB = 2⁴⁰ bytes
Pebibyte	PiB	1,024 TiB = 2⁵⁰ bytes
Exbibyte	EiB	1,024 PiB = 2⁶⁰ bytes
Zebibyte	ZiB	1,024 EiB = 2⁷⁰ bytes
Yobibyte	YiB	1,024 ZiB = 2⁸⁰ bytes
Used by operating systems; 1 GiB = 1.073 GB (hence "missing" storage)
Real-world Size Reference
Size	What it holds
1 KB	A short text message or 1 page of plain text
1 MB	A high-quality photo or a 1-minute audio clip (low quality)
1 GB	A full HD movie (compressed) or ~650 MB music album
1 TB	~250,000 photos or 500 hours of HD video
1 PB	All US academic research libraries combined
1 ZB	Total internet traffic created in the world each year (~2020)
07
Roles in Analytics (Top 10)
1. Data Analyst
Interprets data, creates reports and dashboards, answers business questions using SQL, Excel, and BI tools like Power BI.
2. Data Scientist
Builds ML models, performs statistical analysis, and generates predictive insights using Python/R. Combines coding + statistics.
3. Data Engineer
Designs and maintains pipelines, warehouses, and data infrastructure. Focuses on making data accessible and reliable.
4. Business Intelligence Developer
Creates interactive dashboards and reports. Connects BI tools (Tableau, Power BI) to data sources for decision-makers.
5. Machine Learning Engineer
Deploys and maintains ML models in production environments. Bridge between data science and software engineering.
6. Data Architect
Designs the overall data ecosystem — warehouses, lakes, lakehouses. Sets standards and frameworks for data storage.
7. Database Administrator (DBA)
Manages, maintains, and secures databases. Handles performance tuning, backups, and user access control.
8. Analytics Manager
Leads analytics teams, aligns data strategy with business goals, communicates insights to senior leadership.
9. Chief Data Officer (CDO)
C-suite executive responsible for the overall data strategy, governance, and monetization of data assets.
10. Data Governance Analyst
Ensures data quality, compliance (GDPR), and defines policies for who can access and use data.
08
CRISP-DM Model
CRISP-DM stands for Cross-Industry Standard Process for Data Mining. It is the most widely used framework for carrying out data science and analytics projects. It provides a structured, repeatable process.
1
Business Understanding
Define the problem, goals, and success criteria from a business perspective
2
Data Understanding
Collect initial data, explore it, identify quality issues
3
Data Preparation
Clean, transform, and engineer features; build the final dataset
4
Modeling
Select and apply modeling techniques; train and tune algorithms
5
Evaluation
Assess if the model meets business goals; review the process
6
Deployment
Deploy model to production; monitor and maintain results
CRISP-DM is iterative — you often loop back. For example, after Evaluation you may return to Data Preparation or even Business Understanding.
Phase	Key Question	Output
Business Understanding	What problem are we solving?	Project plan, success criteria
Data Understanding	What data do we have?	Data description, quality report
Data Preparation	How do we clean it?	Final cleaned dataset
Modeling	Which algorithm to use?	Trained model
Evaluation	Is it good enough?	Model evaluation report
Deployment	How to use in real life?	Deployed model / dashboard
09
Domain Analysis
Definition
Understanding the business context before analyzing data
Domain Analysis is the process of gaining deep knowledge about the industry, business rules, and domain-specific context before starting any data analysis. It ensures that insights are relevant, accurate, and actionable.
Example: Before analyzing hospital data, understand medical terminology, patient workflows, and compliance requirements (HIPAA)
Why Domain Analysis Matters
Avoid Misinterpretation
Without domain knowledge, you may draw wrong conclusions from correct data. Ex: A high "bounce rate" in retail is bad, but in news sites it can be normal.
Better Feature Engineering
Domain experts know which variables are important. In lending: "employment type" matters more than "email domain".
Define Correct KPIs
Each domain has unique success metrics. Healthcare uses "readmission rate"; e-commerce uses "cart abandonment rate".
Regulatory Compliance
Finance and healthcare have strict data laws. Domain knowledge prevents legal issues during analysis.
Steps in Domain Analysis
Step	Activity
1. Identify domain	Understand the industry — finance, healthcare, retail, etc.
2. Learn terminology	Know key terms — "churn", "NPS", "LTV", "SKU", etc.
3. Map business processes	Understand how the business operates end-to-end
4. Identify stakeholders	Know who uses the data and for what decisions
5. Define KPIs	Agree on what metrics define success or failure
10
Exploratory Data Analysis (EDA)
Definition
First look at data before formal modeling
EDA is the process of visually and statistically exploring a dataset to understand its structure, patterns, distributions, outliers, and relationships before building models or drawing conclusions. Popularized by statistician John Tukey.
Example: Before predicting house prices, plot histograms, check for nulls, find correlations between area and price
Key Steps in EDA
1. Understand the Data
Check shape (rows × columns), data types, sample rows. Use df.info(), df.head() in Python.
2. Handle Missing Values
Identify nulls using df.isnull().sum(). Decide: drop, fill with mean/median/mode, or flag them.
3. Summary Statistics
Compute mean, median, mode, std, min, max, quartiles. Use df.describe(). Tells you the "shape" of numeric data.
4. Distribution Analysis
Use histograms, box plots, violin plots. Check for skewness (left/right skewed) and normality.
5. Outlier Detection
Identify extreme values using IQR method or z-score. Decide whether to remove, cap, or investigate them.
6. Correlation Analysis
Use heatmaps to find relationships between variables. High correlation = variables move together. Helps feature selection.
7. Categorical Analysis
Bar charts and frequency tables for categorical columns. Find imbalanced classes (e.g., 95% "No" vs 5% "Yes").
8. Bivariate Analysis
Explore relationship between TWO variables. Scatter plots for num-num, box plots for cat-num pairs.
EDA Visualization Guide
Chart Type	Used For	Example Use
Histogram	Distribution of a single numerical variable	Age distribution of customers
Box Plot	Spread, median, and outliers	Salary range by department
Bar Chart	Comparing categories	Sales by product category
Scatter Plot	Relationship between two numerical variables	Height vs Weight
Heatmap	Correlation matrix between all variables	Feature correlation in ML dataset
Pie Chart	Proportions of a whole (use sparingly)	Market share by brand
Line Chart	Trends over time	Monthly revenue over 2 years
Violin Plot	Distribution + density shape	Score distribution by group
EDA is not a one-time step — it is iterative. Each finding leads to more questions. A good EDA often takes 40–60% of the total project time.
