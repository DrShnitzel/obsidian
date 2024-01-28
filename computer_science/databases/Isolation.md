
- read uncommitted - highest concurrency. it reads even data that was not yet committed by other transactions leading to [[Dirty read]]
- read committed  - reads only committed data. But does not prevent [[Non-repeatable read]] and [[Phantom read]]
- repeatable read - ensures that data will be the same each read (like having freezing db state by the start of transaction). But still does not prevent [[Phantom read]]
- serializable - transactions are executed one after another synchronously. It is slow but prevents conflicts

In Postgres default is read committed 

```sql
BEGIN;
SET TRANSACTION ISOLATION LEVEL SERIALIZABLE;
-- Your transaction operations here
COMMIT;
```