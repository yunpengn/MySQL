# 12. Spike

- Possible reasons for a spike in the latency of SQL queries:
    - When the DB is trying to flush the dirty pages to hard disk
    - When the buffer pool is not enough
    - When the DB is free and tries to flush dirty pages
- Parameters related to flushing dirty pages:
    - `innodb_io_capacity`: the capacity of the disk, usually set to the IOPS of the hard disk
    - `innodb_max_dirty_pages_pct`: the percentage of maximum dirty pages
    - `innodb_flush_neighbors`: whether to flush neighbouring pages together with the current page
