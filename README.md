<img width="1600" height="862" alt="Code_Generated_Image" src="https://github.com/user-attachments/assets/1c8ee0f0-e1e4-482e-8152-70e23548b4f5" />#  E-Commerce Executive Sales & Revenue Analytics

![Executive Sales Dashboard](dashboard_preview.png)

##  Executive Summary
This interactive Power BI analytics suite delivers executive-level visibility into global revenue performance, order distribution, and customer purchasing behaviors. Built to translate raw transactional datasets into strategic insights, the dashboard highlights high-growth international markets, seasonal revenue trends, and basket-size performance metrics.

---

##  Core Business Metrics (KPIs)
* **Total Revenue (`$10.14M`)**: Gross revenue accumulated across all active sales territories.
* **Total Orders (`22.1K`)**: Distinct invoice transaction count processed across the fulfillment pipeline.
* **Average Order Value (AOV) (`$458.54`)**: Dynamic revenue yield per invoice, modeled using DAX measure isolation.

---

##  Dynamic Visualizations

### 1. Revenue Trajectory Over Time
* Maps monthly revenue progression to expose seasonality and Q4 demand spikes.
* Highlights peak monthly performance hitting **$1.38M** in late-year promo periods.

### 2. Geographic Market Share
* Ranks global territories by overall revenue contribution.
* Demonstrates core market dominance in the **United Kingdom ($8.1M)** alongside key European expansion zones (**Germany**, **France**, **EIRE**, and **Netherlands**).

---

##  Data Architecture & Tech Stack
* **Business Intelligence:** Microsoft Power BI Desktop
* **Data Modeling:** Advanced DAX (Data Analysis Expressions) leveraging measure tables and divide safeguards
* **Data Prep & Storage:** PostgreSQL / Power Query M Language
* **UI/UX Design:** Custom Dark Slate Executive Palette with high-contrast data callouts

---


##  DAX Calculation Logic

```dax
// Cumulative Gross Revenue
Total Revenue = SUM(Sales[TotalSales])

// Unique Transaction Count
Total Orders = DISTINCTCOUNT(Sales[Invoice])

// Dynamic Average Order Value (AOV)
AOV = DIVIDE([Total Revenue], [Total Orders], 0)
