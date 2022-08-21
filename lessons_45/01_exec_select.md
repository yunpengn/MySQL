# 1. Execution of a select query

- Architecture of MySQL
    - client side: MySQL connectors (in different programming languages) & MySQL shell
    - server layer: SQL parser, SQL optimizer, caches & buffers
    - storage layer: storage engines, file systems, files & logs
- MySQL connectors:
    - Use TCP as the network communication protocol
    - Can use `show processlist;` to see all active connections
    - Connections will be closed after a period of time set by `wait_timeout`
    - Recommended to use long-lived connections to save time on establishing new connections
- SQL query cache
    - Not recommended to use as the cache hit rate is usually low
    - In MySQL 8.0, query cache is completely abandoned
- SQL optimizer
    - Decide join ordering, index usage, etc.
