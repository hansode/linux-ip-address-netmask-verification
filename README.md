Linux: IP address netmask
=========================

System Requirements
-------------------

+ CentOS 6.4


System Configuration Diagram
----------------------------

```
       +--------------------------+
       |                  (node01)|
  +---> eth1                      |
  |    |  10.126.5.18/:prefix_1st |
  |    |  10.126.5.17/:prefix_2nd |
  |    +--------------------------+
  |
ping 10.126.5.18 # ping1
ping 10.126.5.17 # ping2
  |
  |    +--------------------------+
  |    |                  (node02)|
  +-<-- eth1                      |
       |  10.126.5.19/:prefix_1st |
       |                          |
       +--------------------------+
```


Verification Matrix
-------------------

| node \ prefix | 1st | 2nd | ping1 | ping2 |
|:--------------|:----|:----|:------|:------|
| prefix.24-24  |  24 |  24 |   OK  |   OK  |
| prefix.24-32  |  24 |  32 |   OK  |   OK  |
| prefix.32-24  |  32 |  24 |   NG  |   NG  |
| prefix.32-32  |  32 |  32 |   NG  |   NG  |


Getting Started
---------------

```
$ vagrant up
```
