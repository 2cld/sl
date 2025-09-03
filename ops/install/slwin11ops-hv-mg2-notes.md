# slwin11ops-hv-mg2-notes

- ssh ghadmin@10.147.17.135

# network
```bash
ghadmin@mg2:~$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
    link/ether 00:15:5d:09:bf:02 brd ff:ff:ff:ff:ff:ff
    inet 192.168.0.140/24 brd 192.168.0.255 scope global dynamic noprefixroute eth0
       valid_lft 3710sec preferred_lft 3710sec
    inet6 fe80::215:5dff:fe09:bf02/64 scope link
       valid_lft forever preferred_lft forever
3: ztwdjolumt: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 2800 qdisc fq_codel state UNKNOWN group default qlen 1000
    link/ether a6:a5:7b:17:ae:cf brd ff:ff:ff:ff:ff:ff
    inet 10.147.17.135/24 brd 10.147.17.255 scope global ztwdjolumt
       valid_lft forever preferred_lft forever
    inet6 fe80::a4a5:7bff:fe17:aecf/64 scope link
       valid_lft forever preferred_lft forever
ghadmin@mg2:~$
```
