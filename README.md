# 🛡️ Credit Card Fraud Detection & Customer Risk Profiling

## 📌 Project Overview
This end-to-end data analytics project focuses on identifying fraudulent credit card transactions and proactively classifying customer risk levels. [cite_start]Analyzing a large-scale dataset of exactly **500K transactions**[cite: 10, 11], I developed an interactive Power BI dashboard that combines advanced DAX calculations with an adapted RFM (Recency, Frequency, Monetary) framework to transition from simple anomaly detection to comprehensive behavioral profiling. 

[cite_start]The analysis reveals critical insights into a **$48.0K Total Fraud Loss** against a **$21.2M Total Revenue**[cite: 13, 15, 30, 33], providing stakeholders with a clear view of business impact.

## 🛠️ Tools & Technologies
* **Data Processing:** Python (Pandas) / SQL (Data cleaning, handling missing values, and logical transformations).
* **Data Visualization:** Power BI (Interactive reporting, Decomposition Trees, Drill-through capabilities, Custom Tooltips).
* **Data Modeling:** Advanced DAX (Context transition, dynamic segmentation for risk profiling).

## 🧠 Core Business Logic: The Risk Profile Matrix
A distinguishing feature of this project is the **Customer Risk Profile**, which goes beyond standard transaction-level fraud detection. I engineered a dynamic segmentation model using DAX:
1.  **RFM Segmentation:** Customers are categorized based on their purchasing habits (e.g., *New Customers*, *Champions*).
2.  [cite_start]**Fraud Integration:** The model calculates a `Fraud Count` [cite: 116] for each individual user.
3.  **Risk Assignment:** Any user with confirmed fraudulent activity is immediately flagged as a **🔴 FRAUDSTER**. [cite_start]For example, a user might be identified as a **"FRAUDSTER (New Customers)"**, highlighting cases where bad actors create new accounts specifically for malicious activities.

---

## 📊 Dashboard Architecture & Features

### 1. Page 1: Overview Dashboard
[cite_start]Designed for high-level management to monitor overall business health and fraud impact[cite: 1].
* [cite_start]**Executive KPIs:** Real-time tracking of 500K Total Transactions, 568 Fraud Count, and a 0.11% Fraud Rate[cite: 10, 11, 12, 14, 32, 34].
* [cite_start]**Trend Analysis:** Dual-axis charts comparing *Transaction Volume & Fraud Trend* (June - October 2019) and *Fraud Volume & Loss Trend*[cite: 16, 21, 24, 77].
* [cite_start]**High-Risk Categories:** A bar chart clearly identifying **Department Stores** and **Grocery Stores/Supermarkets** as the top targets for fraud attacks[cite: 35, 36, 38].

<img width="999" height="816" alt="image" src="https://github.com/user-attachments/assets/fe049050-921f-4848-8eb7-9fe9f03b1d7a" />

### 2. Page 2: Analyst Investigation
[cite_start]Designed for fraud analysts to drill down into anomalies and explore specific attack vectors[cite: 85].
* [cite_start]**Decomposition Tree:** A root-cause analysis tool answering *"What drives Fraud Attacks?"* by breaking down the 568 fraud cases by **Use chip** (Chip vs Swipe), **Trans size** (Small/Medium/Large), and **Merchant Category**[cite: 100, 101, 102, 103, 110, 119].
* [cite_start]**Temporal Heatmap:** A detailed matrix visualizing fraud frequency by **Day of week** and Hour of day, allowing analysts to spot specific time-based attack patterns[cite: 98].
* [cite_start]**Demographic Segmentation:** Visualizing total transactions across Age Groups (e.g., 25-45, 45-65) to identify vulnerable demographics[cite: 130, 131, 145].

<img width="996" height="815" alt="image" src="https://github.com/user-attachments/assets/0de98034-b3cf-4f76-a8b4-ae68db972257" />

### 3. Page 3: Analyst Detail (Drill-through Profile)
[cite_start]An investigative tool triggered by right-clicking a specific user to view their detailed dossier[cite: 9, 246].
* [cite_start]**Dynamic Client Identification:** Displays specific user details (e.g., **Client ID: 201**)[cite: 161, 162].
* [cite_start]**Risk Status & Impact:** Prominently displays the `Customer Risk Profile` (e.g., *FRAUDSTER (New Customers)*)  [cite_start]alongside their specific Fraud Loss Amount ($383.5) and individual Fraud Rate (4.96%)[cite: 154, 157].
* [cite_start]**Transaction History Table:** A granular ledger listing exact dates, amounts, transaction types (Chip/Online), and highlighting confirmed fraud hits (`target = 1`) for forensic review[cite: 166, 167, 168, 170, 171].

<img width="974" height="562" alt="image" src="https://github.com/user-attachments/assets/18fc53a1-ac0c-4d94-bb6e-525f30d113d9" />

---

## 💡 Key Insights & Actionable Recommendations
Based on the dashboard analysis:
* [cite_start]**Category Vulnerability:** **Department Stores** are overwhelmingly the highest-risk merchant category, experiencing more than double the fraud incidents (118 cases) compared to the second-highest category[cite: 36, 38, 78, 79]. [cite_start]Security rules should be tightened for this specific MCC[cite: 248].
* [cite_start]**Transaction Medium:** Fraudsters are actively bypassing physical security, with a significant portion of fraud originating from **Chip Transactions** rather than Swipe or Online methods[cite: 110, 119, 173].
* [cite_start]**Temporal Patterns:** The heatmap analysis indicates specific clusters of fraudulent activity concentrated on certain days (e.g., Tuesdays and Fridays) and specific afternoon/evening hours[cite: 98], suggesting coordinated attacks rather than random occurrences.

---
*Created by **Lê Hà Chức** - Aspiring Data Analyst | Contact: [https://www.linkedin.com/in/lehachuc/]*
