
Situation when one transaction reads data that wasn’t yet committed by other transaction. It can lead to corrupted or inconsistent data in db

1. Transaction A starts
2. Transaction B starts
3. A reads data not committed by B
4. A commit it’s changes
5. B rolls back
6. Now A committed  changes based on non-existing data