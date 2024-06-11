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

## Query for showing size of tables

```sql
SELECT
    table,
    formatReadableSize(sum(bytes)) AS size
FROM system.parts
WHERE active
    AND database = 'YOUR_DATABSE_NAME'
GROUP BY
    table
ORDER BY
    size DESC;
```
