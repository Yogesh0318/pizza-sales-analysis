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

## Key Questions & SQL Analysis

Below are the main business questions answered with SQL queries:

1. **Total Number of Orders**
```sql
SELECT COUNT(*) AS total_orders
FROM orders;
