# Zudio Retail Sales, Store Productivity & Inventory Velocity Analytics

[![Live Case Study](https://img.shields.io/badge/Live%20Case%20Study-View%20Portfolio-0F172A?style=for-the-badge&logo=vercel)](https://portfolio-sangram.vercel.app/project_2)
[![Tool](https://img.shields.io/badge/Power%20BI-Desktop%20%26%20DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#tech-stack--data-model)
[![Dataset](https://img.shields.io/badge/Dataset-25K%20Transactions%20%7C%2025%20Stores-1E293B?style=for-the-badge)](#dataset-overview)

An end-to-end **Power BI & DAX** retail analytics project modeled on **Zudio (Trent Ltd.)** 2026 Indian value-fashion operations. Built across **25,000 POS transactions**, **25 real store locations**, **60 private-label SKUs (₹49–₹999)**, and **1,500 store-SKU inventory records** to diagnose store real-estate efficiency, promotional margin erosion, and fast-fashion stock velocity.

👉 **[Explore the Full Interactive Case Study & 2K Dashboard Previews](https://portfolio-sangram.vercel.app/project_2)**

---

## Executive Snapshot

| Metric | Value | Context |
| :--- | :--- | :--- |
| **Total Net Sales** | **₹13.10M (₹1.31 Cr)** | 25,000 POS bills · 33,367 units sold (Jan–Nov 2026) |
| **Total Gross Profit** | **₹6.04M** | **46.16%** Gross Profit Margin · ₹523.80 AOV · 1.33 UPT |
| **Store Footprint** | **25 Active Stores** | 14 COCO (Company) · 11 FOCO (Franchise) · 269.9K Sq. Ft. |
| **Space Productivity** | **₹48.52 Sales / Sq. Ft.** | ₹22.39 Gross Profit / Sq. Ft. across 5 states |
| **Promotional Spend** | **₹483.36K (3.56% Avg)** | **₹1.56 Lakh** recoverable margin from >15% markdowns |
| **Inventory Velocity** | **58.93% Sell-Through** | 362 Low Stock Alerts · 9 Zero-Stock Outlets |

---

## Business Problems Solved

1. **Store Rent & Expansion ROI (COCO vs. FOCO):** Evaluated whether asset-light franchise stores (FOCO) in Tier-2/3 cities sustain the same profit margins as high-rent metro malls and high-street flagships (COCO).
2. **The >15% Discount Margin Cliff:** Identified the exact promotional threshold where deeper markdowns stop increasing customer basket size (UPT) and begin destroying gross margin.
3. **Inventory Velocity vs. Stockout Risk:** Pinpointed why high-demand ₹199–₹299 staples experienced stockouts in peak mall stores while slow-moving inventory tied up capital across 75%+ of store bins.

---

## Dashboard Suite (4 Views)

> **Note:** All 4 dashboards are also available in high-resolution PDF format in this repository and zoomable 2K previews on the [live portfolio page](https://portfolio-sangram.vercel.app/project_2).

### 1. Executive Overview — Sales & Customer Trends
Tracks monthly revenue and gross profit seasonality, peak shopping windows, payment mode adoption, and category contribution.

![Executive View Dashboard](images/dashboard_executive_view.webp)

* **Festive Peak:** October led the year at **₹18.2 Lakhs** in sales (₹8.46L profit) — more than double the post-EOSS low in February (₹8.7 Lakhs).
* **Evening Rush:** **55.18% of daily revenue (₹7.23M)** is generated during the **5 PM – 10 PM** window.
* **UPI-First Checkout:** **65.01% of revenue (₹8.51M)** flows through UPI, compared to 21.47% on Cards and 9.08% on Cash.
* **Volume vs. Margin:** Womenswear (39.0%) and Menswear (34.4%) drive **73.4%** of revenue, whereas **Beauty & Personal Care** yields the highest gross margin at **52.97%**.

---

### 2. Store Performance — Locations & Franchise Profitability
Compares store-level sales per sq. ft., regional footprint concentration, and City Tier × Operating Model margins.

![Store View Dashboard](images/dashboard_store_view.webp)

* **Maharashtra Anchor:** Maharashtra accounts for **81.73% of chain revenue (₹10.70M)**, with the 10 Pune outlets contributing **42.39% (₹5.55M)**.
* **Top Productivity Leader:** **Zudio – R City Mall, Ghatkopar** leads spatial density at **₹55.04/sq. ft.**, with 7 Pune stores ranking in the Top 10.
* **FOCO Margin Parity:** Franchise stores (**FOCO**) achieve a **46.20% gross margin**, matching company-owned (**COCO**) flagships (**46.13%**) while operating at lower lease costs across Tier-2/3 markets (**46.25%+** margin).

---

### 3. Discount Analysis — Protecting Profit Margins
Monitors campaign-level discount spend, seasonal EOSS spikes, and category markdown exposure.

![Discount View Dashboard](images/dashboard_discount_view.webp)

* **Full-Price Core:** **73.65% of all bills (18,412)** sold at **0% discount**, contributing ₹9.61M at a **48.07%** margin.
* **EOSS Concentration:** January (₹141.6K) and July (₹152.3K) clearance windows account for **60.81%** of annual discount spend.
* **The >15% Margin Cliff:** Moderate **10%–15%** bundles lift basket size from **1.28 to 1.67 UPT**, whereas **20%–30%** clearance markdowns fail to sustain basket growth (**1.38–1.42 UPT**) and crash margins to **26%–35%**. These deep discounts made up just **4.83% of bills** yet consumed **32.25% (₹1.56 Lakh)** of total discount spend.

---

### 4. Inventory & Stock — Best-Sellers & Stockout Alerts
Tracks SKU unit velocity, category sell-through rates, inventory holding days, and replenishment status across 1,500 store-SKU combinations.

![Stock View Dashboard](images/dashboard_stock_view.webp)

* **Sub-₹299 Essentials Lead Velocity:** All Top 5 best-sellers are priced ₹199–₹299, led by **Men Graphic Streetwear Tee (1,464 units)**, **Men Solid Cotton Crew-Neck Tee (1,439)**, and **Women Everyday Printed Straight Kurti (1,389)**.
* **Critical Stockouts:** All **9 zero-unit stockouts** occurred on high-velocity apparel and footwear basics at high-footfall Mumbai and Pune mall stores.
* **Working Capital Drag:** **75.27% (1,129)** of store-SKU bins held stock for over 130 days (overall avg: **137.28 days**), driven by slower **Beauty (40.0% STR)** and **Footwear (51.9% STR)** turnover vs. **Apparel (64%–65% STR)**.

---

## Tech Stack & Data Model

* **Data Ingestion & Validation:** Power Query (folder ingestion across 4 CSV tables, data type enforcement, duplicate & referential integrity checks).
* **Data Modeling:** Star Schema connecting 2 Dimension tables (`zudio_stores`, `zudio_products`) + a custom DAX `Calendar` table to 2 Fact tables (`zudio_sales_pos`, `zudio_inventory`) via 1-to-Many relationships.
* **Modular DAX Architecture:** Organized into four dedicated measure folders (`KPI`, `Store_KPI`, `Discount_KPI`, and `Stock View`).

### Sample DAX Measures

```dax
// Executive Gross Margin %
Gross Profit Margin % =
DIVIDE([Total Gross Profit], [Total Net Revenue], 0)

// Spatial Productivity
Revenue per SqFt =
DIVIDE([Total Net Revenue], SUM(zudio_stores[store_size_sqft]), 0)

// Promotional Governance
Effective Discount % =
DIVIDE([Total Discount Given], [Total Gross Amount], 0)

// Inventory Replenishment Health
Sell-Through Rate % =
DIVIDE(
    SUM(zudio_inventory[units_sold_ytd_2026]),
    SUM(zudio_inventory[total_available_units]),
    0
)
