**co trzeci**
```php
if( (($i % 3) == 1) and ($i != 1) ) { ... }
```

**pobranie zmiennej out z procedury przy użyciu multi_query**
```php
$query  = "CALL w_tree(".$id.",@crumb);";
$query .= "SELECT @crumb";
if ($db->multi_query($query)) {
    do {
        /* store first result set */
        if ($result = $db->store_result()) {
            while ($row = $result->fetch_row()) {
                printf("%s\n", $row[0]);
            }
            $result->free();
        }
        /* print divider */
        if ($db->more_results()) {
            printf("-----------------\n");
        }
    } while ($db->next_result());
}
```
