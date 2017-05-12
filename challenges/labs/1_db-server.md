### hostname
ip-172-31-6-222.us-west-2.compute.internal

### mysql server version

```
mysql> SELECT @@version;
+-----------+
| @@version |
+-----------+
| 5.6.36    |
+-----------+
1 row in set (0.00 sec)
```

### show databases

```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hive               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
13 rows in set (0.00 sec)
```