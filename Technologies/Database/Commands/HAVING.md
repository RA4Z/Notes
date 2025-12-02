It is an [[SQL]] statement used to filter groups of rows based on conditions.

Applied to the results of [[GROUP BY]] and aggregate functions, it must be used in conjunction with a [[GROUP BY]] clause

```SQL
SELECT city, COUNT(*) AS user_count
FROM users
WHERE age > 30
GROUP BY city
HAVING COUNT(*) > 100; -- Filters groups of cities based on the count of users
```