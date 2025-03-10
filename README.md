# SQL Project Portfolio

## Project Overview

This SQL project demonstrates various techniques and queries used to analyze and extract useful business insights from an e-commerce/order management database. The project includes working with data from `orders`, `customers`, `restaurants`, and `deliveries` tables. The objective of the project is to create meaningful reports, track key metrics, and generate rankings based on different criteria like total order count, average order value (AOV), and more.

### Key Highlights:
- Data extraction and transformation techniques.
- Ranking and aggregation to analyze the best-performing restaurants and customers.
- Customer activity tracking and reporting.
- Time slot analysis of order frequency.
- Advanced SQL functions, including `RANK()`, `EXTRACT()`, and `CASE` statements.

## Table of Contents
1. [Top 5 Most Ordered Items](#top-5-most-ordered-items)
2. [Customer-Specific Order Statistics](#customer-specific-order-statistics)
3. [Order Frequency by Time Slot](#order-frequency-by-time-slot)
4. [Order Aggregation by 2-Hour Intervals](#order-aggregation-by-2-hour-intervals)
5. [Customer Average Order Value](#customer-average-order-value)
6. [High-Spending Customers](#high-spending-customers)
7. [Unfulfilled Deliveries](#unfulfilled-deliveries)
8. [Restaurant Revenue Ranking](#restaurant-revenue-ranking)
9. [Dish Popularity in Different Cities](#dish-popularity-in-different-cities)
10. [Customers Who Ordered in 2023 but Not in 2024](#customers-who-ordered-in-2023-but-not-in-2024)

---

### Top 5 Most Ordered Items
The following query provides the top 5 most ordered items across all customers.

```sql
SELECT count(order_item) AS ordered, order_item
FROM public.orders
GROUP BY order_item
ORDER BY ordered DESC
LIMIT 5;


# Database Schema
The following tables are part of the database:

orders: Contains order details, including order_id, customer_id, restaurant_id, order_item, total_amount, order_time, and order_date.
customers: Contains customer details such as customer_id, customer_name, and email.
restaurants: Contains restaurant details such as restaurant_id, restaurant_name, and city.
deliveries: Contains delivery-related details such as order_id and delivery_status.
Conclusion
This SQL project showcases the ability to write complex queries, including aggregations, joins, and ranking, to generate meaningful insights from an e-commerce/order management database. The insights provided by the queries can be utilized by businesses to understand customer behavior, identify high-performing products and restaurants, and track delivery efficiency.

Contact Information
Feel free to contact me at your.email@example.com for further inquiries or collaboration opportunities.