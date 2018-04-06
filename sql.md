```SQL 
SHOW CREATE TABLE `table_name`
```
generate create script for table

```SQL
show full columns from `table_name`
```
all info about table structure

```SQL
SHOW TABLE STATUS FROM database_name
```
all info about tables in db (total size = Data_lenght)

```SQL 
SELECT TIMESTAMPDIFF(SECOND,'2011-03-08 12:00:00',CURRENT_TIMESTAMP());
``` 
różnica w sekundach pomiędzy podanym czasem a aktualnym
