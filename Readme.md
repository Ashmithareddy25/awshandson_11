# 🧾 AWS Athena Query Analysis – Amazon Sale Report

 
---

## 📘 Overview
This project demonstrates how **Amazon Athena** can be used to analyze e-commerce sales data directly from Amazon S3.  
Using **AWS Glue**, the dataset was crawled and structured into an Athena table, allowing SQL queries to be executed without the need for provisioning servers.  

The queries explore sales patterns, regional loss “hotspots”, discount effects, product profitability rankings, and monthly growth trends.

---

## ⚙️ Workflow Summary
1. **Created S3 Buckets** – Uploaded `Amazon Sale Report.csv` into a raw data folder.  
2. **Configured IAM Role** – Provided S3 and Glue access to Athena and the crawler.  
3. **Created Glue Crawler** – Generated table schema in `output_db` database.  
4. **Used Athena Editor** – Executed all five analytical queries

---

## 🧩 Queries, Explanations & Sample Outputs

---

### **1️⃣ Cumulative Sales Over Time for a Specific Year**
```sql
SELECT 
    date_parse("Date", '%m-%d-%y') AS order_date,
    SUM(CAST(Amount AS double)) OVER (
        ORDER BY date_parse("Date", '%m-%d-%y')
        ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
    ) AS cumulative_sales
FROM "output_db"."raw"
WHERE year(date_parse("Date", '%m-%d-%y')) = 2022
ORDER BY order_date
LIMIT 10;
```


