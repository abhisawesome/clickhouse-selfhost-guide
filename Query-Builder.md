## Query for showing size of database

```sql
SELECT
    database,
    table,
    formatReadableSize(sum(bytes)) AS size
FROM system.parts
WHERE active
GROUP BY
    database,
    table
ORDER BY
    size DESC;

```
