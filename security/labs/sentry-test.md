### Verify user privileges

```
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-4-161.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-4-161.us-west-2.compute.internal@wuminorb.cn
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-4-161.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-4-161.us-west-2.compute.internal@wuminorb.cn
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170513043737_2135325f-3e6d-4f09-b6f2-504720e102fc): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170513043737_2135325f-3e6d-4f09-b6f2-504720e102fc); Time taken: 0.082 seconds
INFO  : Executing command(queryId=hive_20170513043737_2135325f-3e6d-4f09-b6f2-504720e102fc): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513043737_2135325f-3e6d-4f09-b6f2-504720e102fc); Time taken: 0.139 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.314 seconds)
```

### Create a Sentry role with full authorization

```
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170513044040_937ac673-087f-4e85-bc7f-3b0d62b49095): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513044040_937ac673-087f-4e85-bc7f-3b0d62b49095); Time taken: 0.078 seconds
INFO  : Executing command(queryId=hive_20170513044040_937ac673-087f-4e85-bc7f-3b0d62b49095): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513044040_937ac673-087f-4e85-bc7f-3b0d62b49095); Time taken: 0.655 seconds
INFO  : OK
No rows affected (0.745 seconds)
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20170513044040_cb0f7bbb-552a-4ca4-809b-bf845a954c23): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513044040_cb0f7bbb-552a-4ca4-809b-bf845a954c23); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20170513044040_cb0f7bbb-552a-4ca4-809b-bf845a954c23): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513044040_cb0f7bbb-552a-4ca4-809b-bf845a954c23); Time taken: 0.107 seconds
INFO  : OK
No rows affected (0.185 seconds)
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT ROLE sentry_admin TO GROUP tom;
INFO  : Compiling command(queryId=hive_20170513044040_1a229a7d-81b8-4e6d-9711-85a57e3acf1e): GRANT ROLE sentry_admin TO GROUP tom
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513044040_1a229a7d-81b8-4e6d-9711-85a57e3acf1e); Time taken: 0.081 seconds
INFO  : Executing command(queryId=hive_20170513044040_1a229a7d-81b8-4e6d-9711-85a57e3acf1e): GRANT ROLE sentry_admin TO GROUP tom
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513044040_1a229a7d-81b8-4e6d-9711-85a57e3acf1e); Time taken: 0.066 seconds
INFO  : OK
No rows affected (0.159 seconds)
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170513044040_9e2c84ca-8a8c-4f4e-ac79-4d4b0fb746fc): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170513044040_9e2c84ca-8a8c-4f4e-ac79-4d4b0fb746fc); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20170513044040_9e2c84ca-8a8c-4f4e-ac79-4d4b0fb746fc): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513044040_9e2c84ca-8a8c-4f4e-ac79-4d4b0fb746fc); Time taken: 0.114 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.215 seconds)
```

### Create additional test users


### Create test roles

```
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20170513081818_4520c88d-6311-4a91-b003-22bd0731cd87): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081818_4520c88d-6311-4a91-b003-22bd0731cd87); Time taken: 0.082 seconds
INFO  : Executing command(queryId=hive_20170513081818_4520c88d-6311-4a91-b003-22bd0731cd87): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081818_4520c88d-6311-4a91-b003-22bd0731cd87); Time taken: 0.028 seconds
INFO  : OK
No rows affected (0.158 seconds)


0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20170513081818_9e311db3-1447-462e-a398-29568ed9dcc8): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081818_9e311db3-1447-462e-a398-29568ed9dcc8); Time taken: 0.049 seconds
INFO  : Executing command(queryId=hive_20170513081818_9e311db3-1447-462e-a398-29568ed9dcc8): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081818_9e311db3-1447-462e-a398-29568ed9dcc8); Time taken: 0.021 seconds
INFO  : OK
No rows affected (0.081 seconds)

```

