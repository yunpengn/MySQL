# 6. Lock

- MySQL could perform locking on 3 levels:
    - Global lock
    - Table-level lock
    - Row-level lock
- Global lock
    - Could only be triggered with `FLUSH TABLES WITH READ LOCK`
    - Useful when doing system maintainence, such as a full logical backup
    - Only applicable for MyISAM, since you can do a backup on InnoDB with a repeatable-read transaction easily
    - See https://dev.mysql.com/doc/refman/5.7/en/flush.html
- Table-level lock
    - Table lock: useful for concurrency control on non-InnoDB table
    - Metadata lock (MDL): automatically applied to avoid unexpected behaviour due to concurrent DDL statements
