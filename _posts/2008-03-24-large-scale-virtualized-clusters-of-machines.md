---
title: Large scale Virtualized Clusters of machines
author: admin
layout: post
permalink: /large-scale-virtualized-clusters-of-machines/
dsq_thread_id:
  - 26016244
categories:
  - Uncategorized
---
Ok, this is something I have been wanting to post about for a while now, but never got around to it. Either time, or laziness has gotten in the way. But tonight, I have decided to work on this. 

This post is about large scale Virtualized platforms for building and deploying services. companies like Google use [commodity, off the shelf hardware for building their networks][1]. but they use thousands of machines. how would you build a farm of, say, 64 nodes, with just 8 machines? this is what this post is about. 

I am not going to talk about stuff I have tried to build, as I don&#8217;t have the hardware required, but I will talk theoretical ideas here, some things I have thought about building, and other random stuff I think about. 

So, firstly, the hardware. I have been checking prices of processors, motherboards and storage (RAM/Hard Disk) and things are quite cheap at this stage. a Quad core Intel Core 2 Quad processor will set you back (at time of writing) EUR255. For this price, you get a Quad Core 2.4Gz processor, with 8Mb cache, 64bit enabled and built in Virtualization Technology (which is very important, and I will go into that soon). a motherboard that will take one of these processors will set you back about EUR100, and 2 2Gb DDR2 PC5300 DIMMs (of which we will need 2 sets, again more on that later), will set us back EUR150, so EUR300 for the 2 sets. Ideally, we want a board that has onboard video, since these machines will be acting as servers, and I don&#8217;t want to spend extra of graphics. 

Next, storage. We don&#8217;t need CD/DVD ROM drives (we can use [Windows Deployment Services][2] for installing boxes), but we will need hard drives. 2 500GB, 7200RPM Drives should do the job. cost: EUR95 each. Finally, power and cases. We are going to cheat with the cases and just leave them out of a case. this has the advantage of being cooler, since there is no case to duct air around. it will be open in the rack. we just add cooling to the rack its self, and we should be sorted. for PSUs about EUR70 for a 530 watt power supply should do the job. 

So, currently, that works out at about 915EUR per box. For that we are getting a Quad core, 64bit box, with 8Gb of RAM and a 1Tb of RAW storage with a GigE net connection. 

Next, the software. I am thinking [Windows 2008 Server][3] [Core][4] should be installed on this box. with this, [Viridian][5] should be setup and installed, and on a machine, either in the cluster, or external, a copy of [System Centre Virtualization Machine Manager 2007][6] should be installed for management of the cluster. Deploying servers, moving them around, starting and stopping services, etc, will be extremely easy from here on in. 

For a website starting off, you could start with 2 of these machines, each running a Web Service Instance, a DB instance and a backend system of some sort. maybe have a virtual load balancer in between the web and your servers. that&#8217;s 4 Virtual Machines per machine. You can then add machines as you see fit, or as are required. this could then scale to 8 of these machines, each running a couple of instances of web server hardware, a backend system and maybe even a DB. 

Now, I know there are companies out there ([Amazon][7] and [Flexiscale][8]) that will do this, to an extent, for you. you need a new machine, and using an API, you can build it and deploy it. plus there is no money down on that kind of project, but if you want to chance your arm and build a large cluster of Virtual Machines, maybe for an internal project, this would work. I think&#8230; 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:f1de9d43-f6f1-43fa-83a8-f6884204d3c6" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/Virtualization" rel="tag">Virtualization</a>, <a href="http://technorati.com/tags/Clusters" rel="tag">Clusters</a>, <a href="http://technorati.com/tags/Windows%202008" rel="tag">Windows 2008</a>, <a href="http://technorati.com/tags/Viridian" rel="tag">Viridian</a>, <a href="http://technorati.com/tags/Amazon" rel="tag">Amazon</a>, <a href="http://technorati.com/tags/Flexiscale" rel="tag">Flexiscale</a>, <a href="http://technorati.com/tags/Google" rel="tag">Google</a>, <a href="http://technorati.com/tags/Commodity%20Hardware" rel="tag">Commodity Hardware</a>
</div>

 [1]: http://en.wikipedia.org/wiki/Google_platform
 [2]: http://www.microsoft.com/windowsserver2008/deployment/services.mspx
 [3]: http://www.microsoft.com/windowsserver2008/default.mspx
 [4]: http://www.microsoft.com/windowsserver2008/servercore.mspx
 [5]: http://www.microsoft.com/windowsserver2008/virtualization/default.mspx
 [6]: http://www.microsoft.com/systemcenter/scvmm/default.mspx
 [7]: http://www.amazon.com/ec2
 [8]: http://www.flexiscale.com/