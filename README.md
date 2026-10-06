# 🛒 E-Commerce Business Intelligence & Analytics Case Study

## 📌 Executive Summary
This project evaluates transactional data from a multi-category e-commerce platform to extract commercial insights across four operational verticals: **Customer Strategy**, **Product Management**, **Revenue Optimization**, and **Supply Chain Operations**. 

By querying raw transactional ledgers, customer profiles, and catalog data, this project addresses real-world business challenges such as identifying customer acquisition hubs, measuring MoM financial velocity, evaluating catalog deadstock, and modeling purchase frequency cohorts.

---

## 🏢 Business Verticals & Objectives

### 1. Customer Intelligence & Segmentation
* **Market Geography:** Identifies high-density customer regions to optimize regional fulfillment hubs, lower last-mile delivery overhead, and focus localized marketing budgets.
* **Buyer Lifecycle Segmentation:** Evaluates purchase frequencies to categorize the user base into single-purchase buyers, occasional shoppers, and repeat customers for customized retention funnels.
* **Cohort Acquisition Tracking:** Evaluates organic user growth month-by-month based on customer initial order dates, measuring marketing acquisition momentum.

### 2. Product Portfolio & Market Fit
* **High-Value Single-Unit Items:** Pinpoints high-ticket catalog products purchased individually rather than in bulk, revealing premium-tier consumer demand.
* **Category Market Reach:** Analyzes unique customer penetration across merchandise categories to identify broad-appeal acquisition drivers versus niche catalog categories.
* **Low-Engagement Product Pruning:** Identifies low-traction SKUs purchased by less than 5% of the overall customer base to minimize dead inventory storage costs.

### 3. Revenue Trends & Unit Economics
* **Month-on-Month (MoM) Growth:** Tracks monthly revenue velocity and calculates percentage expansion/contraction rates over time.
* **Average Order Value (AOV) Fluctuation:** Monitors changes in average basket value across monthly cycles to evaluate pricing strategies, minimum-order thresholds, and cross-sell effectiveness.
* **Seasonal Sales Peaks:** Evaluates sales concentration across calendar months to identify seasonal demand surges for operational planning.

### 4. Supply Chain & Inventory Planning
* **High-Turnover Velocity:** Isolates fastest-moving SKUs by total units sold to maintain continuous availability and calibrate inventory reorder points.

---

## 🗄️ Relational Data Model

The analysis operates on a normalized schema consisting of four entities:

* **Customers:** Unique customer identifiers, full names, and geographical locations.
* **Products:** Product catalog attributes including categories and baseline retail pricing.
* **Orders:** Master transaction records capturing order timestamps, customer linkage, and gross checkout value.
* **OrderDetails:** Granular line-item breakdown documenting SKU quantities and executed transaction prices.

---

## ⚙️ Analytical Methodology & Techniques

* **Multi-Stage Data Modeling (CTEs):** Segmented complex multi-step questions into modular, readable analytical layers.
* **Chronological Trend Analysis (Window Functions):** Computed period-over-period revenue trajectories and basket value fluctuations without row duplication or multi-pass joins.
* **Cohort Acquisition Modeling:** Isolated initial customer purchase timestamps using grouped temporal aggregation to distinguish new user conversions from repeat purchases.
* **Benchmarking & Penetration Ratios:** Built customer penetration metrics using subquery denominators to assess long-tail catalog engagement.
* **Relational Joins & Set Aggregation:** Connected order histories with regional demographic attributes to maintain accurate customer and product counts.

---

## 📈 Key Strategic Insights Delivered

| Focus Area | Key Metric Analyzed | Strategic Business Impact |
| :--- | :--- | :--- |
| **Logistics** | Regional Customer Concentration | Informs regional fulfillment center investments and supply chain hubs. |
| **Retention** | Order Frequency Distribution | Guides re-engagement email campaigns and loyalty reward tiers for 1-time buyers. |
| **Catalog** | Category Reach & Unit Demand | Informs vendor sourcing, warehouse allocation, and bundle marketing. |
| **Finance** | MoM Growth & AOV Trajectory | Separates customer acquisition growth from average cart basket expansion. |
| **Inventory** | High-Velocity vs. Deadstock SKUs | Mitigates inventory holding costs by identifying candidates for clearance. |

---

## 📂 Repository Contents

* `README.md` — Project context, analytical architecture, and business summary.
* `schema.sql` — Data definition scripts (DDL) for table setup, constraints, and relationships.
* `analysis_queries.sql` — Modular SQL queries written to solve each business problem statement.
