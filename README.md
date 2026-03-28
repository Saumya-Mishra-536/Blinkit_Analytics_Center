# Blinkit Business Analytics Project

**Customer Insights | Feedback Intelligence | Inventory Optimization**

---

## 📌 Project Overview

This project analyzes operational and customer datasets from Blinkit to generate meaningful business insights across three core domains:

- Customer Analytics
- Customer Feedback Analysis
- Inventory Management

The objective is to transform structured raw datasets into actionable KPIs and decision-support dashboards. The project demonstrates end-to-end business analytics implementation using Excel and Looker Studio, including data cleaning, validation, transformation, and visualization.

---

## 🎯 Business Objectives

### Customer Analytics
- Identify high-value customers
- Evaluate revenue contribution by segment
- Track customer acquisition trends
- Analyze geographic distribution

### Feedback Intelligence
- Measure customer satisfaction
- Identify service improvement areas
- Track complaint categories
- Monitor sentiment trends

### Inventory Optimization
- Reduce damaged inventory
- Monitor supplier performance
- Improve logistics handling
- Track operational losses

---

## 📊 Dataset Documentation

---

# 1️⃣ Customer Dataset

### 📌 Dataset Description

Contains demographic, geographic, and transaction summary data used for revenue analysis, segmentation, and lifecycle evaluation.

---

### 📌 Key Fields

| Field Name | Description | Data Type | Business Purpose |
|---|---|---|---|
| customer_id | Unique identifier for each customer | Numeric | Customer tracking |
| customer_name | Customer full name | Text | Identification |
| email | Customer email address | Text | Communication |
| phone | Full phone number | Text | Contact record |
| country_code | Extracted dialing code | Text/Numeric | Standardization |
| phone_number | 10-digit mobile number | Text/Numeric | Clean contact record |
| address | Customer residential address | Text | Geographic analysis |
| area | City/Region name | Text | Regional performance tracking |
| pincode | Postal code | Numeric | Location accuracy |
| registration_date | Date customer registered | Date | Acquisition trend analysis |
| customer_segment | Segment classification | Text | Targeted marketing |
| total_orders | Total number of orders placed | Numeric | Frequency analysis |
| avg_order_value | Average order value | Numeric | Spending behavior |

---

### 📊 Derived Metrics

| Metric Name | Formula | Business Use |
|---|---|---|
| Total Revenue | total_orders × avg_order_value | Revenue contribution analysis |
| Revenue by Segment | SUM(revenue) grouped by segment | Segment profitability |
| Average Order Value by Segment | AVG(avg_order_value) by segment | Spending behavior analysis |
| Top Customers | Rank customers by revenue | High-value customer identification |
| Customer Acquisition Trend | COUNT customers by registration_date | Growth monitoring |

---

# 2️⃣ Customer Feedback Dataset

### 📌 Dataset Description

Captures ratings, qualitative feedback, categorized issues, and sentiment classification for customer experience monitoring.

---

### 📌 Key Fields

| Field Name | Description | Data Type | Business Purpose |
|---|---|---|---|
| feedback_id | Unique feedback identifier | Numeric | Record tracking |
| order_id | Order associated with feedback | Numeric | Transaction linkage |
| customer_id | Linked customer identifier | Numeric | Customer-level analysis |
| rating | Numerical rating (1–5) | Numeric | Satisfaction measurement |
| feedback_text | Customer comment | Text | Qualitative insight |
| feedback_category | Issue category | Text | Root cause analysis |
| sentiment | Sentiment classification | Text | Satisfaction classification |
| feedback_date | Date feedback submitted | Date | Trend analysis |

---

### 📊 Derived Metrics

| Metric Name | Formula | Business Use |
|---|---|---|
| Customer Satisfaction Rate | % of ratings ≥ 4 | Satisfaction measurement |
| Sentiment Distribution | COUNT feedback by sentiment | Experience monitoring |
| Complaint % by Category | Category complaints / total complaints | Issue prioritization |
| Monthly Rating Trend | AVG rating by month | Service improvement tracking |
| Negative Feedback Rate | Ratings ≤ 2 / total feedback | Risk detection |

---

# 3️⃣ Inventory Dataset

### 📌 Dataset Description

Tracks product-level stock intake and damaged stock quantities for operational efficiency and loss monitoring.

---

### 📌 Key Fields

| Field Name | Description | Data Type | Business Purpose |
|---|---|---|---|
| product_id | Unique product identifier | Numeric | Product tracking |
| date | Stock entry date | Date | Time-based monitoring |
| stock_received | Quantity received | Numeric | Inventory tracking |
| damaged_stock | Quantity damaged | Numeric | Loss measurement |

---

### 📊 Derived Metrics

