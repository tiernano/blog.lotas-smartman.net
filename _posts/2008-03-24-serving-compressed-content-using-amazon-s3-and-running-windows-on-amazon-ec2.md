---
title: serving compressed content using Amazon S3 and running Windows on Amazon EC2
author: admin
layout: post
permalink: /serving-compressed-content-using-amazon-s3-and-running-windows-on-amazon-ec2/
dsq_thread_id:
  - 26015652
categories:
  - Uncategorized
---
So, a couple of Amazon AWS related articles i found today and wanted to post about. the first is an article showing you how to serve [compressed content][1] (think CSS and JS files) from Amazon S3. This could be extreamly handy. the article talks about problems if your web browser does not support compression, so it may not be for everyone, but handy none the less! Next is this How-to forge article showing you [how to run Windows on an EC2 instance][2]. this idea really interests me. Since Amazon give you 1.75Gb of RAM for your instance, you could have 3 instances with 512mb each, or with 256 (actually, you could have 7, but leave memory for the main system). theoretcially, you could have 6 windows boxes running on just 2 AMIs, which would mean that for about $150 a month, you would have 6 full Windows machines online, 24/7. now, obviously, some sort of backup system would be required (incase of an AMI rebooting, or the real hardware on the AMI going down) but thats only $25 a month (less bandwidth and S3 costs) for a full Windows machine&#8230; Not bad! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://devblog.famundo.com/articles/2007/03/02/serving-compressed-content-from-amazons-s3
 [2]: http://howtoforge.net/amazon_elastic_compute_cloud_qemu