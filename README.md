# clean-spam-sav
Prestashop Clean spam in sav 
SQL command
```sql
DELETE ct.*, cm.*
FROM ps_customer_thread AS ct
JOIN
	ps_customer_message AS cm
ON cm.id_customer_thread = ct.id_customer_thread
WHERE ct.email LIKE '%qq.com'
```

# clean big tables 
#### ps_connections
```DELETE FROM `ps_connections` WHERE `date_add` < ( NOW( ) - INTERVAL 1 MONTH );```

#### ps_connections_sources
```DELETE FROM `ps_connections_source` WHERE `date_add` < ( NOW( ) - INTERVAL 1 MONTH );```

#### ps_connections_page
```DELETE FROM `ps_connections_page` WHERE `time_start` < ( NOW( ) - INTERVAL 1 MONTH );```

#### ps_guest
```DELETE FROM `ps_guest` ```

#### ps_pagenotfound
```DELETE FROM `ps_pagenotfound` WHERE `date_add` < ( NOW( ) - INTERVAL 1 MONTH );```
