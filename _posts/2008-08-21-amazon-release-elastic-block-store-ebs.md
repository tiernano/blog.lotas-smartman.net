---
title: Amazon release Elastic Block Store (EBS)
author: admin
layout: post
permalink: /amazon-release-elastic-block-store-ebs/
dsq_thread_id:
  - 26016687
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Its taken a while, but amazon have finally released the [Elastic Block Store][1], their presistant data store for [EC2][2]. The way it works is as follows:

  * you create an EC2 instance as normal
  * you create a EBS Volume, ranging from 1Gb to 1Tb. this costs 10c per gb allocated per month.
  * you mount the EBS Volume on the EC2 instance, do your work, and your sorted.
  * if your Ec2 instance goes down, your EBS volume is still there and so is your data. just mount it on a new EC2 instance and Bobs your uncle.

there is already a post on the developer connection center showing you [how to get MySQL working with EBS][3]. 

another feature is snapshots. you can backup your EBS volume to S3 using their snapshot system. you are charged the usual S3 costs for the snapshot hosting, but everything is compressed before it gets to S3. so, say you have a 20Gb volume with only 4 gb of files. this could be compressed to only 3gb or less, depending on the compression. 

Anyway, this is very cool stuff. more info and pricing is [available here][4].

 [1]: http://developer.amazonwebservices.com/connect/ann.jspa?annID=329
 [2]: http://www.amazon.com/ec2
 [3]: http://developer.amazonwebservices.com/connect/entry.jspa?categoryID=100&externalID=1663
 [4]: http://www.amazon.com/b/ref=sc_fe_c_0_201590011_1?ie=UTF8&node=689343011&no=201590011&me=A36L942TSJ2AJA