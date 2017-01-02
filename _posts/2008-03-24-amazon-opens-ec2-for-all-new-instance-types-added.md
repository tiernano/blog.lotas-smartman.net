---
title: Amazon Opens EC2 for all, new instance types added
author: admin
layout: post
permalink: /amazon-opens-ec2-for-all-new-instance-types-added/
dsq_thread_id:
  - 26016275
categories:
  - Uncategorized
---
Good news from the Amazon EC2 team. On their Developer Connection Forum, they have [just announced][1] that EC2 is now open to all, which is cool, and they now have a total of 3 instance types: 

  * Small: which is the standard 1.7Gb memory, 1 EC2 Compute Unit (more on that later) and 160Gb hdd. this is 32bit only, and still goes for 10c per hour.
  * Large: 7.5Gb RAM, 4 EC2 Compute Units (2 virtual cores with 2 compute units each), 850Gb storage and 64bit processing. this goes for 40c per hour.
  * Extra Large: 15Gb memory, 8 EC2 compute cores (4 virtual cores with 2 EC2 compute units each), 1680Gb storage and 64 bit processing. price: 80c per hour. 

But, i hear you ask, what is a EC2 Compute Unit? Amazon has [info here][2]. Originally, they said it was a 1.7Gz Xeon. but as they say in their documentation, its a 1.7Gz early 2006 Xeon. now, they say, its the equivalent of a 1-1.2Gz 2007 Opteron or 2007 Xeon. 

So, this is pretty cool. the opening of EC2 will hopefully get more people working on it, and might get Amazon to add a [SLA to it like they just did to S3][3]. It may also push them to get some sort of EC2->S3 bridge which auto backs up instances. 

[update] [AWB Blog has a bit more on this.][4]

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:b3e43e29-6f49-4e7a-aabe-236841622344" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/EC2" rel="tag">EC2</a>, <a href="http://technorati.com/tags/S3" rel="tag">S3</a>, <a href="http://technorati.com/tags/64Bit" rel="tag">64Bit</a>, <a href="http://technorati.com/tags/Amazon" rel="tag">Amazon</a>, <a href="http://technorati.com/tags/AWS" rel="tag">AWS</a>, <a href="http://technorati.com/tags/Compute%20Unit" rel="tag">Compute Unit</a>, <a href="http://technorati.com/tags/SLA" rel="tag">SLA</a>
</div></p>

 [1]: http://developer.amazonwebservices.com/connect/ann.jspa?annID=241
 [2]: http://www.amazon.com/gp/browse.html?node=201590011#measure
 [3]: http://www.amazon.com/b?ie=UTF8&node=379654011
 [4]: http://aws.typepad.com/aws/2007/10/amazon-ec2-gets.html