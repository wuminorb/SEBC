### Create a 10 GB file using teragen

``` bash
[wuminorb@ip-172-31-6-110 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 100000000 /user/wuminorb/teragen
17/05/11 09:50:14 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-6-110.us-west-2.compute.internal/172.31.6.110:8032
17/05/11 09:50:14 INFO terasort.TeraSort: Generating 100000000 using 4
17/05/11 09:50:14 INFO mapreduce.JobSubmitter: number of splits:4
17/05/11 09:50:14 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/11 09:50:14 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/11 09:50:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494489132402_0002
17/05/11 09:50:15 INFO impl.YarnClientImpl: Submitted application application_1494489132402_0002
17/05/11 09:50:15 INFO mapreduce.Job: The url to track the job: http://ip-172-31-6-110.us-west-2.compute.internal:8088/proxy/application_1494489132402_0002/
17/05/11 09:50:15 INFO mapreduce.Job: Running job: job_1494489132402_0002
17/05/11 09:50:22 INFO mapreduce.Job: Job job_1494489132402_0002 running in uber mode : false
17/05/11 09:50:22 INFO mapreduce.Job:  map 0% reduce 0%
17/05/11 09:50:33 INFO mapreduce.Job:  map 5% reduce 0%
17/05/11 09:50:34 INFO mapreduce.Job:  map 10% reduce 0%
17/05/11 09:50:36 INFO mapreduce.Job:  map 13% reduce 0%
17/05/11 09:50:37 INFO mapreduce.Job:  map 16% reduce 0%
17/05/11 09:50:39 INFO mapreduce.Job:  map 18% reduce 0%
17/05/11 09:50:40 INFO mapreduce.Job:  map 21% reduce 0%
17/05/11 09:50:42 INFO mapreduce.Job:  map 22% reduce 0%
17/05/11 09:50:43 INFO mapreduce.Job:  map 25% reduce 0%
17/05/11 09:50:45 INFO mapreduce.Job:  map 26% reduce 0%
17/05/11 09:50:46 INFO mapreduce.Job:  map 29% reduce 0%
17/05/11 09:50:48 INFO mapreduce.Job:  map 30% reduce 0%
17/05/11 09:50:50 INFO mapreduce.Job:  map 33% reduce 0%
17/05/11 09:50:54 INFO mapreduce.Job:  map 36% reduce 0%
17/05/11 09:51:08 INFO mapreduce.Job:  map 37% reduce 0%
17/05/11 09:51:12 INFO mapreduce.Job:  map 39% reduce 0%
17/05/11 09:51:22 INFO mapreduce.Job:  map 40% reduce 0%
17/05/11 09:51:27 INFO mapreduce.Job:  map 41% reduce 0%
17/05/11 09:51:35 INFO mapreduce.Job:  map 42% reduce 0%
17/05/11 09:51:37 INFO mapreduce.Job:  map 43% reduce 0%
17/05/11 09:51:45 INFO mapreduce.Job:  map 45% reduce 0%
17/05/11 09:52:03 INFO mapreduce.Job:  map 46% reduce 0%
17/05/11 09:52:06 INFO mapreduce.Job:  map 48% reduce 0%
17/05/11 09:52:09 INFO mapreduce.Job:  map 49% reduce 0%
17/05/11 09:52:13 INFO mapreduce.Job:  map 50% reduce 0%
17/05/11 09:52:22 INFO mapreduce.Job:  map 51% reduce 0%
17/05/11 09:52:26 INFO mapreduce.Job:  map 52% reduce 0%
17/05/11 09:52:32 INFO mapreduce.Job:  map 53% reduce 0%
17/05/11 09:52:41 INFO mapreduce.Job:  map 54% reduce 0%
17/05/11 09:52:45 INFO mapreduce.Job:  map 55% reduce 0%
17/05/11 09:52:54 INFO mapreduce.Job:  map 56% reduce 0%
17/05/11 09:53:26 INFO mapreduce.Job:  map 60% reduce 0%
17/05/11 09:53:33 INFO mapreduce.Job:  map 61% reduce 0%
17/05/11 09:53:44 INFO mapreduce.Job:  map 62% reduce 0%
17/05/11 09:53:50 INFO mapreduce.Job:  map 63% reduce 0%
17/05/11 09:54:02 INFO mapreduce.Job:  map 64% reduce 0%
17/05/11 09:54:06 INFO mapreduce.Job:  map 65% reduce 0%
17/05/11 09:54:09 INFO mapreduce.Job:  map 66% reduce 0%
17/05/11 09:54:16 INFO mapreduce.Job:  map 67% reduce 0%
17/05/11 09:54:19 INFO mapreduce.Job:  map 68% reduce 0%
17/05/11 09:54:25 INFO mapreduce.Job:  map 69% reduce 0%
17/05/11 09:54:33 INFO mapreduce.Job:  map 70% reduce 0%
17/05/11 09:54:36 INFO mapreduce.Job:  map 71% reduce 0%
17/05/11 09:54:40 INFO mapreduce.Job:  map 72% reduce 0%
17/05/11 09:54:55 INFO mapreduce.Job:  map 73% reduce 0%
17/05/11 09:55:00 INFO mapreduce.Job:  map 74% reduce 0%
17/05/11 09:55:03 INFO mapreduce.Job:  map 77% reduce 0%
17/05/11 09:55:06 INFO mapreduce.Job:  map 86% reduce 0%
17/05/11 09:55:09 INFO mapreduce.Job:  map 90% reduce 0%
17/05/11 09:55:12 INFO mapreduce.Job:  map 93% reduce 0%
17/05/11 09:55:13 INFO mapreduce.Job:  map 94% reduce 0%
17/05/11 09:55:15 INFO mapreduce.Job:  map 97% reduce 0%
17/05/11 09:55:18 INFO mapreduce.Job:  map 99% reduce 0%
17/05/11 09:55:19 INFO mapreduce.Job:  map 100% reduce 0%
17/05/11 09:55:21 INFO mapreduce.Job: Job job_1494489132402_0002 completed successfully
17/05/11 09:55:21 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494152
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=1165371
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1165371
                Total vcore-seconds taken by all map tasks=1165371
                Total megabyte-seconds taken by all map tasks=1193339904
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1354
                CPU time spent (ms)=161400
                Physical memory (bytes) snapshot=683708416
                Virtual memory (bytes) snapshot=6264938496
                Total committed heap usage (bytes)=937426944
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    5m9.778s
user    0m6.095s
sys     0m0.365s
```

