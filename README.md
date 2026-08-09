# Brazilian E-Commerce Sales Dashboard Analysis.
# End to End Data Analysis Project using Power BI.

## Project Introduction:

The Brazilian E-Commerce Analytics project is an end-to-end Power BI data analytics project developed to analyze the sales performance, customer behavior, order fulfillment, product performance, and delivery experience of an online marketplace in Brazil.

The project uses the Brazilian E-Commerce Public Dataset by Olist, which contains information related to customers, orders, order items, payments, products, sellers, reviews, and product categories. The dataset provides a real-world view of an e-commerce business and allows different aspects of the customer and order journey to be analyzed together.

The primary objective of this project is to transform raw transactional data into meaningful business insights through data cleaning, transformation, data modeling, DAX calculations, KPI development, and interactive visualization using Microsoft Power BI.

The analysis focuses on key business areas such as:

Overall revenue and order performance.

Average Order Value (AOV).

Revenue contribution by product category.

Sales performance across Brazilian states and cities.

Order status and fulfillment performance.

Customer review scores and satisfaction.

Delivery performance and delivery duration.

Relationship between delivery experience and customer ratings.

Identification of high-performing and low-performing regions and categories.

The project follows a complete data analytics workflow, starting from raw datasets and progressing through data preparation, modeling, calculation, visualization, and business interpretation.

## Dashboard Objective:
The main objective is to build an interactive business intelligence dashboard that enables stakeholders to monitor e-commerce performance, identify important trends and patterns, evaluate customer experience, and support data-driven business decisions.

Rather than focusing only on creating visualizations, the project emphasizes the complete analytical process — understanding the business problem, preparing the data, creating a reliable data model, developing meaningful KPIs, analyzing trends, and converting the results into actionable business insights.

## Tools & Technologies Used:
__Power BI__ - Dashboard development and data visualization.

__Power Query__ - Data cleaning and transformation.

__DAX__ – Calculated measures and analytical calculations.

__Data Modeling__ – Relationships between transactional and dimensional data.

__Olist Brazilian E-Commerce Dataset__ – Source data.

## Dataset Information:
The major tables used in the project include:

__Orders__ – Contains order-level information such as order ID, customer ID, order status, and order timestamps.

__Order Items__ – Contains individual items purchased within each order, including product, seller, price, and freight information.

__Order Payments__ – Contains payment-related information such as payment type, payment installments, and payment value.

__Order Reviews__ – Contains customer review scores and review-related information.

__Products__ – Contains product-level attributes and product category information.

__Customers__ – Contains customer information including customer ID and customer location.

__Sellers__ – Contains seller information and seller location.

__Product Category Translation__ – Provides English translations for product category names.

The dataset includes more than 100000 e-commerce transactions across Brazil.
## Business Questions Addressed
1. Which product categories generate the highest revenue?
2. Which states contribute the most to sales?
3. What are the monthly sales trends?
4. What is the average delivery time?
5. Which payment methods are most frequently used?
## Measures Created
#### 1.Total Orders
Total Orders = DISTINCTCOUNT(olist_orders_dataset[order_id])
#### 2.Total Customers
Total Customers = DISTINCTCOUNT(olist_customers_dataset[customer_id])
#### 3.Average Review
Avg Review = AVERAGE(olist_order_reviews_dataset[review_score])
#### 4.Average Order Value
Average Order Value = DIVIDE([Total Sales],[Total Orders],0)
#### 5.Total Sales
Total Sales = SUM(olist_order_items_dataset[Total Price])
#### 6.Total Products
Total Products = DISTINCTCOUNT(olist_products_dataset[product_id])
#### 7. Average Delivery Days
Avg Delivery Days = AVERAGE(olist_orders_dataset[Delivery Days])
#### 8.Total Revenue
Total Payment = SUM(olist_order_payments_dataset[payment_value])
#### 9.Cancelled Orders
Cancelled Orders = 
CALCULATE(
    COUNTROWS(olist_orders_dataset),
    olist_orders_dataset[order_status] = "canceled"
)
#### 10. Cancellation rate %
Cancellation Rate % = 
DIVIDE(
    [Cancelled Orders],
    [Total Orders],
    0
)
## Key Performance Indicators (KPIs)
#### 1.Total Revenue
Total Revenue = SUM(olist_order_payments_dataset[payment_value])
#### 2.Total Orders
Total Orders = DISTINCTCOUNT(olist_orders_dataset[order_id])
#### 3.Total Products
Total Products = DISTINCTCOUNT(olist_products_dataset[product_id])
#### 4.Average Order Value
Average Order Value = DIVIDE([Total Sales],[Total Orders],0)
#### 5.Average Review
Avg Review = AVERAGE(olist_order_reviews_dataset[review_score])
#### 6.Cancellation rate %
Cancellation Rate % = 
DIVIDE(
    [Cancelled Orders],
    [Total Orders],
    0
)
## Visualizations
##### 1. Scatter chart
Customer Rating VS Delivery Days
#### 2.Donut chart 
Payment Method Distribution
#### 3. Combo chart(Line chart + Clustered Column Chart)
Delivery Performance by Month
#### 4.Donut Chart
Order Status

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
