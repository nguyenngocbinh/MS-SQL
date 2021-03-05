### How do you list the primary key of a SQL Server table?
```()
SELECT Col.Column_Name, Col.Table_Name from 
    INFORMATION_SCHEMA.TABLE_CONSTRAINTS Tab, 
    INFORMATION_SCHEMA.CONSTRAINT_COLUMN_USAGE Col 
WHERE 
    Col.Constraint_Name = Tab.Constraint_Name
    AND Col.Table_Name = Tab.Table_Name
    AND Constraint_Type = 'PRIMARY KEY'
```

### How do you return the column names of a table?
```()
SELECT COLUMN_NAME,* 
FROM INFORMATION_SCHEMA.COLUMNS
WHERE lower(COLUMN_NAME) like '%request%' 
```
