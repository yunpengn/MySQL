# 1. What is Distributed DB?

- Requirements for a distributed DB differs for OLTP vs OLAP scenarios.
- General requirements for OLTP distributed DB:
    - Write heavy
    - Low laency
    - High concurrency
    - High availability
    - Ultra-large amount of data
    - Compatible with relational DB
- Measurements for system availability:
    - Recovery time objective (RTO)
    - Recovery point objective (RPO)
- Common solutions for distributed DB:
    - Client-side proxy
    - Server-side proxy
    - App-layer sharding
