# SQL Core: Interview questions

1. **Database Design:**

   - **Question:** Explain the process of normalization and its importance in database design.

     - **Answer:** Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity. It involves breaking down tables into smaller, related tables to eliminate duplicate data. The goal is to minimize data anomalies and ensure that data is stored efficiently.

   - **Question:** What is denormalization, and in what scenarios would you consider using it?

     - **Answer:** Denormalization is the process of combining tables to reduce the number of joins needed for queries, sacrificing some aspects of data integrity for improved query performance. It is often considered in scenarios where read performance is crucial, and the system can tolerate a certain level of data redundancy.

   - **Question:** Describe the differences between a primary key and a foreign key.
     - **Answer:** A primary key is a unique identifier for a record in a table, ensuring data integrity and providing a way to establish relationships with other tables. A foreign key, on the other hand, is a field in a table that refers to the primary key in another table, creating a link between the two tables.

2. **SQL Queries:**

   - **Question:** Write a SQL query to retrieve the second highest salary from an "Employee" table.

     - **Answer:**
       ```sql
       SELECT MAX(salary)
       FROM Employee
       WHERE salary < (SELECT MAX(salary) FROM Employee);
       ```

   - **Question:** Explain the differences between INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN.

     - **Answer:**
       - INNER JOIN returns rows where there is a match in both tables.
       - LEFT JOIN returns all rows from the left table and the matched rows from the right table.
       - RIGHT JOIN is similar but reversed.
       - FULL OUTER JOIN returns all rows when there is a match in either table.

   - **Question:** Write a query to find duplicate records in a table.
     - **Answer:**
       ```sql
       SELECT column_name, COUNT(*)
       FROM table_name
       GROUP BY column_name
       HAVING COUNT(*) > 1;
       ```

3. **Performance Optimization:**

   - **Question:** How would you optimize a slow-performing SQL query?

     - **Answer:** Strategies include indexing, optimizing the query structure, using proper data types, and denormalization in some cases.

   - **Question:** Explain the purpose of database indexes and how they impact query performance.

     - **Answer:** Indexes improve query performance by providing a quick lookup of data. They are created on columns used in WHERE, JOIN, and ORDER BY clauses.

   - **Question:** What is query optimization, and how can it be achieved in SQL?
     - **Answer:** Query optimization involves analyzing and modifying queries to improve efficiency. Techniques include proper indexing, rewriting queries, and using EXPLAIN plans.

4. **Advanced SQL Concepts:**

   - **Question:** What is a stored procedure, and how is it different from a function?

     - **Answer:** A stored procedure is a precompiled set of one or more SQL statements that can be executed by calling the procedure. It can take parameters and return values.

   - **Question:** Explain the use of the GROUP BY and HAVING clauses in SQL.

     - **Answer:** GROUP BY groups rows that have the same values in specified columns, and HAVING filters the results of a GROUP BY based on a specified condition.

   - **Question:** Write a query to pivot data in SQL.
     - **Answer:** Pivoting involves transforming rows into columns. An example is using the CASE statement to create a pivot table.

5. **Transactions and Concurrency:**

   - **Question:** What is a transaction, and why is it important in database systems?

     - **Answer:** A transaction is a sequence of one or more SQL statements executed as a single unit. It follows the ACID properties (Atomicity, Consistency, Isolation, Durability).

   - **Question:** Explain the concepts of ACID properties in the context of database transactions.

     - **Answer:** Atomicity ensures that a transaction is treated as a single, indivisible unit; Consistency ensures that the database remains in a consistent state before and after the transaction; Isolation ensures transactions are independent of each other; Durability ensures that the changes made by a committed transaction are permanent.

   - **Question:** How do you handle concurrent transactions and ensure data consistency?
     - **Answer:** Techniques include locking mechanisms (pessimistic or optimistic) and isolation levels.

6. **Subqueries and Joins:**

   - **Question:** What is a subquery, and how is it different from a JOIN?

     - **Answer:** A subquery is a query nested inside another query. It can be used in SELECT, FROM, WHERE, and HAVING clauses.

   - **Question:** Write a query that uses a subquery to find records that meet a specific condition.

     - **Answer:**
       ```sql
       SELECT column_name
       FROM table_name
       WHERE column_name = (SELECT MAX(column_name) FROM table_name);
       ```

   - **Question:** Explain the concept of a self-join and provide an example.
     - **Answer:** A self-join occurs when a table is joined with itself. It is useful when working with hierarchical data.

7. **Data Modeling:**

   - **Question:** What is an Entity-Relationship Diagram (ERD), and how is it used in database design?

     - **Answer:** An Entity-Relationship Diagram is a visual representation of entities and the relationships between them in a database.

   - **Question:** Describe the differences between a star schema and a snowflake schema.

     - **Answer:** A star schema has a central fact table connected to dimension tables directly, while a snowflake schema normalizes dimension tables by breaking them into multiple related tables.

   - **Question:** How do you handle hierarchical data in a relational database?
     - **Answer:** Techniques include using parent-child tables or a nested set model.

8. **Security and Permissions:**

   - **Question:** Explain the importance of SQL injection prevention and how it can be mitigated.

     - **Answer:** Use parameterized queries or prepared statements to prevent SQL injection attacks.

   - **Question:** How do you grant and revoke permissions in SQL?

     - **Answer:** GRANT is used to give specific privileges to a user, and REVOKE is used to take them away.

   - **Question:** Describe the role of views in database security.
     - **Answer:** Views can limit access to specific columns or rows, providing an additional layer of security.
