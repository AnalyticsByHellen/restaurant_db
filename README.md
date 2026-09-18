# # 🍔 Restaurant Sales SQL Analysis

## 📌 Project Overview

This project analyzes restaurant order data using **MySQL** to understand customer ordering patterns, menu performance, revenue, and sales trends.

The analysis uses SQL to answer real business questions and demonstrate practical skills in:

* Data exploration
* Data quality checks
* SQL JOINs
* Aggregations
* `GROUP BY`
* Subqueries
* Common Table Expressions (CTEs)
* Window functions and ranking
* Date and time analysis
* Revenue analysis

---

## 📊 Dataset

The project uses two main tables:

### `menu_items`

Contains information about the restaurant's menu.

| Column         | Description                  |
| -------------- | ---------------------------- |
| `menu_item_id` | Unique ID for each menu item |
| `item_name`    | Name of the menu item        |
| `category`     | Food category                |
| `price`        | Menu item price              |

### `order_details`

Contains information about items included in customer orders.

| Column             | Description                       |
| ------------------ | --------------------------------- |
| `order_details_id` | Unique ID for each order detail   |
| `order_id`         | ID identifying the customer order |
| `order_date`       | Date the order was placed         |
| `order_time`       | Time the order was placed         |
| `item_id`          | ID of the menu item ordered       |

The two tables are connected through:

```sql
order_details.item_id = menu_items.menu_item_id
```

---

# 🎯 Business Questions

The analysis answers questions across several areas.

## 1. Data Quality

Examples:

* Are there duplicate `order_details_id` values?
* Are there duplicate `order_id + item_id` combinations?
* Are there missing `item_id` values?
* Are there menu items that were never ordered?
* Are all `item_id` values connected to a menu item?

---

## 2. Order Analysis

Examples:

* How many unique orders were placed?
* How many items were ordered in total?
* What is the average number of items per order?
* Which order contains the most items?
* Which orders contain 5 or more items?

---

## 3. Menu Analysis

Examples:

* How many menu items are available?
* How many food categories are there?
* What is the average menu price?
* Which category has the highest average price?
* Which menu items cost more than the overall average price?

---

## 4. Menu Performance

Examples:

* Which menu items are ordered most frequently?
* Which menu items generate the most revenue?
* Which menu items were never ordered?
* Which category has the highest number of items ordered?
* Which category generates the most revenue?

---

## 5. Revenue Analysis

Estimated revenue is calculated using:

```text
Revenue = Number of times an item was ordered × Item Price
```

The analysis investigates:

* Total revenue
* Average revenue per order
* Revenue by menu item
* Revenue by category
* Revenue contribution by menu item
* Highest and lowest revenue-generating items
* Category revenue rankings

---

## 6. Date & Time Analysis

The project also examines when customers place orders.

Questions include:

* How many orders are placed each day?
* Which day generates the most revenue?
* How many orders are placed each month?
* Which month generates the most revenue?
* Which day of the week is busiest?
* Which hour receives the most orders?
* Which hour generates the most revenue?

---

# 🛠️ SQL Skills Demonstrated

### Basic SQL

```sql
SELECT
FROM
WHERE
ORDER BY
```

### Aggregation

```sql
COUNT()
SUM()
AVG()
MIN()
MAX()
```

### Grouping

```sql
GROUP BY
```

### Joining Tables

```sql
JOIN
LEFT JOIN
```

### Conditional Logic

```sql
CASE
```

### Subqueries

Used when a query needs the result of another query for comparison or filtering.

### Common Table Expressions

```sql
WITH ...
```

CTEs are used to break more complex analysis into smaller, easier-to-understand steps.

### Window Functions

```sql
RANK()
DENSE_RANK()
NTILE()
```

Used for ranking menu items and categories.

### Date & Time Functions

```sql
YEAR()
MONTH()
MONTHNAME()
DAYNAME()
HOUR()
DATE_FORMAT()
```

---

# 📁 Project Structure

```text
restaurant-sql-analysis/
│
├── README.md
│
├── data/
│   ├── menu_items.csv
│   └── order_details.csv
│
└── sql/
    ├── 01_data_quality.sql
    ├── 02_order_analysis.sql
    ├── 03_menu_analysis.sql
    ├── 04_menu_performance.sql
    ├── 05_revenue_analysis.sql
    ├── 06_date_time_analysis.sql
    └── 07_ranking_analysis.sql
```

---

# 📈 Key Analysis Areas

The project progresses from simple questions to more advanced analysis:

```text
Data Quality
     ↓
Order Exploration
     ↓
Menu Exploration
     ↓
Menu Performance
     ↓
Revenue Analysis
     ↓
Date & Time Analysis
     ↓
Ranking & Advanced SQL
```

This progression demonstrates how SQL can be used to move from **understanding the data** to answering **business questions**.

---

# 💡 Business Value

The analysis can help a restaurant understand:

* Which menu items customers order most often
* Which products generate the most revenue
* Which categories perform strongly
* When customer demand is highest
* Which menu items may need further investigation
* How revenue is distributed across products and categories

These insights could support decisions around menu planning, promotions, pricing, and operational planning.

---

# 💻 Tools Used

* **MySQL**
* **MySQL Workbench**
* **GitHub**
* SQL

---

# 👩🏽‍💻 Project Purpose

This project was created as part of my **SQL data analytics portfolio** to practice turning business questions into SQL queries and developing practical data analysis skills.

The focus is not only on writing SQL queries, but also on understanding:

> **What question am I answering?**

> **Which table contains the information I need?**

> **Do I need a JOIN?**

> **What should I calculate first?**

> **Do I need a GROUP BY, subquery, CTE, or window function?**

This approach helps connect SQL syntax with real-world business analysis.
