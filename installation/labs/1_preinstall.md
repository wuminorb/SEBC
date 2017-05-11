- check `vm.swappiness`

``` bash
[ec2-user@ip-172-31-27-105 ~]$ sysctl vm.swappiness
vm.swappiness = 60
```

- set `vm.swappiness` to `1`

add above line to `/etc/sysctl.conf` to set `vm.swappiness` at boot time
``` bash
vm.swappiness = 1
```

set `vm.swappiness` at runtime
``` bash
[ec2-user@ip-172-31-27-105 ~]$ sudo sysctl -w vm.swappiness=1
vm.swappiness = 1
```

check `vm.swappiness`
``` bash
[ec2-user@ip-172-31-27-105 ~]$ sysctl vm.swappiness
vm.swappiness = 1
```

- Show the mount attributes of volume(s) 

``` bash
[ec2-user@ip-172-31-27-105 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  1.7G   27G   6% /
tmpfs           7.3G     0  7.3G   0% /dev/shm

[ec2-user@ip-172-31-27-105 ~]$ sudo lsblk -f
NAME    FSTYPE LABEL UUID                                 MOUNTPOINT
xvda
└─xvda1 ext4         05d6faee-1d92-462b-be37-aaa0097875e8 /
```

- List the reserve space setting for ext4 volumes

``` bash
[ec2-user@ip-172-31-27-105 ~]$ sudo tune2fs -l /dev/xvda1 | grep Reserve
Reserved block count:     393126
Reserved GDT blocks:      382
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
```

- Disable transparent hugepage support

Check transparent hugepage setting

``` bash
[ec2-user@ip-172-31-27-105 ~]$ cat /sys/kernel/mm/redhat_transparent_hugepage/enabled
[always] madvise never

[ec2-user@ip-172-31-27-105 ~]$ sudo grep AnonHugePages /proc/meminfo
AnonHugePages:      2048 kB
```

Disable THP at boot time, append to /etc/grub.conf
``` bash
transparent_hugepage=never
```

Disable THP at runtime

``` bash
sudo sh -c 'echo never > /sys/kernel/mm/redhat_transparent_hugepage/enabled'
sudo sh -c 'echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag'
```

Check THP setting

``` bash
[ec2-user@ip-172-31-27-105 ~]$ sudo grep -i HugePages_Total /proc/meminfo
HugePages_Total:       0
```

- List your network interface configuration

``` bash
[ec2-user@ip-172-31-6-110 ~]$ sudo ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:82:0B:27:A1:E8
          inet addr:172.31.6.110  Bcast:172.31.15.255  Mask:255.255.240.0
          inet6 addr: fe80::882:bff:fe27:a1e8/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:3365903 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1198334 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:4506139813 (4.1 GiB)  TX bytes:4717826728 (4.3 GiB)

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:740000 errors:0 dropped:0 overruns:0 frame:0
          TX packets:740000 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:1287197569 (1.1 GiB)  TX bytes:1287197569 (1.1 GiB)
```

- Show that forward and reverse host lookups are correctly resolved

``` bash
[ec2-user@ip-172-31-6-110 ~]$ nslookup ip-172-31-14-185.us-west-2.compute.internal
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-14-185.us-west-2.compute.internal
Address: 172.31.14.185

[ec2-user@ip-172-31-6-110 ~]$ nslookup 172.31.14.185
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
185.14.31.172.in-addr.arpa      name = ip-172-31-14-185.us-west-2.compute.internal.

Authoritative answers can be found from:

```

- Show the ntpd service is running

``` bash
[ec2-user@ip-172-31-27-105 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[ec2-user@ip-172-31-27-105 ~]$ /etc/init.d/ntpd status
ntpd (pid  30431) is running...
```
- Show the nscd service is running

``` bash
[ec2-user@ip-172-31-27-105 ~]$ sudo yum install -y nscd
[ec2-user@ip-172-31-27-105 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[ec2-user@ip-172-31-27-105 ~]$ /etc/init.d/nscd status
nscd (pid 30535) is running...
```