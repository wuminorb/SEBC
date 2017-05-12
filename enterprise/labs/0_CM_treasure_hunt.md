### What is ubertask optimization?

Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

### Where in CM is the Kerberos Security Realm value displayed?
wuminorb.cn

### Which CDH service(s) host a property for enabling Kerberos authentication?

administrtor > security

### How do you upgrade the CM agents?

sudo yum upgrade -y cloudera-scm-agent 

### Give the tsquery statement used to chart Hue's CPU utilization?

select cpu_percent where category=ROLE and serviceName=hive

### Name all the roles that make up the Hive service



### What steps must be completed before integrating Cloudera Manager with Kerberos?
