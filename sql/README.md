## 🗄️ SQL Analysis

SQL was used to understand the dataset and perform initial analysis.

📌 Key operations:
- Data exploration using SELECT queries  
- Joining multiple tables (orders, customers, payments)  
- Aggregating customer transactions  

👉 Example:

```sql
SELECT customer_id, COUNT(order_id) AS frequency, SUM(payment_value) AS monetary
FROM orders
JOIN payments USING(order_id)
GROUP BY customer_id;
