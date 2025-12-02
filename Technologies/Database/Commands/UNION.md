It is an [[SQL]] statement used to combines the result of two or more [[SELECT]] statements vertically, expanding the dataset by adding rows.

Requires that all [[SELECT]] statement within the UNION operation have the same number of columns, and that columns need to have compatible data types and in the same order.

```SQL
SELECT employee_name, 'Employee' AS role
FROM Employees
UNION
SELECT contractor_name, 'Contractor' AS role
FROM Contractors;
```
