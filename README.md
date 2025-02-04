# FastAPI SQL Assignment

This assignment is designed to help you practice writing SQL queries with increasing complexity using a retail database schema. You'll be working with customer orders, products, and sales data.

## Setup

1. Make sure you have Docker and Docker Compose installed on your system.

2. Clone this repository:

3. Start the application:
```bash
docker-compose up --build
```

4. Initialize the database by visiting:
```
http://localhost:8000/initdb
```

5. Access the dashboard at:
```
http://localhost:8000
```

## Assignment Tasks

### Assignment 1: Basic JOIN Query
Implement a query to find the top 10 customers who have spent the most money. The query should return:
- Customer name
- Customer email
- Total amount spent

### Assignment 2: GROUP BY Query
Implement a query to calculate sales metrics by product category, including:
- Category name
- Total number of orders
- Total revenue
- Average order value

### Assignment 3: Complex JOIN with GROUP BY
Implement a query to analyze customer purchasing patterns by membership level and city, showing:
- Membership level
- City
- Total orders
- Average order value
- Number of customers
- Orders per customer

### Assignment 4: Subquery and Advanced Analytics
Implement a query to find products that are performing above average in their category, showing:
- Product name
- Category
- Total sales
- Category average
- Percentage above average

## Implementation

1. Open `app/main.py`
2. Implement the four assignment route handlers:
   - `/assignment1`
   - `/assignment2`
   - `/assignment3`
   - `/assignment4`

Each handler should return a JSON response with a "data" key containing the query results.

## Database Schema

### Customers
- customer_id (PK)
- name
- email
- city
- membership_level
- join_date

### Orders
- order_id (PK)
- customer_id (FK)
- order_date
- total_amount
- status

### Products
- product_id (PK)
- name
- category
- price

### Order_Items
- order_id (FK)
- product_id (FK)
- quantity
- unit_price

## Tips

- Use appropriate JOIN types (INNER, LEFT, RIGHT) based on the requirements
- Pay attention to NULL handling
- Use appropriate aggregate functions
- Consider using window functions for advanced analytics 