| Metric Name | Formula | Business Use |
|---|---|---|
| Damage Percentage | (damaged_stock / stock_received) × 100 | Loss tracking |
| Total Damaged Units | SUM(damaged_stock) | Operational loss measurement |
| High-Damage Products | Rank by damage % | Quality improvement |
| Inventory Efficiency | 100 − Damage % | Operational performance |
| Validation Flag | damaged_stock ≤ stock_received | Data quality control |

---

## 🧹 Data Cleaning & Standardization

- Converted text fields to proper case
- Standardized address formatting
- Removed line breaks from address entries
- Split phone number into country code and mobile number
- Validated phone number format
- Standardized sentiment labels using rating rules
- Flagged invalid inventory records
- Created revenue and damage percentage metrics

---

## 📈 Dashboard Structure

### KPI Overview
- Total Customers
- Total Revenue
- Total Orders
- Average Order Value
- Customer Satisfaction Rate
- Overall Damage Percentage

### Customer Analytics Dashboard
- Segment-wise Revenue
- Customer Distribution
- Top Customers
- Registration Trends

### Feedback Dashboard
- Sentiment Distribution
- Category-wise Issues
- Rating Trends Over Time

### Inventory Dashboard
- Damage Percentage
- High-Damage Products
- Stock vs Damaged Comparison

---

## 🔗 Looker Studio Dashboards

Three interactive dashboards have been published on Looker Studio, each powered by a dedicated dataset. Below is a breakdown of each dashboard, the tables used, and key metrics visualized.

---

### 📊 Dashboard 1 — Customer Analytics

**Link:** https://lookerstudio.google.com/embed/reporting/c0edb5d3-e2f3-47b1-ac47-48a23cd9d900/page/page_12345

**Tables Used:**
| Table | Purpose |
|---|---|
| `customer` | Core table — customer demographics, segments, orders, revenue |

**Key Visuals:**
- Segment-wise revenue breakdown (bar chart)
- Top customers by revenue (ranked table)
- Customer distribution by area/region (map / bar)
- Registration trend over time (line chart)
- KPIs: Total Customers, Total Revenue, Total Orders, Avg Order Value

---

### 📊 Dashboard 2 — Customer Feedback Intelligence *(New)*

**Link:** https://lookerstudio.google.com/embed/reporting/f370c2d0-90f4-4ff2-91ab-8a9fc374e4d3/page/p_c5h14ci21d

**Tables Used:**
| Table | Purpose |
|---|---|
| `customer_feedback` | Core table — ratings, sentiment, feedback categories, dates |
| `customer` | Joined for customer-level feedback aggregation |

**Key Visuals:**
- Sentiment distribution — Positive / Neutral / Negative (donut chart)
- Feedback volume by category: Delivery, Product Quality, App Experience, Support, Packaging, Pricing (bar chart)
- Rating distribution across 1–5 stars (histogram)
- Monthly average rating trend (line / bar chart)
- KPIs: Total Feedback, Avg Rating, Satisfaction Rate (ratings ≥ 4), Negative Feedback Rate

**Dashboard Preview:**

> *See the Looker Studio dashboard screenshot below — displays the Feedback Intelligence page with KPI cards, category-wise complaint breakdown, sentiment donut chart, rating histogram, and monthly trend.*

![Blinkit Customer Feedback Dashboard](Images/feedback_dashboard_preview.png)

---

### 📊 Dashboard 3 — Inventory Management

**Link:** https://lookerstudio.google.com/reporting/545b506c-1370-44fc-87d3-7e5c92b3ddb3/page/aNBqF

**Tables Used:**
| Table | Purpose |
|---|---|
| `inventory` | Core table — product stock received and damaged quantities |

**Key Visuals:**
- Damage percentage by product (bar chart)
- High-damage product rankings (sorted table)
- Stock received vs damaged comparison (grouped bar)
- Inventory efficiency trend over time (line chart)
- KPIs: Total Stock Received, Total Damaged Units, Overall Damage %, Inventory Efficiency

---

## 🛠 Tools & Technologies

- Microsoft Excel
- Looker Studio
- Data Cleaning & Validation
- KPI Development
- Dashboard Design
- Business Analytics Framework

---

## 💡 Key Insights Generated

- Premium customers contribute the highest revenue share
- Delivery issues dominate negative feedback (largest complaint category)
- Positive sentiment correlates with repeat purchases
- Damaged inventory highlights logistics improvement opportunities
- Monthly rating trends show gradual improvement in customer experience

---

## ✅ Conclusion

This project demonstrates comprehensive business analytics across customer performance, service quality, and operational efficiency. By integrating customer behavior insights, structured sentiment analysis, and inventory monitoring, the project provides a holistic view of business performance and supports data-driven strategic decision-making.

---

## 👤 Author

Saumya Mishra
