### useing aws

### instances

public dns
```
ec2-54-69-55-253.us-west-2.compute.amazonaws.com    54.69.55.253    
ec2-35-161-64-189.us-west-2.compute.amazonaws.com   35.161.64.189
ec2-34-208-153-110.us-west-2.compute.amazonaws.com  34.208.153.110
ec2-35-166-138-33.us-west-2.compute.amazonaws.com   35.166.138.33
ec2-54-70-29-110.us-west-2.compute.amazonaws.com    54.70.29.110
```

private dns
```
ip-172-31-6-222.us-west-2.compute.internal
ip-172-31-12-76.us-west-2.compute.internal
ip-172-31-3-241.us-west-2.compute.internal
ip-172-31-1-65.us-west-2.compute.internal
ip-172-31-12-139.us-west-2.compute.internal
```
### linux release

```
LSB Version:    :base-4.0-amd64:base-4.0-noarch:core-4.0-amd64:core-4.0-noarch:graphics-4.0-amd64:graphics-4.0-noarch:printing-4.0-amd64:printing-4.0-noarch
Distributor ID: RedHatEnterpriseServer
Description:    Red Hat Enterprise Linux Server release 6.8 (Santiago)
Release:        6.8
Codename:       Santiago
```

### List the file system capacity for the first node

```
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       30G  1.7G   27G   6% /
tmpfs            16G     0   16G   0% /dev/shm
```

### List the command and output for `yum repolist enabled`

```
[ec2-user@ip-172-31-6-222 ~]$ sudo yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos, security
repo id                                                                                  repo name                                                                                                              status
rhui-REGION-client-config-server-6                                                       Red Hat Update Infrastructure 2.0 Client Configuration Server 6                                                             7
rhui-REGION-rhel-server-releases                                                         Red Hat Enterprise Linux Server 6 (RPMs)                                                                               19,498
rhui-REGION-rhel-server-rh-common                                                        Red Hat Enterprise Linux Server 6 RH Common (RPMs)                                                                        129
repolist: 19,634
```

### List the /etc/passwd entries for zhou and chen

```
zhou:x:2800:2800::/home/zhou:/bin/bash
chen:x:2900:2900::/home/chen:/bin/bash
```

### List the /etc/group entries for shanghai and beijing

```
shanghai:x:2900:
beijing:x:2800:
```