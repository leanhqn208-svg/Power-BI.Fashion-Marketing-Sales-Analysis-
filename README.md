# [Power BI] Fashion Marketing Sales Analysis 


## Table of Contents

1. [📌  Overview](#-overview)  
2. [📂 Dataset & Data Model](#-dataset--data-model)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)
---

## 📌 Overview

### Project Overview
This project focuses on analyzing the business and marketing data of a multi-channel fashion retail and e-commerce enterprise.
It uses a tactical dashboard to link advertising spend with revenue at the SKU level.

### Problem Statement
The business currently lacks a unified view of its marketing effectiveness. 
Sales revenue and marketing costs (CPM, CPC, CTR) are stored in separate datasets, making it difficult for leadership:
* **Identify Profit Drivers:** Determine which specific campaigns or products (SKUs) are truly driving growth.
* **Evaluate ROI:** Measure the real Return on Investment across different marketing channels.
* **Optimize Budget:** Stop wasting resources on underperforming campaigns and reallocate funds to high-conversion areas.

### Core Business Questions
The project focuses on answering key tactical questions:
* **ROI/ROAS:** What is the Return on Ad Spend (ROAS) for each campaign and SKU? 
* **Correlation:** How do marketing metrics like CPM, CPC, and CTR impact net sales?
* **Budget Optimization:** How can we reallocate the budget to maximize total revenue based on KPIs?

---

## 📂 Dataset & Data Model
The dataset (`[DAC] Project 3 - Dataset.xlsx`) contains three core tables:

1. **`Order`**: Raw order-level data including Order ID, timestamp, source (organic/admin), product, category, price, quantity, COGS, and order status.
2. **`mkt_camp_cost`**: Campaign-level daily marketing spend with CPM, CPC, CTR, impressions, and click metrics per campaign.
3. **`mkt_camp_by_sku_cost`**: Campaign × SKU-level breakdown of ads spend, allocated orders, impressions, inbox/comment counts, and derived ROAS metrics.
Includes a `Sample Description` sheet explaining how each marketing KPI is calculated per SKU per campaign.

### Data Model
This project utilizes a Star Schema architecture to ensure performance and analytical flexibility in Power BI.
Two main Fact tables track sales orders and marketing costs per product. 
These connect to shared Dimension tables for dates, products, and campaigns.
<img width="1049" height="630" alt="image" src="https://github.com/user-attachments/assets/202e3415-7ed6-4eca-b10c-dfa926cf441c" />

## 🧠 Design Thinking Process

To ensure this dashboard delivers real business value rather than just displaying raw numbers, I applied a structured Design Thinking approach. This helped bridge the gap between technical data modeling and the actual needs of the business stakeholders (Marketing & Sales Managers).
## 1️⃣ Empathize
<img width="847" height="476" alt="image" src="https://github.com/user-attachments/assets/6841479d-39dc-4ea3-bf3a-26bbdbc2e132" />
<img width="847" height="476" alt="image" src="https://github.com/user-attachments/assets/7cbb8fd9-7388-41c5-905b-61b4f9dce7c5" />


## 2️⃣ Define Point of View (POV)
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/edbd878b-89e0-4f57-9aa8-8c0a11c204bc" />

 
<br>

#### Part 2: Dashboard Information Architecture
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/c1120fcc-228a-49be-8429-3f54ca2a7b00" />


## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  
<img width="1100" height="613" alt="image" src="https://github.com/user-attachments/assets/2507e853-1aab-4194-bd71-0e3f9933b8c8" />



**Observation:** The campaign shows strong overall performance with an Ads Revenue of 3bn and a healthy ROAS of 7.67. However, the Weekly Profit Breakdown reveals a critical trend: while revenue remains high, profitability peaked in Week 2 (+623M) and crashed severely in Week 4 (-530M) and Week 5 (-605M). This indicates that rising ad costs or heavy discounting at the end of the month is eroding all previous gains.

**Recommendation:** Immediately audit and cut low-performing campaigns in the final two weeks of the month to stop the profit bleed. Shift the 17% unspent budget (Utilization is only 83%) toward the top-performing SKU, Kino Dress 2, during its peak performance window to maximize overall margins.

#### 2️⃣ Dashboard 2 Preview 
<img width="1010" height="566" alt="image" src="https://github.com/user-attachments/assets/00fab7e7-1f52-464c-81ec-e154990df4ba" />



**Observation:** The funnel shows a big gap between Impressions (5.11M) and Clicks (0.04M), leading to a low CTR of 0.82%. The Scatter Plot shows that as we show ads more, the cost (CPM) goes up, making it more expensive to reach new people.

**Recommendation:** Focus on testing new ad images to push the CTR above 1%. Spend more on the Váy Chiết Eo Ôm category (highest CTR 1.11% and ROAS 26.23) and stop spending on Chân Váy Tách Set due to its low performance (CTR 0.55%).

#### 3️⃣ Dashboard 3 Preview  
<img width="1007" height="565" alt="image" src="https://github.com/user-attachments/assets/65ce991d-1829-44a3-b663-b8863f1b8b79" />


**Observation:** Performance is highly polarized across the inventory. Lisa Dress 5 and (G)Margnet Dress are exceptionally efficient with ROAS over 17.0, while Audrey Shirt 3 leads in total volume (311M Sales). However, the Weekly Profit Breakdown (Waterfall chart) confirms a net loss in the final two weeks, indicating that high-volume items like the Audrey series may be driving revenue at the expense of late-month margins.

**Recommendation:** Prioritize budget for Lisa Dress 5 to exploit its high efficiency (43.67 ROAS). For lower-performing SKUs like Nalani 2 (high 22K CPC), stop active promotion and shift funds toward the "Tơ" and "Lanh" material categories, which currently contribute over 75% of total revenue.

---

## 🔎 Final Conclusion & Recommendations
📌 Key Takeaways:

* While the marketing campaign achieved a highly impressive headline **ROAS of 7.67** and generated **3bn in Ads Revenue**, a deeper diagnostic reveals structural inefficiencies that severely compromise bottom-line profitability. The project uncovers a classic retail trap: scaling volume at the expense of margins. A critical profit bleed in the final two weeks of the month completely erased the massive gains from Weeks 1 and 2. By transitioning from a generalized spending model to a highly targeted, performance-driven allocation strategy, the business can safeguard its margins while unlocking the 17% unspent budget to fuel proven growth engines.
* Campaign performance was severely bottlenecked by three critical inefficiencies: a late-month profit crash in Weeks 4 and 5 (losing  **-530M** and  **-605M** respectively) driven by soaring month-end CPM/CPC costs and heavy discounting that eroded product margins; severe top-of-funnel friction where  **5.11M impressions** yielded a low  **0.82% CTR** and a mere ~0.2% purchase conversion rate (indicating high-volume but low-intent traffic); and extreme product polarization where capital remained trapped in underperforming assets like Nalani 2 (unsustainable 22K CPC) while high-efficiency "star" products like Lisa Dress 5 (43.67 ROAS) were starved of optimal ad spend.

🚀 Key Actions:

* **1. Immediate Budget Optimization (Next 14 Days):**
**Implement a Hard Cap / Early Kill Switch:** Automatically scale down ad budgets by **50–70%** or halt non-essential conversion campaigns during **the final 10 days** of the month when CPM spikes. Shift to a "maintenance mode" to lock in the profit margins generated in the first half of the month.
**Aggressive Asset Reallocation:** Fully liquidate ad spend on bottom-tier performers **(Chân Váy Tách Set, Nalani 2)**. Funnel that saved capital, along with the **17% unspent budget** buffer, directly into the **"Tơ"** and **"Lanh"** material categories, which already anchor **75% of total revenue**.

* **2. Funnel & Creative Overhaul (Next 30 Days):**
**A/B Test Creative Assets to Break the 1% CTR Barrier:** Since the scatter plot proves that ad costs increase as impressions scale, we must maximize the value of every impression. Pivot creative directions for **low-CTR lines** by testing high-engaging video formats (e.g., styling lookbooks, fabric movement showcases) to push CTR past the **1.11% benchmark** set by the Váy Chiết Eo Ôm category.
**Deploy a Low-Cost Mid-Funnel Retargeting Strategy:** Do not waste cold traffic. Allocate a dedicated **10% of the budget** strictly to retargeting **the 40,000 users (0.04M)** who clicked/interacted but did not purchase, utilizing custom incentives (e.g., limited-time abandoned cart bundles) rather than paying to acquire new cold impressions.
