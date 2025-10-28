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


![Query1](https://github.com/user-attachments/assets/5fbf087a-6061-43db-87d4-53ccfb34c284)

![Query](https://github.com/user-attachments/assets/7149816e-5090-4292-bb91-ecaaf6725ab4)
![Query2_output](https://github.com/user-attachments/assets/7440da80-81b8-4d5a-8a44-a6407ec8655b)
![Query3](https://github.com/user-attachments/assets/f311982d-9c51-4f20-860e-8cde9e5b9387)
![Query3_Output](https://github.com/user-attachments/assets/5122c09f-2025-4fbc-b672-5715094e7abe)

![Query4](https://github.com/user-attachments/assets/790cc831-18a1-443f-b3c2-0a95d919c9ee)
![Query4_output](https://github.com/user-attachments/assets/131f1850-297a-462a-b9b1-7036eb10a542)

![Query5](https://github.com/user-attachments/assets/51a56493-59f4-46ce-ac47-3399c8f6eab9)
![Query5_output](https://github.com/user-attachments/assets/913e9734-3255-4e47-a036-0c306478bbe8)

![Cloudwatch](https://github.com/user-attachments/assets/cf3ee57d-68a6-45f2-b8c8-28dd691dc1af)

![AWS Glue](https://github.com/user-attachments/assets/20b925c3-d21f-4673-a804-91b0fe057984)
![S3](https://github.com/user-attachments/assets/6ec4da25-49d5-46b9-a71b-500563ca1258)

![IAM](https://github.com/user-attachments/assets/0977982c-1195-46bd-afd9-164eeb500250)
