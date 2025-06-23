# RFM Matrix Analysis for Fashion Online Store

## 📖 Overview

* Connection to the CSV file via Power Query in Excel.

2. **Cleaning**

* Removal of duplicates and invalid records.

* Conversion of dates to the standard format (`dd/mm/yyyy`).

* Standardization of numerical fields (removal of symbols and adjustment of decimal separators).

3. **Transformations**

* Creation of auxiliary columns:

* **Recency**: number of days from the last purchase to the date of analysis.

* **Frequency**: total number of orders per customer.

* **Monetary Value**: sum of the value of all purchases.

* Calculation of **RFM scores** by grouping and generation of tracks (for example, top 20% most recent customers, etc.).

4. **Cashback Column**

* We define a cashback percentage on each sale (for example, 5% of the purchase amount).

* We calculate the monetary value of the cashback and add a column that shows the credit available for the next purchase.

> Power Query allowed you to keep the process reproducible: just re-reprove the steps when updating the data.

---

## 📊 Analysis and Insights

### RFM Segmentation

* **New Customers**: High recency, low frequency and moderate monetary value.

* **Loyal Customers**: High frequency and consistent monetary value.

* **Promising Customers**: Moderate recency and increasing frequency.

* **Lost Customers**: Very high Recency (many days without buying).

| Segment | Recommended action |

| --------------------- | ----------------------------------------------- |

| New Customers | Welcome with discount or educational content. |

| Promising Customers | Encourage with exclusive offers. |

| Loyal Customers | VIP program and cashback bonus. |

| Lost Customers | Reactivation campaigns (e-mail, SMS). |

### Cashback as an Incentive

* The cashback amount appears as credit on the next purchase.

* With each new purchase, the customer accumulates more balance and becomes more likely to return.

* Example: customer who spent R\$100.00 receives R\$5.00 cashback to use on the next purchase.

---

## 🚀 Next Steps

1. **Automation**: Migrate the Power Query flow to a centralized ETL solution (for example, Azure Data Factory or Google Cloud Dataflow).

2. **Integration with CRM**: Synchronize RFM segmentations and cashback credits in real time.

3. **A/B tests**: Validate different percentages of cashback and communication formats.

4. **Dashboard**: Develop interactive dashboards in Power BI or Looker to monitor key metrics.

---

## 📝 Contributions

This project is an example of how to use Excel and Power Query for customer intelligence analysis in e-commerce. Feel free to suggest improvements or create issues for discussion.

---

<div align="center">

<sub>Develoved by **Luiz Angelo** • Date of analysis: 06/23/2025</sub>

</div>
