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
ping 10.126.5.18
ping 10.126.5.17
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

| node \ prefix | 1st | 2nd |
|:--------------|:----|:----|
| prefix.24-24  |  24 |  24 |
| prefix.24-32  |  24 |  32 |
| prefix.32-24  |  32 |  24 |
| prefix.32-32  |  32 |  32 |


Getting Started
---------------

```
$ vagrant up
```
