# 16. How does `ORDER BY` work

- MySQL has three sort modes:
    - `<sort_key, rowid>`: sort buffer only contains the row_id and does not contain the actual row
    - `<sort_key, additional_fields>`: sort buffer contains all columns referenced by the query
    - `<sort_key, packed_additional_fields>`: sort buffer contains packed version of all columns (use actual length rather than fixed-length encoding)
- See https://dev.mysql.com/doc/refman/8.0/en/order-by-optimization.html
