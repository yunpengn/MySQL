# 9. Unique Key

- Performance difference between unique key vs normal index:
    - select query: very minimal difference
    - update query: unique key cannot use change buffer
- redo log reduces cost due to random write on hard disk, change buffer reduces cost due to random read on hard disk.
