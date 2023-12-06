# Constraints

[Back to Top Page](../SQL/00_index.md)

## Check

```SQL
SELECT conname, pg_get_constraintdef(oid)
  FROM pg_constraint
 WHERE conrelid = 'table_name'::regclass AND contype = 'p';
```

## Add

```SQL
ALTER TABLE table_name
  ADD CONSTRAINT constraint_name PRIMARY KEY (column1, column2, ...);
```

## Delete(Drop)

```SQL
ALTER TABLE table_name
 DROP CONSTRAINT constraint_name;
```
