---
title: Amazon EC2, Amazon S3, Microsoft Virtual Server, Windows Server and other random thoughts
author: admin
layout: post
permalink: /amazon-ec2-amazon-s3-microsoft-virtual-server-windows-server-and-other-random-thoughts/
dsq_thread_id:
  - 26015506
  - 26015506
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
This is something I have been thinking about for a while now. When Amazon&nbsp;announced EC2, the first think I though was &#8220;What about .NET and ASP.NET?&#8221; yes, you can run Mono on Linux, but I want a full Windows box! So, it got me thinking, and my thinking has gotten me this far:

You have a couple of large machines on your network. each with a couple of processors, lots of RAM, and a fair whack of hard drive space. each of these then are partitioned up into virtual machines using Virtual Server. with the help of the [Virtual Server clustering How To][1], [WAIK][2], iSCSI or SAN Storage, and some scripting, you could easily(or semi easily) get a system that could be very scaleable. 

So, lets say you start with 4 big boxes (Dual proc, Dual Core, 8Gb ram, couple large, fast HDD&#8217;s). Install Win2k3 Server on these, Virtual Server, and some base scripts. Each box then starts to download their base Virtual Images (DB server, Web Server, Application Server, etc) and leaves them on their local machine. So, the DB gets configured for fail over, load balancing and clustering support. each web server and each app server downloads (either from local or S3) the latest build of the site and application service. and they start up. You may also have load balancing machines and 1 or 2 co-ordination servers (these make sure DNS is up to date, etc. actually could be done by the Load Balancer). 

So, the 4 large boxes are running, each has a DB server, 2 web servers,&nbsp;an app server and a load balancer. all load balancers know about each web server and each app server. The DB servers know about each other. 

Everything is working grand, and load starts to increase. you decided to get an extra few machines. these come with same specs as the old one. Use a WAIK system, you boot the machine, and it automatically runs your script (install Win2k3 server, Virtual Server, updates, and latest VM images). then each image boots, runs though its script (download latest app service or web site, or connect to SQL cluster and get data). then the Web Sites and app servers tell the load balancer &#8220;I&#8217;m here&#8221; and start getting hit with traffic. 

So, this is a big rant on the idea, but no actual proof it works. That&#8217;s my next task. now, if only Amazon would add windows to the supported OS list on EC2&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

&#8211;Tiernan

&nbsp;

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:7618d80f-2f3f-4a56-9644-156d2f0b398d" style="padding-right:0px;display:inline;padding-left:0px;float:none;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati tags: <a href="http://technorati.com/tags/S3" rel="tag">S3</a>, <a href="http://technorati.com/tags/EC2" rel="tag">EC2</a>, <a href="http://technorati.com/tags/Windows%20Server" rel="tag">Windows Server</a>, <a href="http://technorati.com/tags/Virtual%20Server" rel="tag">Virtual Server</a>, <a href="http://technorati.com/tags/Amazon%20S3" rel="tag">Amazon S3</a>, <a href="http://technorati.com/tags/Amazon%20EC2" rel="tag">Amazon EC2</a>, <a href="http://technorati.com/tags/Amazon%20AWS" rel="tag">Amazon AWS</a>, <a href="http://technorati.com/tags/Web%202.0" rel="tag">Web 2.0</a>, <a href="http://technorati.com/tags/Load%20balancing" rel="tag">Load balancing</a>, <a href="http://technorati.com/tags/n-Tier%20Applications" rel="tag">n-Tier Applications</a>
</div>

 [1]: http://blog.lotas-smartman.net/archive/2007/01/25/virtual-server-2005-r2-host-clustering-howto.aspx
 [2]: http://www.microsoft.com/downloads/details.aspx?FamilyID=c7d4bc6d-15f3-4284-9123-679830d629f2&DisplayLang=en