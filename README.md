# RFM Analysis and Cashback Program for Online Fashion Store

> **RFM Dashboard Preview**
>
> ![RFM Segmentation Dashboard](https://github.com/luizzangelo/RFM_analysis/blob/main/Screenshot%202025-06-23%20at%2017.24.21.png?raw=true)

## 📖 Overview

Welcome to this project repository showcasing an **RFM Analysis** (Recency, Frequency, Monetary) combined with a **Cashback program** for an online fashion store. The primary goal is to understand customer behavior, strategically segment the customer base, and deliver personalized communication to boost engagement and retention.

---

## 🎯 Motivation & Objectives

1. **Why perform this analysis?**

   * Identify the most valuable and engaged customers.
   * Spot promising customers who need an extra push to purchase again.
   * Detect inactive or at-risk customers for reactivation campaigns.
   * Map the customer journey and tailor communications accordingly.

2. **What is the analysis used for?**

   * Optimize marketing spend by targeting campaigns to the most relevant segments.
   * Implement a Cashback program to encourage repeat purchases and loyalty.
   * Provide actionable insights for customer lifecycle management.

---

## 📥 Data Extraction

* **Source**: Loja Integrada platform.
* **Extracted fields**:

  * Customer ID.
  * Date of last order.
  * Total number of orders and total sales value.
  * Complete order history.

> Data was exported as CSV directly from the Loja Integrada admin panel, capturing all sales within the analysis period.

---

## 🔄 Data Preparation with Power Query

1. **Import**

   * Connected to the CSV file via Power Query in Excel.

2. **Cleaning**

   * Removed duplicate or invalid records.
   * Standardized date formats (`dd/mm/yyyy`).
   * Normalized numeric fields (stripped currency symbols and fixed decimal separators).

3. **Transformations**

   * Created auxiliary columns:

     * **Recency**: Days since the last purchase.
     * **Frequency**: Total number of orders per customer.
     * **Monetary Value**: Sum of all purchase amounts.
   * Calculated RFM scores by grouping and ranking customers into segments (e.g., top 20% most recent purchasers).

4. **Cashback Column**

   * Defined a cashback rate (e.g., 5% of each purchase).
   * Computed the cashback amount and added a column showing the available credit for the next purchase.

> Power Query ensures full reproducibility: simply refresh to update with new data.

---

## 📊 Analysis & Insights

### RFM Segments

* **New Customers**: High recency, low frequency, moderate spend.
* **Loyal Customers**: High frequency and consistent spend.
* **Potential Loyalists**: Moderate recency with increasing frequency.
* **Churned Customers**: Very high recency (long time since last purchase).

| Segment             | Recommended Action                                  |
| ------------------- | --------------------------------------------------- |
| New Customers       | Welcome offers or educational content.              |
| Potential Loyalists | Exclusive promotions to encourage repeat purchases. |
| Loyal Customers     | VIP program and additional cashback bonuses.        |
| Churned Customers   | Reactivation campaigns (email, SMS).                |

### Cashback as an Incentive

* Cashback is credited toward the customer’s next purchase.
* Each new transaction increases the available credit, driving repeat business.
* Example: A €100 purchase yields €5 cashback for the next order.

---

## 🚀 Next Steps

1. **Automation**: Migrate Power Query steps to a centralized ETL system (e.g., Azure Data Factory, Google Cloud Dataflow).
2. **CRM Integration**: Sync RFM segments and cashback balances in real time.
3. **A/B Testing**: Experiment with different cashback rates and communication formats.
4. **Dashboarding**: Build interactive visuals in Power BI or Looker to monitor key metrics.

---

## 📝 Contributions

This repository demonstrates how to leverage Excel and Power Query for customer intelligence in e-commerce. Feel free to open issues or submit pull requests to suggest improvements.

---

<div align="center">
  <sub>Created by **Luiz Angelo** • Analysis Date: 06/23/2025</sub>
</div>
