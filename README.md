
# Logistics & Profitability Insight Hub

## Project Overview

This project is an end-to-end business intelligence tool built in Excel to analyze a large-scale (180,000+ rows) supply chain dataset. The goal was to move beyond static reporting and create a dynamic, automated "Command Center" that empowers business leaders to track performance, identify process bottlenecks, and make data-driven decisions to enhance profitability and customer satisfaction.

The dashboard provides a holistic view of the supply chain by integrating financial, customer, and logistics data, focusing on actionable KPIs like On-Time Delivery (OTD), regional profitability, and revenue at risk.

---


## 📊 Interactive Dashboard Showcase

The core of this project is a fully interactive dashboard designed for executive-level review.

### Main Command Center View
*This view provides a high-level summary of all key performance indicators.*
[![Main Dashboard](Images/dashboard_main.png)](https://github.com/AbHaq24/Supply-Chain-Performance-Profitability-Command-Center/blob/main/Screenshot%202025-09-09%20151222.png)

### Deep Dive Analysis: Isolating a Problem Area
*Here, the dashboard is filtered to analyze the performance for **High-Value Customers in the LATAM market**, immediately revealing a critical service-level issue.*
[![Filtered View of LATAM Market](Images/dashboard_filtered_latam.png)](https://github.com/AbHaq24/Supply-Chain-Performance-Profitability-Command-Center/blob/main/Screenshot%202025-09-09%20153650.png)

---

## 🛠️ Technical Implementation

This project was developed entirely within Microsoft Excel, leveraging its advanced data analytics capabilities.

*   **ETL (Extract, Transform, Load):** **Power Query** served as the backbone for the data pipeline. It was used to:
    *   Connect to the raw CSV data source.
    *   Perform data cleaning, type correction, and handle missing values.
    *   Engineer new, value-added features for analysis, including:
        *   `Profit`: Calculated from sales and profit ratio.
        *   `On-Time Status`: A binary flag to classify every order.
        *   `Customer Value Tier`: A segmentation of orders into High, Mid, and Low-Value.

*   **Data Modeling & Analysis:**
    *   The cleaned data was loaded into Excel's **Data Model** to ensure efficient processing and analysis.
    *   **PivotTables** were used to aggregate data and compute all KPIs. A centralized **"KPI Hub"** sheet was implemented to reliably feed the main dashboard cards, a best practice for complex dashboards.

*   **Visualization & Interactivity:**
    *   The dashboard was built using **PivotCharts**, **Slicers**, and dynamically linked **KPI cards**.
    *   This design allows users to seamlessly filter the entire report across multiple dimensions (Region, Customer Tier, Product, Year) to uncover granular insights.

---

## 📈 Key Findings & Business Impact

The analysis uncovered three critical, actionable insights that could drive significant business value:

1.  **Critical Service Failure:** The overall **On-Time Delivery (OTD) rate was only 42.7%**. This poor performance directly puts **$21 Million in annual revenue at risk** from dissatisfied customers and potential order cancellations.

2.  **Identified Bottleneck:** The root cause of poor performance was traced to a specific area: **'Standard Class' shipments within the LATAM market** accounted for a disproportionately high number of delivery failures. This provides a clear target for operational improvement.

3.  **High-Value Customer Neglect:** The analysis revealed that **High-Value customers were experiencing a late delivery rate of 41%**, indicating that the company's most profitable segment was receiving a suboptimal service experience, posing a significant risk to long-term loyalty and revenue.

---

## 🚀 How to Replicate This Project

This project is designed to be fully reproducible.

1.  **Download the Template:** Clone this repository or download the `Supply_Chain_Template.xlsx` file.
2.  **Get the Data:** Download the source CSV file from [DataCo Smart Supply Chain on Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis).
3.  **Connect the Source:**
    *   Open `Supply_Chain_Template.xlsx`.
    *   Go to **Data > Queries & Connections**.
    *   Right-click the query and select **Edit** to open the Power Query Editor.
    *   In the "Applied Steps" pane, click the gear icon next to the **Source** step.
    *   Browse and point the connection to the CSV file you downloaded.
4.  **Refresh and Explore:** Close the Power Query Editor, then go to the **Data** tab and click **Refresh All**. The dashboard will be fully populated and interactive.
