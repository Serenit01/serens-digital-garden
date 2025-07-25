---
{"dg-publish":true,"permalink":"/1-knowledge/concepts/servers/raid-configuration/","created":"2025-07-25T10:58:51.739+10:00","updated":"2025-07-25T11:32:35.303+10:00"}
---

RAID stands for "Redundant Array of Independent Disks". It is the configuration of the hard drives within your server that can prevent data loss should one of your drives fail. 

There are 5 types of RAID configurations you can choose from and all have their own pros and cons. 

### RAID 0
This config is not fault tolerant and you can lose data should one of your disks fail.
The data is split/striped between the different disks, so if one dies all the data will be list. The only reason you would use this config is for speed, as, since the data is split between two disks instead of one, it's a lot faster. 

### RAID 1
This one is fault tolerant. The data is copied on each disk, so if one dies the other disk has a duplicate of all the data.

### RAID 5
This one requires 3 or more disks. The data is striped/split across multiple disks alone with [[parity 🌱\|parity 🌱]]. Parity is used to rebuild the data in the event of a disk failure.
The parity takes up some disk space though. Say you have four 1TB disks, only 3TBs would be usable for data storage as the equivalent of one entire disk would be used to store the parity. 

### RAID 6
Raid 6 is the same as RAID 5, but it can handle two disk failures at the same time instead of one.


### RAID 10
Raid 10 combined RAID 1 and RAID 0. You need a minimum of 4 disks.
Two of your disks are mirrored to the other two disks using a RAID 1 setup, and then both sets of the two disks are striped/split using RAID 0. So you get speed and fault tolerance with this setup. However, you can only used 50% of your entire storage capacity for this config. 



#### Backlinks:
Sources:
[[2. Sources/Videos/What is RAID 0, 1, 5, & 10 By  PowerCert Animated Videos\|What is RAID 0, 1, 5, & 10 By  PowerCert Animated Videos]]


Notes:
