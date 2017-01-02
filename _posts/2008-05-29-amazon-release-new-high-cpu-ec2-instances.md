---
title: Amazon release new High-CPU EC2 Instances
author: admin
layout: post
permalink: /amazon-release-new-high-cpu-ec2-instances/
dsq_thread_id:
  - 26016609
  - 26016609
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
[Amazon has released][1] some new EC2 instances which are aimed at users who require more CPU power. there are 2 new instances: 

***High-CPU Medium Instance*** 

1.7 GB of memory  
5 EC2 Compute Units (2 virtual cores with 2.5 EC2 Compute Units each)  
350 GB of instance storage  
32-bit platform  
I/O Performance: Moderate   
**Price: $0.20 per instance hour**



***High-CPU Extra Large Instance*** 

7 GB of memory  
20 EC2 Compute Units (8 virtual cores with 2.5 EC2 Compute Units each)  
1690 GB of instance storage  
64-bit platform  
I/O Performance: High  
**Price: $0.80 per instance hour**

&nbsp;

A list of all Instance types now provided is [available here][2].

It has started to make me wonder though; will amazon release a low CPU instance? there are users out there wanting to start small sites who would not want to spend a lot of money on a couple of EC2 instances, but would like to build &#8220;in the cloud&#8221;. but, things could get expencive. For example, the the following as an example:

1 Load Balancer (small instance): 10c X 24 hours a day X 31 days = $74.40

2 Web Servers (small instance): 2 X 10c X 24 hours a day X 31 days = $148.80

(minimum) 1 App Server (Large Instance): 1 X 40c X 24 hours a day X 31 Days = $297.60

2 DB servers (Large instance): 2 X 40c X 24hours a day X 31 Days = $595.20

Total cost: $1116, excluding bandwidth costs and S3 hosting costs&#8230;.

Now, the example above is a &#8220;theoretical&#8221; Web2.0 website. not all sites are going to &#8220;need&#8221; all that hardware. you could probably get away with 1 web server, an app server and a single DB server. Hell, you could get away with 1 instance! but, if you want to build a scalable web site which can cope with being Dugg, then you may need this. you may even need more&#8230; If it where my Web2.0 startup on the line i would want:

2 Load Balancer (small instance): 2X 10c X 24 hours a day X 31 days = $148.80

4 Web Servers (small instance): 4 X 10c X 24 hours a day X 31 days = $297.60

2 App Server (Large Instance): 2 X 40c X 24 hours a day X 31 Days = $595.20

2 Dedicated Memcached Servers (Large Instances): 2 x 40c X 24 hours a day X 31 Days = $297.60

2 DB servers (Extra Large instance): 2 X 80c X 24hours a day X 31 Days = $1190.40

Total cost: $2827.20, excluding bandwidth costs and S3 hosting costs&#8230;.

 [1]: http://developer.amazonwebservices.com/connect/ann.jspa?annID=321
 [2]: http://www.amazon.com/Instances-EC2-AWS/b/?ie=UTF8&node=370375011