# 10. Choose an Index

- MySQL supports the syntax of `FORCE INDEX` and `USE INDEX`
- Query optimizer decides which index to use based on # of rows scanned, tmp table, sorting, etc.
- Query optimizer estimates based on catalog data, such as cardinality of a column
    - `innodb_stats_persistent` decides how to build catalog data
    - `ANALYSE TABLE tbl_name` could trigger to re-build catalog data
