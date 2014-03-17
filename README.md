Linux: IP address netmask
=========================

System Requirements
-------------------

+ CentOS 6.4


Verification Matrix
-------------------

| name         |  1st |  2nd |
|:-------------|:-----|:-----|
| prefix.24-24 |  24  |  24  |
| prefix.24-32 |  24  |  32  |
| prefix.32-24 |  32  |  24  |
| prefix.32-32 |  32  |  32  |


System Configuration Diagram
----------------------------

```
       +----------------------+
       |              (node01)|
  +---> eth1                  |
  |    |  10.126.5.18/:prefix |
  |    |  10.126.5.17/:prefix |
  |    +----------------------+
  |
ping 10.126.5.17
  |
  |    +----------------------+
  |    |              (node02)|
  +-<-- eth1                  |
       |  10.126.5.19/:prefix |
       |                      |
       +----------------------+
```


Getting Started
---------------

```
$ vagrant up
```
