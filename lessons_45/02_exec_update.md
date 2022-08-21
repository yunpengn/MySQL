# 2. Execution of an update query

- redo log
    - a technique called **WAL (write-ahead logging)**, to ensure MySQL can achieve **crash-safe**
    - changes that did not finish updating the data files before an unexpected shutdown are replayed when the server is up again
    - represented by two files `ib_logfile0` and `ib_logfile1` on disk, writes in a circular fashion
    - only available for InnoDB storage engine
    - See https://dev.mysql.com/doc/refman/5.7/en/innodb-redo-log.html
- binlog
    - useful for replication from master to slave & data recovery point-in-time
    - available since MyISAM storage engine
    - See https://dev.mysql.com/doc/internals/en/binary-log-overview.html
