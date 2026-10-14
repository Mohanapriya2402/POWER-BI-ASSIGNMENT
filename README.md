# 📊 Power BI – Data Transformation & Data Modeling

## 📌 Project Overview

This project focuses on preparing, transforming, cleansing, and modeling an E-commerce sales dataset using Microsoft Power BI and Power Query Editor.

The project involves working with three related datasets: List of Orders, Order Details, and Sales Target. Various data preparation techniques are applied to improve data quality, combine related information, perform aggregations, and establish relationships between tables.

The goal is to create a structured and reliable data model that supports sales analysis, profitability analysis, and sales target evaluation.

## 🎯 Project Objectives

- Import multiple datasets into Power BI.
- Clean and transform data using Power Query Editor.
- Apply appropriate data types and text formatting.
- Create custom and conditional columns.
- Merge related tables using Order ID.
- Handle missing values and duplicate records.
- Sort and filter data for analysis.
- Perform grouping and aggregation.
- Establish and manage relationships between tables.
- Prepare data for meaningful business analysis.

## 📂 Dataset Description

This project uses three datasets representing order information, product details, and sales targets.

### 1. List of Orders

| Column | Description |
|---|---|
| Order ID | Unique identifier for an order |
| Order Date | Date on which the order was placed |
| Customer Name | Name of the customer |
| City | Customer's city |
| State | Customer's state |
| Category | Product category |
| Amount | Order amount |
| Profit | Profit earned or loss incurred |

### 2. Order Details

| Column | Description |
|---|---|
| Order ID | Identifier linking order records |
| Category | Product category |
| Sub-Category | Product sub-category |
| Quantity | Quantity ordered |
| Amount | Amount associated with the order details |
| Profit | Profit associated with the order details |

### 3. Sales Target

| Column | Description |
|---|---|
| Category | Product category |
| Month of Order Date | Month associated with the sales target |
| Target | Target amount for the corresponding category and month |

## 🛠️ Tools and Technologies

- **Microsoft Power BI** – Data preparation and modeling
- **Power Query Editor** – Data cleaning and transformation
- **Merge Queries** – Combining related datasets
- **Conditional Columns** – Categorizing profit performance
- **Group By** – Data aggregation and summarization
- **Manage Relationships** – Defining relationships between tables

## 🔄 Tasks Performed

### 1. Data Import

- Imported `List of Orders.csv` into Power BI.
- Opened Power Query Editor using the Transform Data option.
- Imported `Order Details.csv` and `Sales Target.csv`.
- Prepared the three datasets for transformation.

### 2. Row Limiting and Data Types

- Restricted the List of Orders table to the first 500 rows.
- Changed the Order Date column to the Date data type.
- Converted the Amount and Target columns to Fixed Decimal Number where appropriate.

### 3. Text Formatting

Standardized customer names using Proper Case in Power Query to maintain consistent capitalization.

### 4. Column Creation

**Location**

Merged the City and State columns into a new column named `Location`.

Example:

`Chennai, Tamil Nadu`

**Profit Margin**

Created a custom column to calculate profit margin as a percentage.

Formula:

```text
Profit Margin = Profit / Amount
```

The resulting column was formatted as a percentage. Records with a zero or missing Amount require appropriate handling to avoid invalid calculations.

### 5. Conditional Column – Profit Status

Created a conditional column named `Profit Status` using the following rules:

| Condition | Profit Status |
|---|---|
| Profit < 0 | Loss |
| Profit = 0 | Break-Even |
| Profit > 0 | Profit |

This classification helps distinguish profitable orders from loss-making and break-even orders.

### 6. Merging Data

Merged the List of Orders and Order Details tables using `Order ID`.

The merged output was named **Orders Data**.

This process combines relevant order-level and order-detail information for further analysis.

### 7. Handling Missing Values and Duplicates

- Identified missing values across all three datasets.
- Evaluated appropriate strategies for handling missing information.
- Replaced missing values only when a reliable replacement was available.
- Removed records only when justified by data quality or business requirements.
- Retained null values when information could not be reliably inferred.
- Checked duplicate records and applied suitable handling strategies based on business logic.

### 8. Sorting and Filtering

- Sorted the Orders Data table by Order Date in descending order.
- Applied filters to examine orders from a specific state, such as Tamil Nadu.

These operations help focus the analysis on recent orders and selected geographic regions.

### 9. Grouping and Aggregation

Used duplicated queries to perform the required aggregations.

**Order Details Aggregation**

- Count of Order ID
- Average Profit by Category
- Total Amount by Sub-Category

**Sales Target Aggregation**

- Duplicated the Sales Target table.
- Grouped the data by Month of Order Date.
- Calculated the total Target for each month.

These summaries support category-level, sub-category-level, and monthly analysis.

### 10. Data Modeling

Established and reviewed relationships between the datasets using Manage Relationships.

The intended relationships were:

- List of Orders ↔ Order Details using `Order ID`
- Order Details ↔ Sales Target using `Category`

Checked that the relationships were active and correctly defined.

Relationship cardinality and filter direction should be selected based on the uniqueness of the key columns and the intended analytical requirements.

## 📈 Key Analysis Opportunities

The prepared data model can support analysis of:

- Sales and order performance
- Profit and loss distribution
- Profit margin across orders
- Category-wise average profit
- Sub-category-wise sales amounts
- Monthly sales targets
- State-wise order distribution
- Sales performance against targets

## 💡 Skills Demonstrated

- Data Import and Preparation
- Data Cleaning and Quality Checks
- Data Transformation with Power Query
- Data Type Conversion
- Text Standardization
- Custom Column Creation
- Conditional Logic
- Query Merging
- Missing Value Handling
- Duplicate Detection
- Sorting and Filtering
- Grouping and Aggregation
- Data Modeling and Relationships

## 📁 Project Files

- `Data Transformation & Data Modeling Final.pbix` – Power BI project file containing the report, transformed queries, and data model.

## 🎓 Learning Outcomes

Through this project, I developed practical experience in preparing and transforming E-commerce sales data using Power BI.

I learned how to combine related datasets, create calculated columns, handle data quality issues, summarize information, and establish relationships between tables.

This project strengthened my understanding of the data preparation and modeling stages that are essential for reliable business intelligence and reporting.

## 👩‍💻 About Me

I am an **Aspiring Data Analyst** building my technical skills through practical projects and continuous learning.

My current learning journey includes:

**Microsoft Excel | SQL | Python | Power BI | Data Analytics**

This project is part of my growing Data Analyst portfolio, showcasing my hands-on learning and progress in data analytics.
