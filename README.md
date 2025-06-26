# 🛒 Superstore Sales Analysis Report

## 📊 Introduction

This report provides a comprehensive sales performance analysis of a fictional superstore using historical transaction data. The goal is to identify trends, evaluate profitability, assess customer behavior, and recommend data-driven strategies to boost performance.


## 🎯 Aims and Objectives

**Aim:**  
To analyze superstore sales data in order to uncover business insights, evaluate performance metrics, and guide strategic decisions.

**Objectives:**
1. Measure overall and regional sales performance.
2. Understand product and category profitability and return patterns.
3. Segment customers and assess order behaviors.
4. Generate actionable recommendations based on findings.


## 🛠️ 1. Data Preparation

**Source data sheets:**
- `Orders`: Master sales data
- `Customer Name`: Links Order ID to Customer Name
- `Returns`: Contains Returned Order IDs

**Merging Steps:**
- **Customer Lookups**:  
  `=XLOOKUP([@Order ID], 'Customer Name'!B:B, 'Customer Name'!A:A)`  
  → Appended customer names to the Orders sheet.

- **Return Flag**:  
  `=IF(COUNTIF(Returns!A:A, [@Order ID]) > 0, "Returned", "Not Returned")`  
  → Flagged return status for each order.

- **Validation**:
  - Removed duplicates.
  - Spot-checked merged records.
  - Ensured there were no `#N/A` or null lookup results.


## 📈 2. Dashboard Visualizations

### a. Key Performance Indicators (KPIs)
- **Total Sales**: `$14.92M`
- **Total Profit**: `$1.52M`
- **Total Orders**: `8.40K`
- **Return Rate**: `7%`

### b. Key Visuals
- **Sales by Region**
- **Order Quantity by Customer Segment**
- **Sales by Product Sub-Category**
- **Return Status by Product Category**
- **Profit by Product Category**


## ❓ 3. Business Questions Answered

1. Which regions are generating the highest and lowest sales?
2. What is the order distribution across different customer segments?
3. Which product sub-categories are driving the most revenue?
4. What percentage of products are returned per category?
5. Which categories and sub-categories are most and least profitable?
6. How does product return impact profitability?
7. What are the trends in high-volume vs low-profit items?
8. Which customer segments can be prioritized for growth?


## 🔍 4. Insights

### Overall Performance
- **Moderate profit margin** of ~10.2% with a **7% return rate** that affects bottom line.
  
### Regional Analysis
- **West** region dominates with $3.60M in sales.
- **Nunavut** lags behind with just $0.12M — a 29x gap vs West.

### Customer Segmentation
- **Corporate clients** make the most orders (79K), suggesting higher B2B activity.
  
### Product Performance
- **Top Sellers**: Office Machines, Tables, Telephones.
- **Low Performers**: Rubber Bands, Labels, Scissors.
  
### Returns
- **Office Supplies** have the highest return count (461).
- **Furniture** and **Technology** follow with lower but notable return volumes.

### Profitability
- **Technology** is the most profitable category ($886K, 58% of total).
- **Furniture** contributes the least profit despite significant sales.


## ✅ 5. Recommendations

1. **Boost High-Margin Sales**  
   - Prioritize **Technology** marketing and upselling to maximize profit per order.

2. **Reduce Returns**  
   - Investigate **Office Supplies** quality and expectation mismatches.
   - Implement a **pre-purchase validation system** or clearer product descriptions.

3. **Regional Strategy**  
   - Create targeted promotions for **Nunavut** and **Yukon**.
   - Use success strategies from the **West** to uplift underperforming areas.

4. **Customer-Focused Campaigns**  
   - Tailor loyalty and retention strategies for **Corporate** segment.
   - Increase engagement with **Small Business** and **Home Office** through custom bundles or discounts.

5. **Optimize Inventory**  
   - Consider phasing out underperforming SKUs (e.g., **Rubber Bands**, **Labels**).
   - Reallocate shelf and promo space to high-turnover items.



📁 Superstore-Sales-Analytics
├── Superstore Sales Analytics Dashboard.png
├── README.md
└── Superstore.xlsx
