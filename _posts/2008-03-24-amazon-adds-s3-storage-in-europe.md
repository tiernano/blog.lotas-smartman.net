---
title: Amazon adds S3 storage in Europe
author: admin
layout: post
permalink: /amazon-adds-s3-storage-in-europe/
dsq_thread_id:
  - 26016283
categories:
  - Uncategorized
---
This morning, amazon has added [S3 storage options in Europe][1]. What does that mean? Well, instead of your data being hosted in the US, you now have the option of storing it in Europe. Not sure exactly where the data center is, just yet, but not having&nbsp;to cross the ocean is going to reduce the time to upload and download data.

couple of things: 1, its more [expensive to host data in Europe][2]. its not &#8220;much&#8221; more expensive, but more, none the less. 18c per gig hosted, compared to the 15c in the US. transfer is the same price, but the request charge is more too. 0.012c per 1000 put or get requests, compared to 0.01c in the US. Also, data between S3 Europe and EC2 will be charged, so its not free like in the US.

now, this sounds like a step in the right direction, but its slightly off. I don&#8217;t want to have to upload data twice for it to be replicated over the US and European data centers. second, a second US data center would be very nice to have, and third, a Data center in Asia would make their CDN complete. This about it this way: I have an image I would like storage and served from Amazon S3 (both Europe and US). I need to upload this twice, and call different URLs (I think) for this to come from the different centers. IF amazon did that work (I upload once, with a replicate tag, and I only pointed to one address) it would be very sweet. upload once, serve anywhere! We can all hope and pray&#8230;

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:474a8955-b421-4166-bb52-fac2e6ed87d4" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/CDN" rel="tag">CDN</a>, <a href="http://technorati.com/tags/Amazon" rel="tag">Amazon</a>, <a href="http://technorati.com/tags/S3" rel="tag">S3</a>, <a href="http://technorati.com/tags/EC2" rel="tag">EC2</a>, <a href="http://technorati.com/tags/Europe" rel="tag">Europe</a>, <a href="http://technorati.com/tags/Datacenter" rel="tag">Datacenter</a>
</div></p>

 [1]: http://developer.amazonwebservices.com/connect/ann.jspa?annID=242
 [2]: http://www.amazon.com/gp/browse.html?node=16427261