It is an [[SQL]] statement used to filter individual rows based on specific conditions.

Applied directly to columns in the original table

Executed early in the query process, before [[GROUP BY]] and aggregate functions are calculated

```SQL
SELECT city, COUNT(*) AS user_count
FROM users
WHERE age > 30 -- Filters individual users before grouping
GROUP BY city
HAVING COUNT(*) > 100;
```