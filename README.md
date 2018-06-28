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
