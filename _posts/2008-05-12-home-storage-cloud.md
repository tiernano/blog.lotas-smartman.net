---
title: Home Storage Cloud?
author: admin
layout: post
permalink: /home-storage-cloud/
dsq_thread_id:
  - 26016567
  - 26016567
categories:
  - Uncategorized
---
Is it posible to build a home cloud storage system with spare storage from machine? and if not, why not? since we all need large amounts of storage for different things, and we dont want our storage "disapearing" any time soon, a distributed file system over multiple machine, all backed up to each other, would make life very cool&#8230; but would it work?

some thinking behind this:

take my network as an example. I have my main workstation, with 300Gb internal storage and 2 300Gb external drives. My old media center has 200Gb of storage. i have a Dual Opteron server with 160Gb storage, a PowerEdge server with 80Gb and an old IBM server with 3 18Gb SCSI Drives. Total storage, just in my room and on, is nearly 1.4Tb.

now, say that i could add storage from the machines to a storage pool, as much as i want. i would add, say, 500Gb from the main workstation, 100Gb from the old media center, 60 from the opteron, 20 from the poweredge and 36 from the old SCSI Box. that, as RAW data, weights in at 716Gb. using some sort of RAID system, depending on the way its setup, you could have (assumptions made below):&nbsp;

716Gb Striped (RAID 0)  
356Gb Mirrored (RAID 1)  
713.99Gb RAID 5  
711.99Gb RAID 6  
711.99Gb RAID 50

the assumptions i made are as follows:

split all storage into 2Gb chunks. if you have a 100Gb partition, the "system" may see it as 50 2Gb "drives".

i used a [RAID Calculator here][1]. total storage was 716Gb, giving me a total of 356 2Gb units.

RAID 6 may be the best option, since it will accept more than 1 drive failure. only issue i can see is if you have a very large machine with lots of storage, and a physical drive with lots of these "disks" fail, your screwed as a lot of data is lost. RAID 10 may be better, but then you may want to make sure your total pool is no larger than your smallest machine&#8230; which would not be great. in my example above, the smallest machine is 20Gb. thats not a lot of storage to share. i am starting to think that cloud storage works best if it is left in the cloud&#8230;.

 [1]: http://www.icc-usa.com/store/pc/viewContent.asp?idpage=7