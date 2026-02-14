# 📊 Project Background: OmniRetail Strategic Ad-Hoc Audit

**OmniRetail Pvt Ltd** is a diversified retail powerhouse operating across the African continent in the **Electronics, Clothing, Home & Kitchen, and Grocery** sectors. Despite a strong footprint in four major regions (North, South, East, West), the company was hit by a wave of operational friction: underperforming stores, high return rates in premium lines, and a visible misalignment between foot traffic and actual profitability.

**The mission was to move from "Observation" to "Optimization."** Originally, stakeholders tasked me with answering **9 fundamental business questions**. However, I recognized that these only scratched the surface. I proactively engineered **6 additional strategic questions** to bridge the gap between raw data and actionable recovery. This comprehensive **15-question audit** was designed to provide a surgical roadmap to stabilize the North region and fix the "Return Crisis" in Electronics.

Insights and recommendations are provided on the following key areas:

* **The Regional Divide** (West's Dominance vs. North's Decline)
* **The "Return" Crisis** (Plugging Value Leakage in High-Ticket Categories)
* **The Loyalty Vacuum** (Addressing the <20% Customer Retention Rate)
* **Category Dynamics** (Stabilizing Grocery & Accelerating Home/Toys)

https://github.com/user-attachments/assets/8ae9285d-b73e-44c4-a679-c016b5cbf571

