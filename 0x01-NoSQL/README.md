0x01. NoSQL
What NoSQL means:
"NoSQL" stands for "Not Only SQL." It is a term used to describe a category of database systems that do not strictly adhere to the traditional relational database management system (RDBMS) model. NoSQL databases are designed to handle large volumes of unstructured or semi-structured data, providing flexibility and scalability that may be challenging for traditional SQL databases.

Difference between SQL and NoSQL:
Data Structure:

SQL: Relational databases use a structured schema with predefined tables and relationships.
NoSQL: NoSQL databases can handle unstructured, semi-structured, or structured data, and the schema can be dynamic, allowing for more flexibility.
Scalability:

SQL: Scaling a relational database can be complex, often requiring vertical scaling (upgrading hardware).
NoSQL: NoSQL databases are designed to scale horizontally, making it easier to handle large amounts of data by adding more servers to the database.
Query Language:

SQL: SQL databases use the SQL query language for defining and manipulating the data.
NoSQL: NoSQL databases use various query languages or APIs, and the structure of the data often influences how it's queried.
ACID:
ACID is an acronym that represents the following properties in database transactions:

Atomicity: Transactions are treated as a single, indivisible unit of work. Either all changes are committed, or none are.

Consistency: A transaction brings the database from one valid state to another. It ensures that the integrity constraints of the database are not violated.

Isolation: Transactions are isolated from each other until they are completed. The intermediate state of a transaction is not visible to other transactions.

Durability: Once a transaction is committed, its changes are permanent and survive any subsequent failures.

Document Storage:
Document storage is a type of NoSQL database model where data is stored in flexible, semi-structured documents (e.g., JSON, BSON). Each document can have a different structure, and the data can be nested. Document stores are highly scalable and suitable for scenarios where the data is naturally hierarchical.

NoSQL Types:
There are various types of NoSQL databases, including:

Document Stores: MongoDB, CouchDB
Key-Value Stores: Redis, DynamoDB
Column-family Stores: Cassandra, HBase
Graph Databases: Neo4j, Amazon Neptune
Benefits of a NoSQL Database:
Scalability: Easily scales horizontally to handle increased data and traffic.
Flexibility: Accommodates diverse data types and structures.
Performance: Provides high performance for certain types of queries.
Schema-less Design: Allows dynamic and evolving data models.
Querying, Inserting, Updating, and Deleting in a NoSQL Database:
The specific syntax and methods depend on the NoSQL database type. Generally:

Querying: Typically involves using a query language or API specific to the database. For example, MongoDB uses a query language similar to JSON.
Inserting/Updating/Deleting: Operations are often performed using specific methods or commands provided by the database.
How to Use MongoDB:
MongoDB is a popular document-oriented NoSQL database. Here's a brief overview:
