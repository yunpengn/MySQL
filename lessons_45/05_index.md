# 5. Index

- Covering index:
    - Can satisfy all requested columns in a query without performing a further lookup into the clustered index.
- Left-prefix index rule:
    - A query can search an index efficiently if its `WHERE` clause matches the leading columns of the index, in left-to-right order.
- 
