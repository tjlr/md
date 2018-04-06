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
CREATE TABLE IF NOT EXISTS dbDest.tblDest SELECT * FROM dbSrc.tblSrc;
```
kopia tabeli

```SQL 
SELECT TIMESTAMPDIFF(SECOND,'2011-03-08 12:00:00',CURRENT_TIMESTAMP());
``` 
różnica w sekundach pomiędzy podanym czasem a aktualnym


//---------------------------
```SQL
SHOW TABLE STATUS FROM bcg4 WHERE `Engine` <> ""; -- bez widoków
SHOW CREATE TABLE `table_name`;
show full columns from `table_name`;

show full columns from `table_name`;
select * from notes order by lastmod desc limit 10;

select * from information_schema.PARAMETERS where SPECIFIC_NAME = "sp_name" -- procedure parameters
select * from information_schema.ROUTINES -- procedures list
select ROUTINE_BODY from information_schema.ROUTINES where ROUTINE_NAME = "sp_name"
SHOW CREATE PROCEDURE sp_name -- procedure body
select * from information_schema.VIEWS -- views list
SHOW CREATE VIEW view_name -- view body
select * from information_schema.COLUMNS --
```
