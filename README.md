# Marketing Campaign Customer Analysis

## Project Overview

This project focuses on understanding customer behavior and marketing campaign performance using a customer marketing dataset. The analysis involves data exploration, data cleaning, feature engineering, and preparation of the dataset for further Exploratory Data Analysis (EDA) and customer segmentation.

The objective is to transform raw customer data into a clean and structured format that can be used to generate business insights and support marketing decisions.

---

## Dataset Information

The dataset contains information about customers, including:

- Demographic details
  - Year of Birth
  - Education
  - Marital Status
  - Income

- Household information
  - Number of children at home
  - Number of teenagers at home

- Product spending
  - Wine
  - Fruits
  - Meat Products
  - Fish Products
  - Sweet Products
  - Gold Products

- Purchase behavior
  - Store Purchases
  - Web Purchases
  - Catalog Purchases

- Marketing campaign responses
  - Campaign acceptance history
  - Response to the latest campaign

---

## Project Objectives

1. Understand the structure of the dataset.
2. Identify missing values and data quality issues.
3. Clean and preprocess the dataset.
4. Create meaningful features for analysis.
5. Prepare the dataset for visualization and customer segmentation.

---

## Task 1: Data Understanding and Preprocessing

### Dataset Exploration

The following operations were performed:

```python
df.head()
df.shape
df.columns
df.info()
```

These commands were used to:

- Understand the dataset structure
- Examine column names
- Identify data types
- Determine the number of records and features

### Missing Value Analysis

```python
df.isnull().sum()
```

Findings:
- Missing values were identified in the Income column.
- Appropriate imputation techniques were applied to handle missing data.

### Duplicate Record Check

```python
df.duplicated().sum()
```

Purpose:
- Identify duplicate customer records.
- Maintain data integrity.

### Date Conversion

```python
df['Dt_Customer'] = pd.to_datetime(
    df['Dt_Customer'],
    dayfirst=True
)
```

Purpose:
- Convert customer enrollment date into datetime format.
- Enable future time-based analysis.

### Feature Engineering

#### Age Calculation

```python
df['Age'] = 2026 - df['Year_Birth']
```

Created a new Age feature from Year_Birth.

#### Total Spending

```python
df['Total_Spending'] = (
    df['MntWines'] +
    df['MntFruits'] +
    df['MntMeatProducts'] +
    df['MntFishProducts'] +
    df['MntSweetProducts'] +
    df['MntGoldProds']
)
```

Created a Total_Spending feature to represent overall customer expenditure.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- VS Code
- GitHub

---

## Key Learning Outcomes

- Data loading and inspection using Pandas
- Data cleaning and preprocessing techniques
- Missing value handling
- Duplicate record detection
- Date transformation
- Feature engineering
- Preparing datasets for advanced analytics

---
## Task 2: Exploratory Data Analysis (EDA)

## Objective
The objective of this task was to perform Exploratory Data Analysis (EDA) on the Marketing Campaign dataset to identify customer demographics, spending patterns, purchasing behavior, and relationships between different variables.

---

## Visualizations Performed

- Age Distribution Analysis
- Income Distribution Analysis
- Education Distribution Analysis
- Marital Status Analysis
- Product Spending Analysis
- Purchase Channel Analysis
- Correlation Heatmap

---

## Key Insights

- Most customers belong to the middle-aged group, with the highest concentration between 45 and 65 years.
- The majority of customers fall within a moderate income range, while a small number of high-income outliers are present.
- Graduation is the most common education level among customers.
- Married customers represent the largest customer segment in the dataset.
- Wine products generate the highest customer spending, followed by Meat products.
- Store purchases are the most preferred purchase channel, followed by web purchases.
- Catalog purchases contribute the lowest number of purchases.
- Income shows a positive relationship with Total Spending, indicating that higher-income customers generally spend more.
- Customers who purchase more frequently tend to have higher overall spending.
- Product spending categories exhibit positive correlations, suggesting that customers spending more in one category often spend more in others.

---

## Conclusion

The Exploratory Data Analysis revealed valuable insights into customer demographics, spending habits, and purchasing preferences. The results indicate that middle-aged, moderately to highly earning customers contribute significantly to revenue. Wine and Meat products are the most popular spending categories, while physical stores remain the preferred purchase channel. These findings can help businesses improve customer targeting, optimize marketing campaigns, and enhance product promotion strategies.

---

## Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook
---
# Task 3: Data Visualization Dashboard

## Customer Purchase & Campaign Analysis Dashboard

### Overview
This project presents an interactive Power BI dashboard designed to analyze customer purchasing behavior, spending patterns, marketing campaign performance, and demographic insights. The dashboard helps identify customer preferences and key business trends through visual analytics.

### Tools Used
- Power BI
- Power Query
- DAX
- CSV Dataset

### Dashboard Features
- Total Customers
- Average Income
- Average Age
- Total Spending
- Spending by Product Category
- Purchase Channel Analysis
- Income vs Total Spending
- Campaign Acceptance Analysis
- Customer Marital Status Distribution

### Key Insights
- Wine products contribute the highest customer spending.
- Store purchases are the most preferred purchase channel.
- Higher-income customers generally tend to spend more.
- Marketing campaign responses vary across campaigns.
- Married and Together customers represent a significant customer segment.

### Skills Demonstrated
- Data Cleaning
- Data Transformation
- Data Modeling
- DAX Measures
- Data Visualization
- Dashboard Design

### Dashboard Preview



---

## Author

**Swarangi Bhagwat**

Aspiring Data Analyst | Python | SQL | Power BI | Data Analytics Enthusiast

