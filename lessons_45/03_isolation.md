# 3. Isolation

- Transaction is only supported by the InnoDB storage engine
- Isolation is to solve these problems:
    - Dirty read
    - Non-repeatable read
    - phantom read
- Isolation levels:
    - Read uncommitted
    - Read committed
    - Repeatable read
    - Serializable
- Implementation of isolation:
    - Use **MVCC (multi-version concurrency control)**
    - Achived with the undo tablespaces
    - Undo tablespaces could only be deleted when there is no older read-view
    - See https://dev.mysql.com/doc/refman/8.0/en/innodb-multi-versioning.html
