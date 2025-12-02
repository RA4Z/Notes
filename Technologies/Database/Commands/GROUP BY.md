It is an [[SQL]] clause used to group rows that have the same values in specified columns into summary rows.

Organizes the result set into groups based on the unique values in one or more specified columns

```SQL
SELECT country, COUNT(customer_id) AS total_customers
FROM customers
GROUP BY country;
```