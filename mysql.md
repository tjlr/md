### dump
```c
mysqldump baza > /path/file.sql -p
```

```sql
mysqldump baza -u root -p -r /path/file.sql
```

### bulk load
**sql**
```sql
LOAD DATA INFILE 'data.txt' INTO TABLE tbl_name
  FIELDS TERMINATED BY ',' ENCLOSED BY '"'
  LINES TERMINATED BY '\n';
```

**data.txt**
```x
"col1","col2","col3"\n
"col1","col2","col3"\n
"col1","col2","col3"\n
"col1","col2","col3"\n
"col1","col2","col3"\n
```

