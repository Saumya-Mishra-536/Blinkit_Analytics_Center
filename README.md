Blinkit Business Analytics Project

Customer Insights | Feedback Intelligence | Inventory Optimization

Project Overview

This project analyzes operational and customer data from Blinkit to generate meaningful business insights across three core areas: Customer Analytics, Customer Feedback Analysis, and Inventory Management.

The objective is to transform structured raw datasets into performance metrics and decision-support dashboards. The analysis focuses on customer behavior, service quality measurement, and operational efficiency monitoring.

Through systematic data cleaning, validation, transformation, and visualization, this project demonstrates end-to-end business analytics implementation using Excel.

Dataset Overview

The project consists of three primary datasets:

Customer Dataset

Customer Feedback Dataset

Inventory Dataset

Each dataset serves a distinct analytical purpose and contributes to overall business performance tracking.

1. Customer Dataset
Description

This dataset contains customer demographic details, geographic information, and summarized transaction metrics. It supports revenue analysis, segmentation, and customer lifecycle evaluation.

Business Objectives

Identify high-value customers

Evaluate revenue contribution by segment

Track customer acquisition trends

Analyze geographic distribution

Data Dictionary – Customer Dataset
Column Name	Description	Data Type	Business Purpose
customer_id	Unique identifier for each customer	Numeric	Primary key for customer tracking
customer_name	Full name of the customer	Text	Identification
email	Customer email address	Text	Communication
phone	Full phone number including country code	Text	Contact
country_code	Extracted country dialing code	Numeric/Text	Standardization
phone_number	10-digit mobile number	Numeric/Text	Clean contact record
address	Customer residential address	Text	Geographic analysis
area	City/Region name	Text	Regional performance tracking
pincode	Postal code	Numeric	Location accuracy
registration_date	Date customer registered	Date	Acquisition trend analysis
customer_segment	Segment classification (Premium, Regular, New, Inactive)	Text	Targeted marketing
total_orders	Total number of orders placed	Numeric	Frequency analysis
avg_order_value	Average value per order	Numeric	Spending behavior
Derived Metrics

Total Revenue = total_orders × avg_order_value

Revenue by Segment

Average Order Value by Segment

Top Customers by Revenue

2. Customer Feedback Dataset
Description

This dataset captures customer satisfaction ratings, qualitative feedback, categorized issues, and sentiment classification.

Business Objectives

Measure customer satisfaction

Identify service improvement areas

Track complaint categories

Monitor sentiment trends

Data Dictionary – Feedback Dataset
Column Name	Description	Data Type	Business Purpose
feedback_id	Unique feedback identifier	Numeric	Primary key
order_id	Order associated with feedback	Numeric	Transaction linkage
customer_id	Linked customer identifier	Numeric	Customer-level analysis
rating	Numerical rating (1–5)	Numeric	Satisfaction measurement
feedback_text	Customer comment	Text	Qualitative analysis
feedback_category	Type of issue (Delivery, App Experience, Product Quality, Customer Service)	Text	Root cause analysis
sentiment	Derived sentiment label	Text	Satisfaction classification
feedback_date	Date feedback submitted	Date	Trend analysis
Rating Mapping

1 – Bad
2 – Average
3 – Neutral
4 – Very Good
5 – Excellent

Sentiment Buckets

Positive (4–5)

Neutral (3)

Negative (1–2)

Key Metrics

Customer Satisfaction Rate

Sentiment Distribution

Category-wise Complaint Percentage

Monthly Rating Trends

3. Inventory Dataset
Description

This dataset tracks product-level stock intake and damaged stock quantities. It supports quality control and operational efficiency monitoring.

Business Objectives

Reduce damaged inventory

Monitor supplier performance

Improve logistics handling

Track operational loss

Data Dictionary – Inventory Dataset
Column Name	Description	Data Type	Business Purpose
product_id	Unique product identifier	Numeric	Product tracking
date	Stock entry date	Date	Time-based tracking
stock_received	Quantity received	Numeric	Inventory tracking
damaged_stock	Quantity damaged	Numeric	Loss measurement
Derived Metric

Damage Percentage = (damaged_stock / stock_received) × 100

Validation Rule:
damaged_stock must not exceed stock_received

Data Cleaning and Standardization

The following data preparation steps were performed:

Converted text fields to proper case

Cleaned and standardized address formatting

Removed line breaks from address entries

Split phone number into country code and mobile number

Validated phone number format

Standardized sentiment labels based on rating

Flagged invalid inventory records

Created revenue and damage percentage metrics

Dashboard Structure
KPI Overview

Total Customers

Total Revenue

Total Orders

Average Order Value

Customer Satisfaction Rate

Overall Damage Percentage

Customer Analytics

Segment-wise Revenue

Customer Distribution

Top Customers

Registration Trends

Feedback Analysis

Sentiment Distribution

Category-wise Issues

Rating Trends Over Time

Inventory Monitoring

Damage Percentage

High-Damage Products

Stock vs Damaged Comparison

Conclusion

This project demonstrates comprehensive business data analysis across customer performance, service quality, and operational efficiency. By integrating customer behavior insights, structured sentiment analysis, and inventory monitoring, the project provides a holistic view of business performance and supports data-driven strategic decision-making.
Looker:
Dashboard1: https://lookerstudio.google.com/embed/reporting/c0edb5d3-e2f3-47b1-ac47-48a23cd9d900/page/page_12345


Dashboard2: https://lookerstudio.google.com/reporting/f370c2d0-90f4-4ff2-91ab-8a9fc374e4d3/page/page_12345/edit

Dashboard3: https://lookerstudio.google.com/reporting/545b506c-1370-44fc-87d3-7e5c92b3ddb3/page/aNBqF


