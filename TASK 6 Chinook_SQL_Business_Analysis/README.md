# Chinook SQL Business Analysis

This project explores business insights from the [Chinook Music Store Database](https://github.com/lerocha/chinook-database) using advanced SQL in PostgreSQL. It was completed as part of my **Data Analyst Internship Task 6 at Elevvo**.

## Tools Used

- **PostgreSQL** with **pgAdmin**
- SQL: Joins, Window Functions, Aggregations, CTEs
- **Chinook Sample Database**
- **RFM Segmentation** for Customer Analysis

---

## Key Business Questions Answered

- **Top-Selling Tracks**
- **Revenue by Country and City**
- **Monthly Revenue & Order Trends**
- **Top 5 Customers by Spending**
- **Revenue by Genre and Artist**
- **RFM (Recency, Frequency, Monetary) Segmentation**

---

## Project Structure

| File                     | Description                              |
| ------------------------ | ---------------------------------------- |
| `chinook_analysis.sql`   | Complete business analysis + RFM queries |
| `Chinook_PostgreSql.sql` | Database creation and insertion script   |
| `README.md`              | Project overview and summary             |

---

## Sample Query: Top 5 Customers by Spending

```sql
SELECT
  c.customer_id,
  c.first_name || ' ' || c.last_name AS customer_name,
  SUM(i.total) AS total_spent
FROM customer c
JOIN invoice i ON c.customer_id = i.customer_id
GROUP BY c.customer_id, customer_name
ORDER BY total_spent DESC
LIMIT 5;
```

---

##  About Me

**Name:** Abdur Rahman\
**Role:** Data Analyst Intern | Computer Science Undergraduate\
**Focus:** Data Analytics • Business Intelligence • SQL • Python • Power BI\
**University:** Air University, Islamabad

**GitHub:** [github.com/AbdurRahman-ML](https://github.com/AbdurRahman-ML)

---

##  Connect With Me

-  **Email:** [abdurrahman82733@gmail.com](mailto:abdurrahman82733@gmail.com)
-  **LinkedIn:** [linkedin.com/in/abdur-rahmanml](https://www.linkedin.com/in/abdur-rahmanml/)
