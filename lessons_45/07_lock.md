# 7. Lock

- Two-phase locking (2PL)
    - expanding phase (locks are acquired & no lock is released) + shrinking phase (locks are released & no lock is acquired)
    - guarantees serializability
    - See https://en.wikipedia.org/wiki/Two-phase_locking
- Dead lock
    - Two txns sharing the same resource preventing each other from accessing the resource, resulting in both ceasing to function.
    - In InnoDB, have `innodb_lock_wait_timeout` (by default 50s) + `innodb_deadlock_detect` (could be CPU intensive)
