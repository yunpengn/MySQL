# 14. Why is `COUNT *` slow

- Time complexity of `SELECT COUNT(*) FROM tbl_name`:
    - In MyISAM, it is O(1) since the # of rows in a table is stored as a table metadata
    - In InnoDB, it is still O(n) since it needs to scan the whole table
- The choice that InnoDB makes is a wise one because:
    - With MVCC, it is hard to give a precise answer on the # of rows that exist in a table
    - Maintaining a global counter can be pretty expensive
- It is preferred to maintain a global counter in other caching solutions, such as Redis
