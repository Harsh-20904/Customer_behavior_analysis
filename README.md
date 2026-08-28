# Customer_behavior_analysis
This project focuses on analyzing customer behavior and purchasing patterns using Python (Pandas), MySQL, and Power BI. The goal is to transform raw customer data into meaningful insights that can help understand customer segments, purchasing frequency, spending patterns, and overall customer engagement.

#Customer Behavior Data Analytics Project

# Overview

This project presents an **end-to-end data analytics workflow** focused on understanding **customer behavior, purchasing patterns, and customer segmentation**.

The project starts with a raw dataset and progresses through **data loading, Exploratory Data Analysis (EDA), data cleaning, SQL analysis using MySQL, and interactive dashboard development in Power BI**. A detailed analytical report and project presentation were also created using **Gamma**.

The objective is to transform raw customer data into meaningful insights that can support better understanding of customer behavior and business decision-making.


# Project Objectives

* Understand customer purchasing behavior
* Perform Exploratory Data Analysis (EDA)
* Clean and preprocess raw data
* Store and analyze data using MySQL
* Create meaningful customer segments
* Identify purchasing and spending patterns
* Build an interactive Power BI dashboard
* Present key findings through a report and presentation


# Dataset

The dataset contains customer-related information used to analyze purchasing behavior.

Typical attributes include:

* Customer information
* Purchase history
* Purchase frequency
* Spending/purchase amount
* Customer demographics
* Customer segments
* Other behavioral attributes

> **Note:** The dataset used in this project is included in the repository.



# Tools & Technologies

| Tool                     | Purpose                                 |
| ------------------------ | --------------------------------------- |
| **Python**               | Data analysis and preprocessing         |
| **Pandas**               | Data cleaning and manipulation          |
| **Matplotlib / Seaborn** | Data visualization during EDA           |
| **MySQL**                | Data storage and SQL analysis           |
| **SQL**                  | Querying and customer behavior analysis |
| **Power BI**             | Interactive dashboard and visualization |
| **Gamma**                | Project report and presentation         |

---

# Project Workflow

Raw Dataset
     ↓
Python / Pandas
     ↓
Exploratory Data Analysis
     ↓
Data Cleaning & Transformation
     ↓
MySQL Database
     ↓
SQL Analysis
     ↓
Power BI
     ↓
Interactive Dashboard
     ↓
Report & Presentation


# 1 Data Loading

The dataset was first imported into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("customer_data.csv")

df.head()
```

Initial inspection was performed using functions such as:

```python
df.shape
df.info()
df.describe()
df.isnull().sum()
df.duplicated().sum()
```

This helped understand the structure and quality of the dataset.

---

# 2️ Exploratory Data Analysis (EDA)

EDA was performed to identify patterns, relationships, distributions, and potential issues in the data.

Key activities included:

* Understanding numerical and categorical variables
* Checking data distributions
* Identifying missing values
* Detecting duplicate records
* Identifying potential outliers
* Analyzing customer purchase behavior
* Studying relationships between different variables
* Creating charts and visualizations

---

# 3️ Data Cleaning

The dataset was cleaned and prepared for analysis.

Major data-cleaning activities included:

* Handling missing values
* Removing duplicate records
* Correcting data types
* Standardizing categorical values
* Handling inconsistent data
* Creating new analytical columns
* Categorizing customers based on purchasing behavior

Example:

```python
df.drop_duplicates(inplace=True)

df["purchase_date"] = pd.to_datetime(df["purchase_date"])
```

---

# 4️ MySQL & SQL Analysis

After cleaning, the data was loaded into a **MySQL database** for structured storage and SQL-based analysis.

SQL techniques used include:

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `HAVING`
* `JOIN`
* Aggregate functions
* `CASE`
* `CTE`
* Conditional calculations

### Customer Segmentation Example

Customers were categorized based on their previous purchase behavior.

```sql
CASE
    WHEN previous_purchase = 1 THEN 'New'
    WHEN previous_purchase BETWEEN 2 AND 10 THEN 'Returning'
    ELSE 'Loyal'
END AS customer_segment
```

This helped identify different customer groups and compare their behavior.

---

# 5️ Power BI Dashboard

The cleaned and analyzed data was connected to **Power BI** to create an interactive dashboard.

### Dashboard Includes

* Total Customers
* Customer Segments
* Purchase Behavior
* Purchase Frequency
* Customer Distribution
* Spending Analysis
* Key Performance Indicators (KPIs)
* Interactive filters and slicers
* Charts and visualizations

The dashboard allows users to interact with the data and explore customer behavior from different perspectives.

---

# Dashboard

The Power BI dashboard provides a visual summary of the analysis.

> Add your dashboard screenshot here:

```markdown
![Customer Behavior Dashboard](images/dashboard.png)
```

The dashboard is designed to provide a quick understanding of important customer behavior trends and patterns.

---

#  Results & Key Insights

The analysis helped identify meaningful patterns in customer behavior, including:

* Distribution of customers across different segments
* Differences between new, returning, and loyal customers
* Customer purchasing frequency
* Spending and purchasing patterns
* Important behavioral trends
* Potential areas for improving customer retention

These insights can help businesses better understand their customers and develop more targeted strategies for **customer retention, engagement, and marketing**.



# 📁 Project Structure

```text
Customer-Behavior-Analysis/
│
├── dataset/
│   └── customer_data.csv
│
├── notebooks/
│   └── customer_analysis.ipynb
│
├── sql/
│   └── customer_analysis.sql
│
├── dashboard/
│   └── customer_behavior_dashboard.pbix
│
├── presentation/
│   └── project_presentation.pdf
│
└── README.md
```
# 💡 Business Value

This project demonstrates how different data analytics tools can be combined to solve a real-world business problem:

**Python** → Clean and explore data
**MySQL** → Store and analyze structured data
**Power BI** → Communicate insights through dashboards
**Gamma** → Present findings professionally

The project demonstrates an end-to-end **Data Analyst workflow** from raw data to actionable business insights.

---

# 🚀 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Python
* Pandas
* SQL
* MySQL
* Customer Segmentation
* Data Visualization
* Power BI
* Dashboard Development
* Business Intelligence
* Data Storytelling
* Report & Presentation Development

---

# 👤 Author

**Harsh Gautam**

Aspiring Data Analyst | Python | SQL | MySQL | Power BI | Data Analytics

---

⭐ If you found this project useful, consider giving the repository a star!
