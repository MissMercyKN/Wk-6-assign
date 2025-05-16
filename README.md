# Wk-6-assign
Question 1 🧑‍💼
Get firstName, lastName, email, and officeCode of all employees using INNER JOIN:

SELECT 
    employees.firstName, 
    employees.lastName, 
    employees.email, 
    employees.officeCode
FROM 
    employees
INNER JOIN 
    offices ON employees.officeCode = offices.officeCode;
Explanation: The INNER JOIN ensures only employees that are assigned to existing offices are returned.


Question 2 🛍️
Get productName, productVendor, and productLine using LEFT JOIN:

SELECT 
    products.productName, 
    products.productVendor, 
    products.productLine
FROM 
    products
LEFT JOIN 
    productlines ON products.productLine = productlines.productLine;
 Explanation: LEFT JOIN ensures all products are returned, even if they don't have a matching entry in the productlines table.


Question 3 📦
Get orderDate, shippedDate, status, and customerNumber for the first 10 orders using RIGHT JOIN:

SELECT 
    orders.orderDate, 
    orders.shippedDate, 
    orders.status, 
    orders.customerNumber
FROM 
    customers
RIGHT JOIN 
    orders ON customers.customerNumber = orders.customerNumber
LIMIT 10;
Explanation: RIGHT JOIN ensures all orders are included, even if the corresponding customer data is missing. The LIMIT 10 returns only the first 10 records.
