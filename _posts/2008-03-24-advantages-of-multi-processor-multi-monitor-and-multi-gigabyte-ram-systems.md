---
title: Advantages of multi processor, multi monitor and multi gigabyte ram systems
author: admin
layout: post
permalink: /advantages-of-multi-processor-multi-monitor-and-multi-gigabyte-ram-systems/
dsq_thread_id:
  - 26016035
  - 26016035
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
<img src="http://images.lotas-smartman.net/image.ashx?id=737b65f3-0d60-4258-87e8-4bb114686833" align="right" /> with the advances in computing and processing power, more and more people has access to multi core and multi core + multi proc machines. For example, there are currently no Apple products shipping with less then a Dual core processor. Even the [Mac Mini][1], Apples smallest machine, has a Dual Core Core Duo in it. 

At the&nbsp;moment, I am sitting in front of a Dual processor Dual core machine (the [Mac Pro][2]) and sitting beside a Dual Processor AMD box. The Mac Pro is currently encoding 5 videos (Ripped a DVD as an ISO, and I am currently re-encoding 5 episodes from that DVD to MP4, for XBox360 play back), ripping another DVD, running a mail server in Virtual PC, checking email with outlook, surfing the web with both IE7 and FireFox, and posting this using Windows Live Writer. The whole system is nice and stable, still responsive, and organized, strangely enough. most of the encoding windows are on the second monitor (I have Dual 20&#8243; dell widescreen monitors) and current work items are on the other one. Processor is running at 100% load, there is currently 3Gb of ram being used out of a possible 5,&nbsp; and the machine has been up for the last 51 and a half hours. 

And, after using this for a while, with this kind of performance, it makes me wonder why companies don&#8217;t give honking great machines to their Dev&#8217;s and Engineers. Think about it: you have a honking great dev box, 4 or maybe even&nbsp;8&nbsp;processing cores, 8 &#8211; 16gb RAM, a TB or 2 of HDD (RAID of course) and 2 nice, large monitors (20 &#8211; 30&#8243;). You could have your main Dev machine (say Win2k3, VS2005, SQL 2005, etc) sitting in a Virtual Machine. it could be automatically backed up to a larger network storage area every night at a set time, for safe keeping (keep last 7 days of machines stored there, compressed, for later retrieval, just in case). As well as nightly backups, there should be a base image, for quick restarts, if you want to start fresh. 

You could have a second Dev VM box, for testing new technologies (say, for example this could be running Win2k8, VS Orcas, SQL 2008) which would allow dev&#8217;s to try out new technologies, without having to worry about breaking anything. 

Then, there is the virtualized testing environment, which could have a DB backend, an Application tier, and a front end system. if you want to test with multiple boxes (for failover and load balancing, etc), not a problem. just fire up a couple of extra VM&#8217;s and you should be good to go!

The advantages of this is everything can be separated, and because everything is in Virtual Machines, if anything goes wrong, you can move the VHD to a different box and start it up. Say, a HDD in your dev box goes down and your waiting for Tech Support to replace it. just download the latest image from your network share on to your laptop and your back up and running (probably not as fast as you could have been on your honking dev box, but better then sitting around looking at a blank screen&#8230;).

There have been a lot of studies showing the [advantages of Multi Monitor systems][3], so i wont go into detail on it here, but in a development or engineering environment, you can be working on something on one screen, and see the results on another. 

Comments welcome! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:9cc3c4ac-15aa-4181-8def-10796e22bed8" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Multi%20Processor" rel="tag">Multi Processor</a>, <a href="http://technorati.com/tags/Dual%20Core" rel="tag">Dual Core</a>, <a href="http://technorati.com/tags/Multi%20Monitor" rel="tag">Multi Monitor</a>, <a href="http://technorati.com/tags/Dev%20box" rel="tag">Dev box</a>, <a href="http://technorati.com/tags/Engineering%20Box" rel="tag">Engineering Box</a>, <a href="http://technorati.com/tags/Virtual%20Machines" rel="tag">Virtual Machines</a>, <a href="http://technorati.com/tags/Hardware" rel="tag">Hardware</a>
</div>

 [1]: http://www.apple.com/macmini/
 [2]: http://www.apple.com/macpro
 [3]: http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=286833