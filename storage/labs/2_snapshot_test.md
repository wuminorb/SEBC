### HDFS Lab: Test HDFS Snapshots

``` bash
[ec2-user@ip-172-31-6-110 ~]$ su wuminorb
[wuminorb@ip-172-31-6-110 ec2-user]$ hadoop fs -mkdir /user/wuminorb/snapshot-test
[wuminorb@ip-172-31-6-110 ec2-user]$ hadoop fs -put /home/wuminorb/SEBC-Shanghai.zip /user/wuminorb/snapshot-test/SEBC-Shanghai.zip
[wuminorb@ip-172-31-6-110 ec2-user]$ exit
exit
[ec2-user@ip-172-31-6-110 ~]$ sudo su hdfs
[hdfs@ip-172-31-6-110 ec2-user]$ hdfs dfsadmin -allowSnapshot /user/wuminorb/snapshot-test
Allowing snaphot on /user/wuminorb/snapshot-test succeeded
[hdfs@ip-172-31-6-110 ec2-user]$ hdfs dfs -createSnapshot /user/wuminorb/snapshot-test sebc-hdfs-test
Created snapshot /user/wuminorb/snapshot-test/.snapshot/sebc-hdfs-test
[hdfs@ip-172-31-6-110 ec2-user]$ hadoop fs -rm -r /user/wuminorb/snapshot-test
rm: Failed to move to trash: hdfs://ip-172-31-4-161.us-west-2.compute.internal:8020/user/wuminorb/snapshot-test: The directory /user/wuminorb/snapshot-test cannot be deleted since /user/wuminorb/snapshot-test is snapshottable and already has snapshots
[hdfs@ip-172-31-6-110 ec2-user]$ exit
exit
[ec2-user@ip-172-31-6-110 ~]$ su wuminorb
[wuminorb@ip-172-31-6-110 ec2-user]$ hadoop fs -rm -r -skipTrash /user/wuminorb/snapshot-test/SEBC-Shanghai.zip
Deleted /user/wuminorb/snapshot-test/SEBC-Shanghai.zip
[wuminorb@ip-172-31-6-110 ec2-user]$ hadoop fs -cp /user/wuminorb/snapshot-test/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip /user/wuminorb/snapshot-test/SEBC-Shanghai.zip
```