0x00. MySQL advanced

1. Creating Tables with Constraints:
When you design a database, you want to ensure data integrity, and one way to achieve this is by using constraints. Constraints are rules that dictate the kind of data that can be inserted, updated, or deleted in a table. In MySQL, you can create tables with constraints using the CREATE TABLE statement. Here are some common constraints:

Primary Key:

Ensures uniqueness of each record in a table.
Example:
sql
Copy code
CREATE TABLE users (
    user_id INT PRIMARY KEY,
    username VARCHAR(50) NOT NULL
);
Foreign Key:

Establishes a link between two tables, ensuring referential integrity.
Example:
sql
Copy code
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    user_id INT,
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);
Check Constraint:

Defines a condition that must be true for each row.
Example:
sql
Copy code
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    price DECIMAL(10,2) CHECK (price > 0)
);
2. Optimizing Queries by Adding Indexes:
Indexes are structures that help to improve the speed of data retrieval operations on a database. They work similarly to the index in a book, allowing the database engine to find data faster. Common types include:

Single-Column Index:

Index on a single column.
Example:
sql
Copy code
CREATE INDEX idx_lastname ON employees (last_name);
Composite Index:

Index on multiple columns.
Example:
sql
Copy code
CREATE INDEX idx_name_dept ON employees (last_name, department_id);
Unique Index:

Ensures the uniqueness of values in the indexed columns.
Example:
sql
Copy code
CREATE UNIQUE INDEX idx_username ON users (username);
3. Stored Procedures and Functions in MySQL:
Stored procedures and functions are precompiled and stored in the database for reuse. They help improve code modularity, security, and performance.

Stored Procedure:

A set of SQL statements that can be executed together.
Example:
sql
Copy code
DELIMITER //
CREATE PROCEDURE GetEmployee(IN employee_id INT)
BEGIN
    SELECT * FROM employees WHERE id = employee_id;
END //
DELIMITER ;
Function:

A function returns a value and can be used in SQL queries.
Example:
sql
Copy code
DELIMITER //
CREATE FUNCTION CalculateTax(IN salary DECIMAL(10,2)) RETURNS DECIMAL(10,2)
BEGIN
    RETURN salary * 0.1;
END //
DELIMITER ;
4. Views in MySQL:
A view is a virtual table based on the result of a SELECT query. It simplifies complex queries and provides a layer of abstraction.

Creating a View:

Example:
sql
Copy code
CREATE VIEW high_salary_employees AS
SELECT * FROM employees WHERE salary > 50000;
Using a View:

Once created, you can query it like a regular table.
sql
Copy code
SELECT * FROM high_salary_employees;
5. Triggers in MySQL:
Triggers are special types of stored procedures that are automatically executed (or "triggered") in response to certain events.

Creating a Trigger:
Example:

sql
Copy code
CREATE TRIGGER before_insert_employee
BEFORE INSERT ON employees
FOR EACH ROW
SET NEW.join_date = NOW();
This trigger sets the join_date to the current timestamp before inserting a new employee.
