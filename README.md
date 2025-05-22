# 🧠 Marketing Campaign Customer Segmentation (Power BI Project)

## 📊 Overview

This Power BI project analyzes customer demographic and transactional data from a Portuguese marketing campaign dataset. The analysis focuses on customer segmentation using **RFM (Recency, Frequency, Monetary) scoring**, behavioral patterns by age, and channel/product preferences to generate data-driven marketing insights.

---

## 📁 Dataset

- Source: `marketing_campaign.csv` (tab-delimited)
- Rows: 2,240+
- Fields: Demographics, transactions, marketing responses

---

## 🧹 Data Preparation (Power Query M)

Key transformations included:

- Replacing invalid or missing income values
- Calculating **Age** and categorizing into `Age_Group`
- Standardizing categorical fields (e.g., `Education`, `Marital_Status`)
- Deriving total **Frequency** and **Monetary** from various purchase columns
- Generating quantile-based **RFM scores (1–5)**
- Combining scores into `RFM_Segment`, `RFM_Score`, and categorized `RFM_Category`

---

## 📈 Dashboard Pages

### 📌 Page 1: Customer Overview (KPI Cards)
- **Total Customers**
- **Average Income**
- **Average Age**
- **Average Recency**
- **Total Spending**
- 📊 Bar chart: Customers by Education and Marital Status

---

### 🔎 Page 2: RFM Segmentation
- Table: Recency, Frequency, Monetary scores per customer
- Bar chart: Customers by `RFM_Segment`
- Treemap: `RFM_Segment` grouped by `RFM_Category`

---

### 💳 Page 3: Spending Behavior by Age
- Area chart: Average Frequency and Monetary vs Age Group
- Bar chart: Average Spending per Age Group
- Column chart: Average Monetary per Age Group

---

### 📦 Page 4: Product & Channel Preference
- Bar chart: Most Purchased Product Types by Age Group
- Column chart: Preferred Channel by Age Group
- Treemap: Total Spending by Age Group
- Column chart: Marketing Campaign Response by Age Group

---

## 🔍 Segmentation Logic (RFM Category)

| Category            | Criteria                                                  |
|---------------------|------------------------------------------------------------|
| Champion            | Recency = 5, Frequency = 5, Monetary = 5                   |
| Loyal High Spender  | All R, F, M ≥ 4                                            |
| Big Spender         | Monetary = 5 and Frequency ≤ 3                             |
| At Risk             | Recency ≤ 2 and Frequency ≥ 4 and Monetary ≤ 3            |
| Recent Low Value    | Recency ≥ 4 and Frequency ≤ 2 and Monetary ≤ 3            |
| Others              | All remaining combinations                                |

---

## 🛠 Tools Used

- **Power BI**
- **Power Query (M language)**
- **CSV Data**

---

## 🧑‍💼 Author

**Etebom Ntuk**  
[GitHub Profile](https://github.com/netebom) | [LinkedIn](https://www.linkedin.com/in/ntuk-etebom/)  

