# Olist E-Commerce Performance Analysis

An analysis of the Olist Brazilian e-commerce dataset to answer three business
questions around customer value, delivery performance, and revenue drivers,
using SQL, Python, and Power BI.

## Dataset

[Olist Brazilian E-Commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
(Kaggle)- 100k orders across customers, orders, order items, payments,
reviews, products, and sellers tables.

## Tools Used

- **Python (pandas)** — data loading and manipulation
- **SQL (SQLite)** — querying and aggregation
- **Power BI** — dashboard and visualization

## Business Questions & Key Findings

### 1. Are repeat customers more valuable than one-time buyers?
Only about 5.9% of customers are repeat buyers, but they spend **$239.46**
on average per customer. Meanwhile, one time buyers spend $160.58 on average.
Repeat buyers spend about 49% more on average.
This business depends heavily on one-time purchases. So, even a small increase 
in repeat-purchase rate could grow revenue. 
This can be done through retention efforts like email follow-ups and loyalty incentives.

### 2. Does delivery time affect customer satisfaction?
There is an inverse relationship between delivery time and review score.
The orders with a 5-star review took an average of 10.7 days to deliver, while
1-star reviews took nearly twice as long at 21.3 days. 
Delivery time seems to impact customer satisfaction a lot.
Investment in faster and reliable shipping could directly improve review scores 
and customer retention.

### 3. Which product categories generate the most revenue?
**Health & beauty** is the top revenue category (**$1.23M**),
ahead of **watches/gifts** (**$1.17M**) despite watches/gifts having far
less orders. This implies a higher average order value per purchase. 
Bed/bath/table has the highest order count (9,272)
but lower revenue, suggesting a lower-priced, higher-volume category. 
This suggests different strategies to increase revenue like: 
health & beauty may benefit from volume-driven promotions, while
watches/gifts could be leaned into as a premium, higher-margin category.

## Data Cleaning 

- Filtered to orders with `order_status = 'delivered'` to exclude
  canceled or unavailable orders from revenue and delivery analysis.
- Excluded orders with a missing delivery date from delivery-time analysis

## Dashboard

![Dashboard](dashboard.png)

## Project Structure
```
├── 01_data_ingestion.ipynb      
├── 03_business_analysis.ipynb   
├── dashboard.png                
├── q1_repeat_customers.csv
├── q2_delivery_vs_review.csv
├── q3_top_categories.csv
└── README.md
```
