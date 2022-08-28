# 11. Index on a `VARCHAR` column

- MySQL supports prefix index on a `VARCHAR` column, such as `ADD INDEX idx_name (col_name(6))`
- A prefix index could save space, but may result in scanning more rows
    - Try to think about cardinality when designing the length of a prefix index
- A prefix index may be no longer a covering index
- MySQL does not support hash index, but one could build hash index at the application layer
