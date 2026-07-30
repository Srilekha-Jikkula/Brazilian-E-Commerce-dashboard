# Brazilian E-Commerce Dashboard Analysis.
# End to End Data Analysis Project using Power BI.
## Project OverView
This project focuses on analyzing BrazilianE-commerce saes data to uncover valuable business insights. The dashboard was built using Power BI to help stakeholders understand sales performance,Customer behaviour, deivery trends, and payment preferences.
The goal of this project is to transform raw transactional data into meaningful visual insights that support data-driven decision-Making.
## Dashboard Objective
Anayze overall sales performance
Identify top- Performing product categories
Understand customer distribution across states
Evalte delivery performance 
Study payment method preferences
Track monthly sales trends
## Tools & Technologies Used
Power BI - Data visualization and dashboard creation
Power Query
## Dataset Information
The dataset used in this project is the Brazilian E-commerce public Dataset.
It contains information about:
1.Customers
2.Geolocation
3.Order-items
4.Order_Payments
5.Order_reviews
6.Orders
7.Products
8.Sellers
9.Product_category_name_translation
The dataset includes more than 100000 e-commerce transactions across Brazil.
## Business Questions Addressed
1. Which product categories generate the highest revenue?
2. Which states contribute the most to sales?
3. What are the monthly sales trends?
4. What is the average delivery time?
5. Which payment methods are most frequently used?
## Measures Created
### 1.Total Orders
Total Orders = DISTINCTCOUNT(olist_orders_dataset[order_id])
### 2.Total Customers
Total Customers = DISTINCTCOUNT(olist_customers_dataset[customer_id])
### 3.Average Review
Avg Review = AVERAGE(olist_order_reviews_dataset[review_score])
### 4.Average Order Value
Average Order Value = DIVIDE([Total Sales],[Total Orders],0)
### 5.Total Sales
Total Sales = SUM(olist_order_items_dataset[Total Price])
### 6.Total Products
Total Products = DISTINCTCOUNT(olist_products_dataset[product_id])
### 7. Average Delivery Days
Avg Delivery Days = AVERAGE(olist_orders_dataset[Delivery Days])
### 8.Total Payment
Total Payment = SUM(olist_order_payments_dataset[payment_value])
### 9.Cancelled Orders
Cancelled Orders = 
CALCULATE(
    COUNTROWS(olist_orders_dataset),
    olist_orders_dataset[order_status] = "canceled"
)
### 10. Cancellation rate %
Cancellation Rate % = 
DIVIDE(
    [Cancelled Orders],
    [Total Orders],
    0
)
## Key Performance Indicators (KPIs)
1.Total Revenue
2.Total Orders
3.Total Customers
4.Average Delivery Time
5.Customer Review Score
6.Monthly Sales Growth
## Dashboard Insights
1.São Paulo contributes the highest number of orders and revenue.
2.Credit card is the most preferred payment method among customers.
3.Sales show noticeable spikes during festive and holiday seasons.
4.Faster delivery times tend to result in higher customer review scores.
## Dashboard Preview

(Add your Power BI dashboard screenshot here)

Example:
## Project Outcome

This dashboard enables businesses to monitor important sales metrics, identify high-performing regions and categories, and improve operational efficiency using data insights.

## Author
Jikkula Srilekha
Aspiring Data Analyst
Skills: SQL | Power BI | Excel | Python | Dada visualization | Data Modeling | Dashboard management
