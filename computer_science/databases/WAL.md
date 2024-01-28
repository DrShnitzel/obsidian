
Whrite Ahead Log is a concept to ensure data integrity. Commonly used in databases and journaled file systems.

Transactions. Durability(persisting data despite system failures) and Consistency(data follow some rules and constrains)

`checkpoints` that mark persisted data

```sql
// Start of Transaction 1
T1 START
T1 UPDATE Accounts 001 Balance 1000 -> 950
T1 UPDATE Accounts 002 Balance 2000 -> 2050
T1 COMMIT

// Start of Transaction 2
T2 START
T2 UPDATE Accounts 003 Balance 1500 -> 1600
T2 COMMIT
```
