# pizza-sales-analysis
# 🍕 Pizza Sales Analysis

## Project Overview
The **Pizza Sales Analysis** project aims to extract actionable insights from pizza sales data. By analyzing orders, revenue, and customer preferences, this project helps answer key business questions, such as:

- Which pizzas generate the most revenue?
- What are the peak ordering hours?
- Which pizza categories and sizes are most popular?

This analysis can support decision-making for inventory management, marketing strategies, and menu optimization.

---

## Database Schema

The database consists of three main tables:

### 1. `orders`
| Column      | Type     | Description                        |
|------------|----------|------------------------------------|
| order_id   | INT      | Unique order identifier             |
| order_date | DATE     | Date when the order was placed      |
| order_time | TIME     | Time when the order was placed      |

### 2. `order_items`
| Column    | Type     | Description                           |
|-----------|----------|---------------------------------------|
| order_id  | INT      | References `orders(order_id)`          |
| pizza_id  | INT      | References `pizzas(pizza_id)`         |
| quantity  | INT      | Number of pizzas in the order         |
| size      | VARCHAR  | Size of pizza (Small, Medium, Large) |

### 3. `pizzas`
| Column     | Type     | Description                        |
|------------|----------|------------------------------------|
| pizza_id   | INT      | Unique pizza identifier             |
| name       | VARCHAR  | Pizza name                          |
| category   | VARCHAR  | Category (Veg/Non-Veg)             |
| price      | DECIMAL  | Price of a single pizza             |


---



---

## ❓ Business Questions Answered

1. Retrieve the total number of orders placed.  
2. Calculate the total revenue generated from pizza sales.  
3. Identify the highest-priced pizza.  
4. Find the most common pizza size ordered.  
5. List the top 5 most ordered pizza types along with their quantities.  
6. Join necessary tables to find the total quantity of each pizza category ordered.  
7. Determine the distribution of orders by hour of the day.  
8. Find the category-wise contribution to total revenue.  
9. List the top 3 most ordered pizza types based on revenue.  
10. Analyze the average order value.

---


