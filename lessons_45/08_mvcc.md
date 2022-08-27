# 8. MVCC

- MVCC provides a consistent read view, which achieves RC (read committed) and RR (repeatable read)
- InnoDB assigns an auto-increment transation ID to every transaction when it starts.
    - When the transaction modifies a certain row, a new version of that row is generated and its `trx_id` column is assigned the transaction ID of this current transaction.
    - Physically, InnoDB does not store multiple versions of the same row. Instead, it only stores the latest version and uses undo log to represent its older versions logically.
- With MVCC, a consistent read view makes sure:
    - A value is visible if its `trx_id` is smaller than or equal to the transaction ID of the current transaction
    - A value is invisible if its `trx_id` is greater than the transaction ID of the current transaction (thus need to follow undo log to find its older versions)
