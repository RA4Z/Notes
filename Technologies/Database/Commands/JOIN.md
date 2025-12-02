It is an [[SQL]] statement used to combines the result of two or more [[SELECT]] horizontally, based com a shared column ([[Foreign Key]]) or condition. It create new columns in the result set.

Requires a common column ([[Foreign Key]]) or a relationship between the tables to establish the join condition.

```SQL
SELECT Customers.customer_name, Orders.order_id
FROM Customers
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id;
```