# 6. Lock

- MySQL could perform locking on 3 levels:
    - Global lock
    - Table-level lock
    - Row-level lock
- Global lock
    - Could only be triggered with `FLUSH TABLES WITH READ LOCK`
    - Useful when doing system maintainence, such as a full logical backup
    - See https://dev.mysql.com/doc/refman/5.7/en/flush.html
- 
