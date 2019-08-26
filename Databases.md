###Dababases

A database index is a data structure that improves the speed of operations in a table.
Databases uses indexes  to create and retrieve data from the database very quickly. Using an index to retrieve a portion of rows to perform a count ( * ) is the necessary alteration to overcome a full table scan for your application. Primary key, foreign key, and unique constraints.indexes By default have  indexes. You may want to create "indexes" for other columns that are frequently used in joins or search conditions.
The data is taken from a column in the table and is stored in alphabetical in a separate location called an index. 

Creating Indexes:

CREATE INDEX idx_lastname
ON Employees (lastname);

To create an index on a combination of columns
CREATE INDEX idx_fullname
ON Employees (lastname, firstname);

Partitioning:

Partitioning is a database design technique which is used to improves performance, manageability, simplifies maintenance and reduce the cost of storing large amounts of data. With partitioning queries that access only a fraction of the data can run faster because there are fewer data to scan.

Partitioning methods

Horizontal partitioning
Horizontal partitioning divides a table into multiple tables. Each table then contains the same number of columns, but fewer rows.
Vertical Partitioning
Vertical partitioning involves creating tables with fewer columns and using additional tables to store the remaining columns

Partitioning criteria

* Range partitioning
* List partitioning
* Composite partitioning
* Round-robin partitioning
* Hash partitioning

Creating partition on a table

Suppose that we have a MySQL table with the following schema
```CREATE TABLE `Employee` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `firstname` varchar(50) DEFAULT NULL,
`lastname` varchar(50) DEFAULT NULL,
 `email` varchar(100) DEFAULT NULL,
 `created` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
 PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1```


Range partitioning
A table that is partitioned by range is partitioned in such a way that each partition contains rows for which the partitioning expression value lies within a given range. Ranges should be contiguous but not overlapping and are defined using the VALUES LESS THAN operator.
 
```ALTER TABLE Employees  PARTITION BY RANGE (id)
  (
    PARTITION p1 VALUES LESS THAN (100),
    PARTITION p2 VALUES LESS THAN (200), 
    PARTITION p3 VALUES LESS THAN (300),  
    PARTITION p4 VALUES LESS THAN (400),
    PARTITION p5 VALUES LESS THAN (500),
    PARTITION p6 VALUES LESS THAN (600)
    PARTITION p7 VALUES LESS THAN MAXVALUE 
  );
```
striping:


clustering:

clustering is a technology that allows distributing the database across multiple independent nodes, to eliminate every possibility of failure thus providing high availability and low latency. It allows for almost infinite scaling of your MySQL-based website or application, which can be done horizontally, i.e. with very inexpensive machines. and low latency
