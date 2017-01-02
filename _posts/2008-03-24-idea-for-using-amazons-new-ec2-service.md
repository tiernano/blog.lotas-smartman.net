---
title: Idea for using Amazons new EC2 service
author: admin
layout: post
permalink: /idea-for-using-amazons-new-ec2-service/
dsq_thread_id:
  - 26015081
  - 26015081
categories:
  - Uncategorized
---
Well, i have an idea on how to use <a HREF="/archive/2006/08/25/13135.aspx">Amazons EC2 Service</a>, but not sure how well it will work. the idea is fairly simple. Podcasting/Video Casting distribution network using BitTorrent. Since [S3][1] already supports BitTorrent support, you upload the file to your S3 account. once there, you post the link to the torrent file in a RSS Feed, which is being monitored by your EC2 servers. they then download and start seeding your file, and keep seeding the file till you tell them to stop. 

since each server has 250mb/s of bandwidth to its name, you have a fair wack of bandwidth at your disposal. each server has access to about 160Gb hdd, so your sorted there too. 

if a machine dies or gets rebooted, and you loose your data (which is one of the caviats of the service) your sorted still because you just have this info in your boot file and your special image.

 [1]: http://www.amazon.com/s3