### The kinit command use to authenticate test user

```
[ec2-user@ip-172-31-6-110 ~]$ kinit tom
Password for tom@wuminorb.cn:
```
### The output from a klist command listing credentials and ticket lifetime

```
[ec2-user@ip-172-31-6-110 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: tom@wuminorb.cn

Valid starting     Expires            Service principal
05/13/17 04:09:59  05/14/17 04:09:59  krbtgt/wuminorb.cn@wuminorb.cn
        renew until 05/20/17 04:09:59
```