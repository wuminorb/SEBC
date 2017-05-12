### The full teragen command and job output
```
[zhou@ip-172-31-6-222 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapreduce.map.memory.mb=1024 -Dmapred.map.tasks=6 -Ddfs.block.size=67108864 65536000 /user/zhou/tgen
17/05/11 23:32:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-12-76.us-west-2.compute.internal/172.31.12.76:8032
17/05/11 23:32:22 INFO terasort.TeraSort: Generating 65536000 using 6
17/05/11 23:32:22 INFO mapreduce.JobSubmitter: number of splits:6
17/05/11 23:32:22 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/11 23:32:22 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/11 23:32:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494557530022_0001
17/05/11 23:32:23 INFO impl.YarnClientImpl: Submitted application application_1494557530022_0001
17/05/11 23:32:23 INFO mapreduce.Job: The url to track the job: http://ip-172-31-12-76.us-west-2.compute.internal:8088/proxy/application_1494557530022_0001/
17/05/11 23:32:23 INFO mapreduce.Job: Running job: job_1494557530022_0001
17/05/11 23:32:29 INFO mapreduce.Job: Job job_1494557530022_0001 running in uber mode : false
17/05/11 23:32:29 INFO mapreduce.Job:  map 0% reduce 0%
17/05/11 23:32:41 INFO mapreduce.Job:  map 14% reduce 0%
17/05/11 23:32:44 INFO mapreduce.Job:  map 24% reduce 0%
17/05/11 23:32:47 INFO mapreduce.Job:  map 32% reduce 0%
17/05/11 23:32:50 INFO mapreduce.Job:  map 38% reduce 0%
17/05/11 23:32:53 INFO mapreduce.Job:  map 44% reduce 0%
17/05/11 23:32:56 INFO mapreduce.Job:  map 53% reduce 0%
17/05/11 23:32:59 INFO mapreduce.Job:  map 59% reduce 0%
17/05/11 23:33:02 INFO mapreduce.Job:  map 68% reduce 0%
17/05/11 23:33:06 INFO mapreduce.Job:  map 71% reduce 0%
17/05/11 23:33:09 INFO mapreduce.Job:  map 75% reduce 0%
17/05/11 23:33:12 INFO mapreduce.Job:  map 81% reduce 0%
17/05/11 23:33:33 INFO mapreduce.Job:  map 86% reduce 0%
17/05/11 23:33:42 INFO mapreduce.Job:  map 87% reduce 0%
17/05/11 23:34:15 INFO mapreduce.Job:  map 90% reduce 0%
17/05/11 23:34:16 INFO mapreduce.Job:  map 93% reduce 0%
17/05/11 23:34:17 INFO mapreduce.Job:  map 96% reduce 0%
17/05/11 23:34:18 INFO mapreduce.Job:  map 100% reduce 0%
17/05/11 23:34:20 INFO mapreduce.Job: Job job_1494557530022_0001 completed successfully
17/05/11 23:34:20 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=741102
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=511
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=621702
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=621702
                Total vcore-seconds taken by all map tasks=621702
                Total megabyte-seconds taken by all map tasks=636622848
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=511
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=834
                CPU time spent (ms)=112300
                Physical memory (bytes) snapshot=1652105216
                Virtual memory (bytes) snapshot=9475166208
                Total committed heap usage (bytes)=3036151808
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    2m0.175s
user    0m4.620s
sys     0m0.343s
```
### The result of the time command
```
real    2m0.175s
user    0m4.620s
sys     0m0.343s
```
### The command and output of hdfs dfs -ls /user/zhou/tgen
```
[zhou@ip-172-31-6-222 ec2-user]$ hdfs dfs -ls /user/zhou/tgen
Found 7 items
-rw-r--r--   3 zhou beiijing          0 2017-05-11 23:34 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou beiijing 1092266700 2017-05-11 23:34 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou beiijing 1092266700 2017-05-11 23:34 /user/zhou/tgen/part-m-00001
-rw-r--r--   3 zhou beiijing 1092266600 2017-05-11 23:34 /user/zhou/tgen/part-m-00002
-rw-r--r--   3 zhou beiijing 1092266700 2017-05-11 23:34 /user/zhou/tgen/part-m-00003
-rw-r--r--   3 zhou beiijing 1092266700 2017-05-11 23:34 /user/zhou/tgen/part-m-00004
-rw-r--r--   3 zhou beiijing 1092266600 2017-05-11 23:34 /user/zhou/tgen/part-m-00005
```