**PowerQuery M Code regarding data preparation process of various tables can be found [[here]](https://github.com/mehedibhai101/Ad-hoc_Business_Analytics/tree/main/Data%20Cleaning).**

**DAX queries regarding various analytical calculations can be found [[here]](https://github.com/mehedibhai101/Ad-hoc_Business_Analytics/tree/main/DAX%20Calculations).**

**An interactive Power BI dashboard used to report and explore analysis can be found [[here]](https://app.powerbi.com/view?r=eyJrIjoiMjFlYzlhOTgtMzRjMy00ODdlLTkwNzEtNzVlOWUwNjJjMGY5IiwidCI6IjAwMGY1Mjk5LWU2YTUtNDYxNi1hNTI4LWJjZTNlNGUyYjk4ZCIsImMiOjEwfQ%3D%3D).**

---

# 🏗️ Data Structure & Initial Checks

The analysis is powered by a comprehensive transaction dataset (`OmniRetail.csv`) containing **500 records**, capturing the full lifecycle of retail operations from sale to return.

* **`Sale_ID` & `Sale_Date**`: Primary keys used to track transaction velocity and temporal trends.
* **`Customer_ID`**: The unique identifier used to measure the **Retention Rate** and calculate Customer Lifetime Value (CLV).
* **`Product_ID` & `Product_Category**`: Segmenting performance across **Electronics, Grocery, Clothing, Toys, and Home**.
* **`Store_ID` & `Region**`: Geographic attributes identifying the **North, South, East, and West** sales hubs.
* **`Quantity_Sold` & `Unit_Price**`: Core financial metrics (Unit Price is currently standardized at **$200.59** across the board).
* **`Payment_Method`**: Tracking the adoption of **Credit Card, Cash, UPI, and Net Banking** across different regions.
* **`Returned`**: A binary indicator (Yes/No) used to isolate "Value Leakage" and calculate the **10% overall return rate**.
* **`Total_Sale_Amount`**: The derived revenue metric representing the final transaction value.

### 🗺️ Entity Relationship Diagram (ERD)
![Entity Relationship Diagram](Dataset/entity_relationship_diagram.svg)

---

# 📋 Executive Summary

### Overview of Findings

The audit revealed that while OmniRetail is functional, it is highly fragmented. The **West Region** is the primary revenue engine (**$144K**), whereas the **North** is suffering from a visible **market contraction**. A major friction point was discovered in **Electronics**, where high return rates are eroding the margins of otherwise successful stores. Furthermore, the analysis identified a "Revenue-Traffic Paradox" in **Store S003**, which sees high transaction volume but fails to convert it into significant top-line revenue compared to its peers.

---

# 🔍 Strategic Insights (The 15-Question Breakdown)

### 🌏 The Regional Divide (The "West Side Story")

* **The West-South Power Couple:** The **West ($144K)** and **South ($130K)** regions account for the lion's share of revenue. These regions show stable purchasing patterns and should be the priority for new product launches.
* **The North Contraction:** Revenue in the **North** is on a declining trend. This isn't just a dip; it’s a systematic reduction in customer spend that requires an immediate assortment review.
* **The S003 Inefficiency:** While some stores are optimized, **S003** exhibits high footfall (order count) but low revenue per square foot. It is likely over-reliant on low-margin Grocery items rather than high-ticket Electronics.

<img width="1102" height="431" alt="Image" src="https://github.com/user-attachments/assets/b5ae9897-8377-4216-9bd1-2a979e567f52" />

### 📦 Product & Category Analysis

* **Electronics Margin Bleed:** While Electronics drive high AOV, they also suffer from the **highest return rates**. This suggests either a quality control issue or a mismatch between online descriptions and physical products.
* **Grocery Stability:** The **Grocery** category acts as the "Volume Engine," providing consistent cash flow even when luxury categories like Home & Kitchen fluctuate.

<img width="1167" height="336" alt="Image" src="https://github.com/user-attachments/assets/d78025e6-29b2-48bb-ae65-0fc741e3ab1f" />

### 👥 Customer Behavior & Payments

* **The One-and-Done Problem.** Data reveals a critical **Retention Rate of less than 20%**. The vast majority of customers make a single purchase and never return, indicating a failure in post-purchase engagement.
* **The "Silent" High-Value Customer.** A small segment of customers exhibits high spending with **zero returns**. These are our "Ideal Profiles," yet there is no dedicated program to lock them in.
* **The UPI Revolution:** In urbanized regions, **UPI and Credit Card** usage is surging. However, the **East region** remains heavily dependent on **Cash**, indicating a need for localized promotional offers to incentivize digital payments.

<img width="1169" height="421" alt="Image" src="https://github.com/user-attachments/assets/cba4de9c-02bb-4a14-8b24-821352200001" />

### 📅 Trends & Seasonality

* **Q1/Q4 Volatility:** Demand in the **North and East** spikes in Q2 but craters in Q1. Inventory levels are currently misaligned with these swings, leading to stockouts in summer and overstock in winter.

<img width="865" height="334" alt="Image" src="https://github.com/user-attachments/assets/0b3d5b92-1b1f-4b5b-bb25-1950660cb9a7" />

---

# 🚀 Recommendations:

* **The "Northern Revitalization" Plan:** Immediately audit the product mix in the **North Region**. Shift inventory away from slow-moving Electronics towards high-velocity Grocery and Home essentials to stabilize cash flow.
* **"Fit-First" Initiative:** To tackle the Clothing return crisis, implement a "True-Fit" sizing guide online and a stricter quality control check for Electronics suppliers. Target a **15% reduction in returns** within 6 months.
* **Launch "Omni-Prime" Loyalty:** addressing the <20% retention is critical. Launch a tiered loyalty program rewarding frequency over volume. Offer **"Free Next-Day Delivery"** to repeat buyers to lock in the Grocery segment.
* **Cross-Pollination Strategy:** Use the high-traffic Grocery category as a "Trojan Horse." Print **20% Off Coupons for Toys/Home** on every Grocery receipt to drive cross-category adoption.
* **Regional Payment Optimization:** In the cash-heavy East/North, incentivize digital payments with a **"5% Cashback on Digital Wallet"** promo to improve checkout speed and customer data capture.
* **Store-Level Re-Balancing:** Re-allocate high-margin inventory from **S003 to S006 (West)** where the "Propensity to Spend" is 15% higher.

---

## ⚠️ Assumptions and Caveats:

Throughout the analysis, the following strategic assumptions were made to address specific data architecture challenges identified during the audit:

* **Uniform Pricing Structure:** All products within the dataset currently share an identical Unit Price ($200.59). For this analysis, it is assumed that revenue variance is driven strictly by volume and regional sales velocity rather than price elasticity.
* **Flat Regional Hierarchy:** The data lacks a direct Region-to-Store hierarchy (e.g., the same Store ID appearing in multiple regions). Analysis assumes regional assignments in the fact table are the "Source of Truth" for geographic performance.
* **Product ID Granularity:** Some unique products share the same ID in the source system. Analysis treats these as category-level aggregations to maintain data integrity across the dashboard.
* **Retention Calculation:** Due to a lack of historical acquisition dates, retention is calculated as a percentage of unique Customer IDs appearing in more than one transaction cycle within the current window.

---

## 📂 Repository Structure

```
Ad-hoc_Business_Analytics/
│
├── Dashboard/                            # Final visualization and reporting outputs
│   ├── assets/                           # Visual elements used in reports (logos, icons, etc.)
│   │   ├── Icons/                        # Collection of icons used in KPI Cards/Buttons
│   │   └── Theme.json                    # Custom Power BI color palette for dashboard
│   ├── live_dashboard.md                 # Links to hosted Power BI Service report
│   └── static_overview.pdf               # Exported PDF version of the final dashboard for quick viewing
│
├── Data Cleaning/                        # ETL process and Power Query transformations
│   ├── calendar_table.m                  # M-script for generating a dynamic Calendar table
│   └── sales_table.m                     # M-script for cleaning and transforming raw sales records
│
├── Dataset/                              # The data foundation of the project
│   ├── entity_relationship_diagram.svg   # Visual map of table connections and cardinality
│   └── Sales_Data.csv                    # The primary raw data source containing transaction history
│
├── DAX Calculations/                     # Business logic and analytical formulas
│   ├── calculated_column.md              # Definitions for static row-level logic
│   └── measures.md                       # Dynamic aggregation formulas (e.g., Total Revenue, MoM Growth)
│
├── LICENSE                               # Legal terms for code and data usage
├── README.md                             # Project background, summary and key insights
└── business_questions.md                 # The 15 strategic business questions for Ad-hoc Analysis
``` 

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute it with proper attribution.

---

## 🌟 About Me

Hi! I’m **Mehedi Hasan**, well known as **Mehedi Bhai**, a Certified Data Analyst with strong proficiency in *Excel*, *Power BI*, and *SQL*. I specialize in data visualization, transforming raw data into clear, meaningful insights that help businesses make impactful data-driven decisions.

Let’s connect:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/mehedi-hasan-b3370130a/)
[![YouTube](https://img.shields.io/badge/YouTube-red?style=for-the-badge\&logo=youtube\&logoColor=white)](https://youtube.com/@mehedibro101?si=huk7eZ05dOwHTs1-)
