# 5. Index

- Covering index:
    - Can satisfy all requested columns in a query without performing a further lookup into the clustered index.
- Left-prefix index rule:
    - A query can search an index efficiently if its `WHERE` clause matches the leading columns of the index, in left-to-right order.
- Ordering of columns within a composite index:
    - Try to cover as much query space as possible (think about left-prefix matching)
    - Try to save space (cardinality of each column)
- Index condition pushdown (ICP):
    - An optional optimization feature introduced since MySQL 5.6
    - If parts of the `WHERE` condition can be evaluated by using only columns from the index, the MySQL server pushes this part of the `WHERE` condition down to the storage engine
    - ICP is only used for secondary indexes (since its goal is to reduce full-row reads)
    - See https://dev.mysql.com/doc/refman/5.6/en/index-condition-pushdown-optimization.html
