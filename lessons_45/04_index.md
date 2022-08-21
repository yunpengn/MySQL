# 4. Index

- Data structures for index
    - Hash map: good for unique key equality search
    - Sorted list: good for unique key equality search & range search, but very expensive for writes
    - Search tree: balanced between reads and writes, such as **B+ tree** and **LSM tree** and **skip-list**
- InnoDB only uses **B+ tree** for index
    - clusted index for primary key, non-clusted index for secondary keys
    - related to the size of each data page on disk
- Recommended to use `BIGINT UNSIGNED NOT NULL PRIMARY KEY AUTO_INCREMENT` as primary key:
    - Sequential insert to the tail of the B+ tree, minimal changes to existing nodes
    - Smallest representation of unique identifiers, save index space
