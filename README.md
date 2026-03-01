# 🛡️ Credit Card Fraud Detection & Customer Risk Profiling

## 📌 Project Overview
This end-to-end data analytics project focuses on identifying fraudulent credit card transactions and proactively classifying customer risk levels. Analyzing a large-scale dataset of exactly **500K transactions**, I developed an interactive Power BI dashboard that combines advanced DAX calculations with an adapted RFM (Recency, Frequency, Monetary) framework to transition from simple anomaly detection to comprehensive behavioral profiling. 

The analysis reveals critical insights into a **$48.0K Total Fraud Loss** against a **$21.2M Total Revenue**, providing stakeholders with a clear view of business impact.

## 🛠️ Tools & Technologies
* **Data Processing:** Python (Pandas) / SQL (Data cleaning, handling missing values, and logical transformations).
* **Data Visualization:** Power BI (Interactive reporting, Decomposition Trees, Drill-through capabilities, Custom Tooltips).
* **Data Modeling:** Advanced DAX (Context transition, dynamic segmentation for risk profiling).

## 🧠 Core Business Logic: The Risk Profile Matrix
A distinguishing feature of this project is the **Customer Risk Profile**, which goes beyond standard transaction-level fraud detection. I engineered a dynamic segmentation model using DAX:
1.  **RFM Segmentation:** Customers are categorized based on their purchasing habits (e.g., *New Customers*, *Champions*).
2.  **Fraud Integration:** The model calculates a `Fraud Count` for each individual user.
3.  **Risk Assignment:** Any user with confirmed fraudulent activity is immediately flagged as a **🔴 FRAUDSTER**. For example, a user might be identified as a **"FRAUDSTER (New Customers)"**, highlighting cases where bad actors create new accounts specifically for malicious activities.

---

## 📊 Dashboard Architecture & Features

### 1. Page 1: Overview Dashboard
Designed for high-level management to monitor overall business health and fraud impact.
* **Executive KPIs:** Real-time tracking of 500K Total Transactions, 568 Fraud Count, and a 0.11% Fraud Rate.
* **Trend Analysis:** Dual-axis charts comparing *Transaction Volume & Fraud Trend* (June - October 2019) and *Fraud Volume & Loss Trend*.
* **High-Risk Categories:** A bar chart clearly identifying **Department Stores** and **Grocery Stores/Supermarkets** as the top targets for fraud attacks.

<img width="999" height="816" alt="image" src="https://github.com/user-attachments/assets/fe049050-921f-4848-8eb7-9fe9f03b1d7a" />

### 2. Page 2: Analyst Investigation
Designed for fraud analysts to drill down into anomalies and explore specific attack vectors.
* **Decomposition Tree:** A root-cause analysis tool answering *"What drives Fraud Attacks?"* by breaking down the 568 fraud cases by **Use chip** (Chip vs Swipe), **Trans size** (Small/Medium/Large), and **Merchant Category**.
* **Temporal Heatmap:** A detailed matrix visualizing fraud frequency by **Day of week** and Hour of day, allowing analysts to spot specific time-based attack patterns.
* **Demographic Segmentation:** Visualizing total transactions across Age Groups (e.g., 25-45, 45-65) to identify vulnerable demographics.

<img width="996" height="815" alt="image" src="https://github.com/user-attachments/assets/0de98034-b3cf-4f76-a8b4-ae68db972257" />

### 3. Page 3: Analyst Detail (Drill-through Profile)
An investigative tool triggered by right-clicking a specific user to view their detailed dossier.
* **Dynamic Client Identification:** Displays specific user details (e.g., **Client ID: 201**).
* **Risk Status & Impact:** Prominently displays the `Customer Risk Profile` (e.g., *FRAUDSTER (New Customers)*) alongside their specific Fraud Loss Amount ($383.5) and individual Fraud Rate (4.96%).
* **Transaction History Table:** A granular ledger listing exact dates, amounts, transaction types (Chip/Online), and highlighting confirmed fraud hits (`target = 1`) for forensic review.

<img width="974" height="562" alt="image" src="https://github.com/user-attachments/assets/18fc53a1-ac0c-4d94-bb6e-525f30d113d9" />

---

## 💡 Key Insights & Actionable Recommendations
Based on the dashboard analysis:
* **Category Vulnerability:** **Department Stores** are overwhelmingly the highest-risk merchant category, experiencing more than double the fraud incidents (118 cases) compared to the second-highest category. Security rules should be tightened for this specific MCC.
* **Transaction Medium:** Fraudsters are actively bypassing physical security, with a significant portion of fraud originating from **Chip Transactions** rather than Swipe or Online methods.
* **Temporal Patterns:** The heatmap analysis indicates specific clusters of fraudulent activity concentrated on certain days (e.g., Tuesdays and Fridays) and specific afternoon/evening hours, suggesting coordinated attacks rather than random occurrences.

---
*Created by **Lê Hà Chức** - Aspiring Data Analyst | Contact: [https://www.linkedin.com/in/lehachuc/]*
