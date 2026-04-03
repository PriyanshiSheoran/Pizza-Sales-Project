# 🍕 Pizza Store Sales SQL Project

## 📌 Description
This project analyzes pizza store sales data using SQL to generate valuable insights on revenue, customer demand, and product performance. It demonstrates how raw data can be transformed into meaningful business insights.

## 🔑 Key Highlights
- Revenue and order analysis  
- Top & least selling pizzas  
- Sales trends by time (hour/day)  
- Category & size-wise performance  
- Real-world business insights using SQL  

## 🗄️ Database Used
MySQL / PostgreSQL  

## 🛠️ Tech Stack
- SQL  
- DBMS (MySQL / PostgreSQL)  

## 📊 Key Tables
- orders – stores order date & time  
- order_details – quantity and order info  
- pizzas – pizza size and price  
- pizza_types – pizza name & category  

## 📚 Concepts Used
- JOINS (INNER JOIN)  
- GROUP BY  
- AGGREGATE FUNCTIONS (SUM, COUNT)  
- ORDER BY  
- LIMIT  

## 📥 How to Use
Download or clone this repository.  
Import the dataset into your SQL database.  
Run the queries from the SQL file and analyze results.  

## 💻 Example Query
```sql
SELECT pt.name, SUM(od.quantity) AS total_sold
FROM order_details od
JOIN pizzas p ON od.pizza_id = p.pizza_id
JOIN pizza_types pt ON p.pizza_type_id = pt.pizza_type_id
GROUP BY pt.name
ORDER BY total_sold DESC
LIMIT 5;
