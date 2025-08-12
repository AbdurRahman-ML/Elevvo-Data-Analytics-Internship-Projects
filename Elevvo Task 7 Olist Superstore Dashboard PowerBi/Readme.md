#  E-Commerce Analytics Project (Olist Brazilian E-Commerce)

##  Project Overview

This project analyzes a real-world Brazilian e-commerce dataset to uncover business insights and visualize them through interactive dashboards.

**Workflow:**
1. Data Cleaning & Preparation (Python)
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Data Modeling for Power BI
5. Interactive Dashboard Creation

##  Dataset

The dataset contains multiple relational tables covering orders, customers, products, deliveries, and payments.

### Key Tables

- **Orders** – Order-level details including order dates, status, and customer IDs.
- **Customers** – Customer demographics and location data.
- **Product Sales** – Pricing, freight, and product category information.
- **Delivery Performance** – Shipping timelines and delays.
- **Payment Analysis** – Payment methods, installments, and amounts.
- **RFM Segmentation** – Recency, Frequency, and Monetary metrics for customer segmentation.

##  Python Workflow (EDA & Cleaning)

### 1. Data Import & Inspection

```python
import pandas as pd
orders = pd.read_csv("orders.csv")
customers = pd.read_csv("customers.csv")
product_sales = pd.read_csv("product_sales.csv")
```

### 2. Data Cleaning

- Removed duplicates
- Handled missing values in product dimensions and reviews
- Converted date columns to datetime format

### 3. Exploratory Data Analysis (EDA)

- Order distribution over time
- Sales by product category
- Customer distribution by state
- Review score distribution

### 4. Feature Engineering

- Extracted year, month, and day from order dates
- Calculated delivery delays & created an on-time delivery flag
- Built RFM Segmentation (Recency, Frequency, Monetary)

### 5. Exporting Cleaned Data for Power BI

```python
orders.to_csv("clean_orders.csv", index=False)
customers.to_csv("clean_customers.csv", index=False)
product_sales.to_csv("clean_product_sales.csv", index=False)
```

##  Power BI Data Modeling

### Data Model Structure

**Fact Tables:**
- product_sales
- delivery_performance
- payment_analysis
- rfm_segmentation

**Dimension Tables:**
- dim_orders
- dim_customers

### Relationships

- dim_orders.order_id → product_sales.order_id
- dim_customers.customer_id → dim_orders.customer_id
- dim_orders.order_id → delivery_performance.order_id
- dim_orders.order_id → payment_analysis.order_id

##  Power BI Measures (DAX)

```dax
-- Total Orders
Total Orders = DISTINCTCOUNT(dim_orders[order_id])

-- Total Revenue
Total Revenue = SUM(product_sales[price])

-- Average Order Value
AOV = DIVIDE([Total Revenue], [Total Orders])

-- On-Time Delivery Rate
On-Time Rate =
VAR OnTime = CALCULATE(
    COUNTROWS(delivery_performance),
    delivery_performance[on_time] = "Yes"
)
RETURN DIVIDE(OnTime, COUNTROWS(delivery_performance))

-- RFM - Average Monetary Value
Avg Monetary = AVERAGE(rfm_segmentation[Monetary])
```

##  Dashboard Pages

### 1. Executive Summary
- Total Orders
- Total Revenue
- Average Order Value
- On-Time Delivery Rate

### 2. Product Performance
- Top-selling categories
- Top products by revenue
- Average review score per category

### 3. Customer Insights
- Customers by segment
- Repeat purchase rate
- RFM segmentation distribution

### 4. Delivery Insights
- Delivery delays over time
- On-time delivery rate by seller

##  Key Insights

- **Steady Growth**: Revenue has grown steadily, with a peak in late 2017.
- **Top Categories**: A few categories drive the majority of revenue.
- **Customer Concentration**: São Paulo and Rio de Janeiro dominate orders.
- **Delivery Impact**: On-time deliveries correlate with higher review scores.
- **High-Value Customers**: RFM analysis identifies profitable customer segments.

##  Tools & Technologies

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **Power BI** — Data Modeling, DAX, Interactive Visuals
- **GitHub** — Version Control & Documentation

##  About Me

**Name:** Abdur Rahman\
**Role:** Data Analyst Intern | Computer Science Undergraduate\
**Focus:** Data Analytics • Business Intelligence • SQL • Python • Power BI\
**University:** Air University, Islamabad

**GitHub:** [github.com/AbdurRahman-ML](https://github.com/AbdurRahman-ML)

---
