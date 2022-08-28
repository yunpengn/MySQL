# 13. Size of a Table File

- `innodb_file_per_table` determines whether InnoDB stores data for each table in an independent file
- What happens when a row is deleted:
    - InnoDB marks a slot as deleted and ready for reuse, rather than really moving its positions on disk
    - Thus, deleting data too frequently may result in disk fragmentation
- Rebuild a table using `ALTER TABLE ...` could reduce disk fragmentation
- An online DDL must be an in-place operation, an in-place operation may not be online
