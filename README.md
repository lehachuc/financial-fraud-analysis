# 🛡️ Fraud Detection & Customer Risk Analysis

## 📌 Project Overview
This project focuses on identifying fraudulent transactions and classifying customer risk profiles using a dataset of over 500,000 transactions. By leveraging **Power BI, SQL, and Python**, this dashboard provides actionable insights into fraud patterns, monetary impact, and customer behavior.

## 🛠️ Tools & Technologies Used
* **Data Processing & ETL:** Python (Pandas), SQL
* **Data Visualization:** Power BI
* **Data Modeling & Calculations:** Advanced DAX
* **Analytical Framework:** Custom RFM (Recency, Frequency, Monetary) Model

## 🧠 Business Logic: The Risk Profile Matrix
A core feature of this project is the **Customer Risk Profile**. Instead of simple metrics, I engineered a dynamic segmentation model:
1. **RFM Segmentation:** Grouping customers based on their transaction history (e.g., *Champions, New Customers, At Risk VIP*).
2. **Fraud Integration:** Combining RFM segments with a calculated `Fraud Count` using DAX.
3. **Outcome:** Any user with 1+ fraudulent transaction is immediately flagged as **🔴 FRAUDSTER**, revealing cases where VIP customers might be masking malicious activities.

## 📊 Dashboard Previews

### 1. Executive Overview
<img width="999" height="816" alt="image" src="https://github.com/user-attachments/assets/fe049050-921f-4848-8eb7-9fe9f03b1d7a" />
> Highlights key metrics including Total Fraud Loss, Transaction Volumes, and Geographical Fraud Distribution.

### 2. Analyst Investigation & RFM
<img width="996" height="815" alt="image" src="https://github.com/user-attachments/assets/0de98034-b3cf-4f76-a8b4-ae68db972257" />
> Deep dive into anomaly detection using Decomposition Trees and interactive Slicers by State, Age Group, and Time.

### 3. User Profile Detail (Drill-through)
<img width="974" height="562" alt="image" src="https://github.com/user-attachments/assets/18fc53a1-ac0c-4d94-bb6e-525f30d113d9" />
> A granular view of individual customer behavior, risk status, and complete transaction history.

## 💡 Key Insights & Recommendations
* *(Tự điền 1): Ngành hàng XYZ chiếm tỉ lệ gian lận cao nhất...*
* *(Tự điền 2): Nhóm tuổi ABC có xu hướng bị lừa đảo qua thẻ tín dụng...*
* *(Tự điền 3): Phân khúc khách hàng VIP bị trà trộn gian lận chiếm X%...*

---
*Created by [Tên của bạn] - Aspiring Data Analyst*
