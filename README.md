# week-6-joins-and-relationship
-- Question 1: Retrieve employee details with office information using INNER JOIN
SELECT employees.firstName, employees.lastName, employees.email, employees.officeCode
FROM employees
INNER JOIN offices ON employees.officeCode = offices.officeCode;

-- Question 2: Retrieve product details with product line information using LEFT JOIN
SELECT products.productName, products.productVendor, products.productLine
FROM products
LEFT JOIN productlines ON products.productLine = productlines.productLine;

-- Question 3: Retrieve order details with customer information using RIGHT JOIN
SELECT orders.orderDate, orders.shippedDate, orders.status, orders.customerNumber
FROM customers
RIGHT JOIN orders ON customers.customerNumber = orders.customerNumber
ORDER BY orders.orderDate DESC
LIMIT 10;