### Run the terasort command on this file

``` bash
[wuminorb@ip-172-31-6-110 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort -Dmapred.reduce.tasks=4 /user/wuminorb/teragen /user/wuminorb/terasort
17/05/11 10:01:50 INFO terasort.TeraSort: starting
17/05/11 10:01:51 INFO input.FileInputFormat: Total input paths to process : 4
Spent 289ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 294ms
Sampling 10 splits of 300
Making 4 from 100000 sampled records
Computing parititions took 859ms
Spent 1155ms computing partitions.
17/05/11 10:01:52 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-6-110.us-west-2.compute.internal/172.31.6.110:8032
17/05/11 10:01:53 INFO mapreduce.JobSubmitter: number of splits:300
17/05/11 10:01:53 INFO Configuration.deprecation: mapred.reduce.tasks is deprecated. Instead, use mapreduce.job.reduces
17/05/11 10:01:53 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494489132402_0003
17/05/11 10:01:53 INFO impl.YarnClientImpl: Submitted application application_1494489132402_0003
17/05/11 10:01:53 INFO mapreduce.Job: The url to track the job: http://ip-172-31-6-110.us-west-2.compute.internal:8088/proxy/application_1494489132402_0003/
17/05/11 10:01:53 INFO mapreduce.Job: Running job: job_1494489132402_0003
17/05/11 10:01:59 INFO mapreduce.Job: Job job_1494489132402_0003 running in uber mode : false
17/05/11 10:01:59 INFO mapreduce.Job:  map 0% reduce 0%
17/05/11 10:02:07 INFO mapreduce.Job:  map 2% reduce 0%
17/05/11 10:02:11 INFO mapreduce.Job:  map 3% reduce 0%
17/05/11 10:02:14 INFO mapreduce.Job:  map 4% reduce 0%
17/05/11 10:02:15 INFO mapreduce.Job:  map 5% reduce 0%
17/05/11 10:02:20 INFO mapreduce.Job:  map 6% reduce 0%
17/05/11 10:02:21 INFO mapreduce.Job:  map 7% reduce 0%
17/05/11 10:02:27 INFO mapreduce.Job:  map 8% reduce 0%
17/05/11 10:02:28 INFO mapreduce.Job:  map 9% reduce 0%
17/05/11 10:02:29 INFO mapreduce.Job:  map 10% reduce 0%
17/05/11 10:02:35 INFO mapreduce.Job:  map 11% reduce 0%
17/05/11 10:02:36 INFO mapreduce.Job:  map 12% reduce 0%
17/05/11 10:02:41 INFO mapreduce.Job:  map 13% reduce 0%
17/05/11 10:02:43 INFO mapreduce.Job:  map 14% reduce 0%
17/05/11 10:02:46 INFO mapreduce.Job:  map 15% reduce 0%
17/05/11 10:02:49 INFO mapreduce.Job:  map 16% reduce 0%
17/05/11 10:02:51 INFO mapreduce.Job:  map 17% reduce 0%
17/05/11 10:02:56 INFO mapreduce.Job:  map 18% reduce 0%
17/05/11 10:02:57 INFO mapreduce.Job:  map 19% reduce 0%
17/05/11 10:03:02 INFO mapreduce.Job:  map 20% reduce 0%
17/05/11 10:03:03 INFO mapreduce.Job:  map 21% reduce 0%
17/05/11 10:03:05 INFO mapreduce.Job:  map 22% reduce 0%
17/05/11 10:03:10 INFO mapreduce.Job:  map 23% reduce 0%
17/05/11 10:03:12 INFO mapreduce.Job:  map 24% reduce 0%
17/05/11 10:03:16 INFO mapreduce.Job:  map 25% reduce 0%
17/05/11 10:03:18 INFO mapreduce.Job:  map 26% reduce 0%
17/05/11 10:03:19 INFO mapreduce.Job:  map 27% reduce 0%
17/05/11 10:03:24 INFO mapreduce.Job:  map 28% reduce 0%
17/05/11 10:03:26 INFO mapreduce.Job:  map 29% reduce 0%
17/05/11 10:03:31 INFO mapreduce.Job:  map 30% reduce 0%
17/05/11 10:03:32 INFO mapreduce.Job:  map 31% reduce 0%
17/05/11 10:03:36 INFO mapreduce.Job:  map 32% reduce 0%
17/05/11 10:03:38 INFO mapreduce.Job:  map 33% reduce 0%
17/05/11 10:03:40 INFO mapreduce.Job:  map 34% reduce 0%
17/05/11 10:03:44 INFO mapreduce.Job:  map 35% reduce 0%
17/05/11 10:03:46 INFO mapreduce.Job:  map 36% reduce 0%
17/05/11 10:03:51 INFO mapreduce.Job:  map 37% reduce 0%
17/05/11 10:03:52 INFO mapreduce.Job:  map 38% reduce 0%
17/05/11 10:03:54 INFO mapreduce.Job:  map 39% reduce 0%
17/05/11 10:03:59 INFO mapreduce.Job:  map 40% reduce 0%
17/05/11 10:04:00 INFO mapreduce.Job:  map 41% reduce 0%
17/05/11 10:04:05 INFO mapreduce.Job:  map 42% reduce 0%
17/05/11 10:04:06 INFO mapreduce.Job:  map 43% reduce 0%
17/05/11 10:04:11 INFO mapreduce.Job:  map 44% reduce 0%
17/05/11 10:04:13 INFO mapreduce.Job:  map 45% reduce 0%
17/05/11 10:04:15 INFO mapreduce.Job:  map 46% reduce 0%
17/05/11 10:04:19 INFO mapreduce.Job:  map 47% reduce 0%
17/05/11 10:04:21 INFO mapreduce.Job:  map 48% reduce 0%
17/05/11 10:04:25 INFO mapreduce.Job:  map 49% reduce 0%
17/05/11 10:04:27 INFO mapreduce.Job:  map 50% reduce 0%
17/05/11 10:04:29 INFO mapreduce.Job:  map 51% reduce 0%
17/05/11 10:04:33 INFO mapreduce.Job:  map 52% reduce 0%
17/05/11 10:04:35 INFO mapreduce.Job:  map 53% reduce 0%
17/05/11 10:04:40 INFO mapreduce.Job:  map 54% reduce 0%
17/05/11 10:04:41 INFO mapreduce.Job:  map 55% reduce 0%
17/05/11 10:04:46 INFO mapreduce.Job:  map 56% reduce 0%
17/05/11 10:04:47 INFO mapreduce.Job:  map 57% reduce 0%
17/05/11 10:04:49 INFO mapreduce.Job:  map 58% reduce 0%
17/05/11 10:04:54 INFO mapreduce.Job:  map 59% reduce 0%
17/05/11 10:04:56 INFO mapreduce.Job:  map 60% reduce 0%
17/05/11 10:05:00 INFO mapreduce.Job:  map 61% reduce 0%
17/05/11 10:05:02 INFO mapreduce.Job:  map 62% reduce 0%
17/05/11 10:05:03 INFO mapreduce.Job:  map 63% reduce 0%
17/05/11 10:05:08 INFO mapreduce.Job:  map 64% reduce 0%
17/05/11 10:05:10 INFO mapreduce.Job:  map 65% reduce 0%
17/05/11 10:05:14 INFO mapreduce.Job:  map 66% reduce 0%
17/05/11 10:05:15 INFO mapreduce.Job:  map 67% reduce 0%
17/05/11 10:05:20 INFO mapreduce.Job:  map 68% reduce 0%
17/05/11 10:05:22 INFO mapreduce.Job:  map 69% reduce 0%
17/05/11 10:05:24 INFO mapreduce.Job:  map 70% reduce 0%
17/05/11 10:05:29 INFO mapreduce.Job:  map 71% reduce 0%
17/05/11 10:05:31 INFO mapreduce.Job:  map 72% reduce 0%
17/05/11 10:05:36 INFO mapreduce.Job:  map 73% reduce 0%
17/05/11 10:05:37 INFO mapreduce.Job:  map 74% reduce 0%
17/05/11 10:05:39 INFO mapreduce.Job:  map 75% reduce 0%
17/05/11 10:05:44 INFO mapreduce.Job:  map 76% reduce 0%
17/05/11 10:05:46 INFO mapreduce.Job:  map 77% reduce 0%
17/05/11 10:05:50 INFO mapreduce.Job:  map 78% reduce 0%
17/05/11 10:05:51 INFO mapreduce.Job:  map 79% reduce 0%
17/05/11 10:05:55 INFO mapreduce.Job:  map 80% reduce 0%
17/05/11 10:05:58 INFO mapreduce.Job:  map 81% reduce 0%
17/05/11 10:06:00 INFO mapreduce.Job:  map 82% reduce 0%
17/05/11 10:06:04 INFO mapreduce.Job:  map 83% reduce 0%
17/05/11 10:06:08 INFO mapreduce.Job:  map 84% reduce 0%
17/05/11 10:06:09 INFO mapreduce.Job:  map 84% reduce 3%
17/05/11 10:06:11 INFO mapreduce.Job:  map 84% reduce 6%
17/05/11 10:06:14 INFO mapreduce.Job:  map 84% reduce 7%
17/05/11 10:06:15 INFO mapreduce.Job:  map 85% reduce 13%
17/05/11 10:06:17 INFO mapreduce.Job:  map 85% reduce 14%
17/05/11 10:06:18 INFO mapreduce.Job:  map 85% reduce 17%
17/05/11 10:06:20 INFO mapreduce.Job:  map 85% reduce 18%
17/05/11 10:06:21 INFO mapreduce.Job:  map 85% reduce 20%
17/05/11 10:06:22 INFO mapreduce.Job:  map 86% reduce 20%
17/05/11 10:06:23 INFO mapreduce.Job:  map 86% reduce 21%
17/05/11 10:06:24 INFO mapreduce.Job:  map 86% reduce 23%
17/05/11 10:06:25 INFO mapreduce.Job:  map 86% reduce 24%
17/05/11 10:06:26 INFO mapreduce.Job:  map 86% reduce 25%
17/05/11 10:06:27 INFO mapreduce.Job:  map 86% reduce 26%
17/05/11 10:06:28 INFO mapreduce.Job:  map 86% reduce 27%
17/05/11 10:06:29 INFO mapreduce.Job:  map 87% reduce 27%
17/05/11 10:06:30 INFO mapreduce.Job:  map 87% reduce 28%
17/05/11 10:06:31 INFO mapreduce.Job:  map 87% reduce 29%
17/05/11 10:06:35 INFO mapreduce.Job:  map 88% reduce 29%
17/05/11 10:06:40 INFO mapreduce.Job:  map 89% reduce 29%
17/05/11 10:06:42 INFO mapreduce.Job:  map 89% reduce 30%
17/05/11 10:06:46 INFO mapreduce.Job:  map 90% reduce 30%
17/05/11 10:06:52 INFO mapreduce.Job:  map 91% reduce 30%
17/05/11 10:06:58 INFO mapreduce.Job:  map 92% reduce 30%
17/05/11 10:06:59 INFO mapreduce.Job:  map 92% reduce 31%
17/05/11 10:07:04 INFO mapreduce.Job:  map 93% reduce 31%
17/05/11 10:07:10 INFO mapreduce.Job:  map 94% reduce 31%
17/05/11 10:07:16 INFO mapreduce.Job:  map 95% reduce 31%
17/05/11 10:07:18 INFO mapreduce.Job:  map 95% reduce 32%
17/05/11 10:07:21 INFO mapreduce.Job:  map 96% reduce 32%
17/05/11 10:07:26 INFO mapreduce.Job:  map 97% reduce 32%
17/05/11 10:07:32 INFO mapreduce.Job:  map 98% reduce 32%
17/05/11 10:07:33 INFO mapreduce.Job:  map 98% reduce 33%
17/05/11 10:07:37 INFO mapreduce.Job:  map 99% reduce 33%
17/05/11 10:07:43 INFO mapreduce.Job:  map 100% reduce 33%
17/05/11 10:07:45 INFO mapreduce.Job:  map 100% reduce 55%
17/05/11 10:07:46 INFO mapreduce.Job:  map 100% reduce 63%
17/05/11 10:07:48 INFO mapreduce.Job:  map 100% reduce 69%
17/05/11 10:07:49 INFO mapreduce.Job:  map 100% reduce 70%
17/05/11 10:07:51 INFO mapreduce.Job:  map 100% reduce 73%
17/05/11 10:07:54 INFO mapreduce.Job:  map 100% reduce 76%
17/05/11 10:07:55 INFO mapreduce.Job:  map 100% reduce 77%
17/05/11 10:07:57 INFO mapreduce.Job:  map 100% reduce 80%
17/05/11 10:07:58 INFO mapreduce.Job:  map 100% reduce 81%
17/05/11 10:08:00 INFO mapreduce.Job:  map 100% reduce 84%
17/05/11 10:08:01 INFO mapreduce.Job:  map 100% reduce 85%
17/05/11 10:08:03 INFO mapreduce.Job:  map 100% reduce 88%
17/05/11 10:08:04 INFO mapreduce.Job:  map 100% reduce 89%
17/05/11 10:08:06 INFO mapreduce.Job:  map 100% reduce 91%
17/05/11 10:08:07 INFO mapreduce.Job:  map 100% reduce 92%
17/05/11 10:08:09 INFO mapreduce.Job:  map 100% reduce 94%
17/05/11 10:08:10 INFO mapreduce.Job:  map 100% reduce 95%
17/05/11 10:08:12 INFO mapreduce.Job:  map 100% reduce 96%
17/05/11 10:08:16 INFO mapreduce.Job:  map 100% reduce 97%
17/05/11 10:08:19 INFO mapreduce.Job:  map 100% reduce 98%
17/05/11 10:08:22 INFO mapreduce.Job:  map 100% reduce 99%
17/05/11 10:08:26 INFO mapreduce.Job:  map 100% reduce 100%
17/05/11 10:08:27 INFO mapreduce.Job: Job job_1494489132402_0003 completed successfully
17/05/11 10:08:27 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4488736579
                FILE: Number of bytes written=8901883798
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000046200
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=912
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=4
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=1657179
                Total time spent by all reduces in occupied slots (ms)=543470
                Total time spent by all map tasks (ms)=1657179
                Total time spent by all reduce tasks (ms)=543470
                Total vcore-seconds taken by all map tasks=1657179
                Total vcore-seconds taken by all reduce tasks=543470
                Total megabyte-seconds taken by all map tasks=1696951296
                Total megabyte-seconds taken by all reduce tasks=556513280
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375145585
                Input split bytes=46200
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375145585
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1200
                Failed Shuffles=0
                Merged Map outputs=1200
                GC time elapsed (ms)=23463
                CPU time spent (ms)=1185230
                Physical memory (bytes) snapshot=144435236864
                Virtual memory (bytes) snapshot=476896727040
                Total committed heap usage (bytes)=179031244800
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/05/11 10:08:27 INFO terasort.TeraSort: done

real    6m38.425s
user    0m8.993s
sys     0m0.490s
```