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

## Future Work

- Exploratory Data Analysis (EDA)
- Customer Segmentation
- RFM Analysis
- Data Visualization
- Marketing Campaign Performance Analysis
- Dashboard Development using Power BI

---

## Author

**Swarangi Bhagwat**

Aspiring Data Analyst | Python | SQL | Power BI | Data Analytics Enthusiast

