
Occurs when data is modified by another transaction during execution of the current transaction.

```sql
T1 START
T1 SELECT name FROM users WHERE id = 1 # JOHN
T2 START
T2 UPDATE users SET name = “JANE” WHERE id = 1
T2 COMMIT
T1 SELECT name FROM users WHERE id = 1 # JANE
```