### Grant read privilege for all tables to reads
```
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20170513081818_5959e057-049a-4396-b921-c131eef0697a): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081818_5959e057-049a-4396-b921-c131eef0697a); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20170513081818_5959e057-049a-4396-b921-c131eef0697a): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081818_5959e057-049a-4396-b921-c131eef0697a); Time taken: 0.031 seconds
INFO  : OK
No rows affected (0.099 seconds)


0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20170513081818_88e8786e-d52b-4cbd-9a5b-fb0c37fbbc3b): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081818_88e8786e-d52b-4cbd-9a5b-fb0c37fbbc3b); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20170513081818_88e8786e-d52b-4cbd-9a5b-fb0c37fbbc3b): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081818_88e8786e-d52b-4cbd-9a5b-fb0c37fbbc3b); Time taken: 0.025 seconds
INFO  : OK
No rows affected (0.09 seconds)
```


### Grant read privilege for default.sample07 only to 'writes'

```
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20170513081919_620913eb-380e-4b90-ae3a-23220d8f7b4c): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081919_620913eb-380e-4b90-ae3a-23220d8f7b4c); Time taken: 0.05 seconds
INFO  : Executing command(queryId=hive_20170513081919_620913eb-380e-4b90-ae3a-23220d8f7b4c): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081919_620913eb-380e-4b90-ae3a-23220d8f7b4c); Time taken: 0.067 seconds
INFO  : OK
No rows affected (0.129 seconds)


0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20170513081919_e98233aa-1705-43ff-8fcd-d2ceadeefa57): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081919_e98233aa-1705-43ff-8fcd-d2ceadeefa57); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20170513081919_e98233aa-1705-43ff-8fcd-d2ceadeefa57): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081919_e98233aa-1705-43ff-8fcd-d2ceadeefa57); Time taken: 0.031 seconds
INFO  : OK
No rows affected (0.095 seconds)


0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20170513081919_fc98f9e1-81d6-42c3-a5cb-71c9aa906e53): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170513081919_fc98f9e1-81d6-42c3-a5cb-71c9aa906e53); Time taken: 0.05 seconds
INFO  : Executing command(queryId=hive_20170513081919_fc98f9e1-81d6-42c3-a5cb-71c9aa906e53): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513081919_fc98f9e1-81d6-42c3-a5cb-71c9aa906e53); Time taken: 0.024 seconds
INFO  : OK
No rows affected (0.087 seconds)
```


### kinit as george, then login to beeline

```
[george@ip-172-31-6-110 ec2-user]$ kinit george
Password for george@wuminorb.cn:

[george@ip-172-31-6-110 ec2-user]$ beeline

Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-4-161.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-4-161.us-west-2.compute.internal@wuminorb.cn
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-4-161.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-4-161.us-west-2.compute.internal@wuminorb.cn
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ

0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170513082121_5c12f97b-ad87-4b0a-bd5a-e60314492153): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170513082121_5c12f97b-ad87-4b0a-bd5a-e60314492153); Time taken: 0.058 seconds
INFO  : Executing command(queryId=hive_20170513082121_5c12f97b-ad87-4b0a-bd5a-e60314492153): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513082121_5c12f97b-ad87-4b0a-bd5a-e60314492153); Time taken: 0.112 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.256 seconds)
0: jdbc:hive2://ip-172-31-4-161
```

as ferdinand
```
0: jdbc:hive2://ip-172-31-4-161.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170513082626_fb31fbb1-3098-4830-9f58-3ff9ef5ba5f9): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170513082626_fb31fbb1-3098-4830-9f58-3ff9ef5ba5f9); Time taken: 0.095 seconds
INFO  : Executing command(queryId=hive_20170513082626_fb31fbb1-3098-4830-9f58-3ff9ef5ba5f9): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170513082626_fb31fbb1-3098-4830-9f58-3ff9ef5ba5f9); Time taken: 0.114 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.318 seconds)
```