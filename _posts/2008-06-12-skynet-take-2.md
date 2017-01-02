---
title: SkyNet, take 2
author: admin
layout: post
permalink: /skynet-take-2/
dsq_thread_id:
  - 26016644
categories:
  - Uncategorized
---
So, a few days ago, i mentioned the [SmugMug SkyNet][1] system they have running for photo and video processing. Well, today i started to think about it a bit more, but not with virtual machines, but more physical machines. i suppose Virtual Instances could be used aswell, but physical hardware is what started me thinking, and he is my theory:

It all starts with the Physical machine. I am thinking the Mac Mini (or, a couple of these) since they [make good HPC clusters][2]. You get a few of these runnning, say, Windows Server 2008, and enable [Wake On Lan][3]. this is one of the important parst. 

Next, a Windows service should be installed on each of the machines which talks to a central head node. this head node is also the cluster head. if there are no items in the cluster queue, it sends a message to the machines to go to sleep (shutdown). all machines then are completly off, using no power at all. You then need a task done and you send it to the cluster head. if there are more items to be processed than machines, all machines are fired up and start processing. If there are less, only the required number of machines are kicked off. and when the queue empties, the machines start to get shut down again!

now, this is one of those chalanges which would not be too hard to actually do. the problem is more around working out cost savings. but, lets do some estimates&#8230;

Apple lists the 1.8Gz Dual core Mac Mini (i think this is the Core Duo since its "from late 2006") as 2[3W @ idle and 110W @ full load.][4] given the new Mac Minis have more ram, processor power and hard drives, etc, i am going to estimate (and if i am wrong, please comments) that the NEw 2Gz Core 2 Duo Mac mini uses 25w @ idle and 120w @ full load.

We will also assume your a bit mad and have 16 of these in your home cluster (a little over 8 grant, 32 cores, up to 32Gb of ram and a load of storage&#8230;). 

so, if the machines are idle for 20 hours a day, and your cost per KW/H is 12c, for all 16 machines to run idle all day, it will cost you 96c&#8230; doesent sound like a lot though does it&#8230; but thats only 16 machines, and thats not including the saving on Air con&#8230; 

Also, this is only for Mac minis. if your using bigger, larger machines, which could use 80&nbsp; &#8211; 120 w of power at idle, your talking EUR3.06 to EUR4.60 per day in electric! neadless to day, the less idle time, the less youll save&#8230; shutting down 16 mac minis idle for 1 hour a day will only save you about 5c&#8230; 

i suppse the next question you have to ask your self is why? with virtualization being a big thing now, why have loads of full machines running? it could be procesisng power. if you need a lot of stuff processed, and its going to need 50 or 60 CPUs to run on at 100%, then sticking it on a machine with 8 cores aint going to solve anything&#8230; but sticking it on 32 mac minis, each with dual cores, could be handy&#8230;. Hmmm&#8230; starting to wonder about shutting down Virtual Hosts when load goes down&#8230; 32 mac minis, each dual core, running 64 instances to start. as instances are not needed any more, they are shutdwn using the Virtualization API (Hyper-V and PowerShell). when all a hosts instances are down, shut down the host till its needed again&#8230; youll be waiting a little longer for the whole thing (host and instance) to boot, but it would definatly save power!

 [1]: http://blog.lotas-smartman.net/don-macaskill-on-skynet/
 [2]: http://blog.lotas-smartman.net/mac-mini-as-a-hpc-compute-cluster/
 [3]: http://en.wikipedia.org/wiki/Wake-on-LAN
 [4]: http://docs.info.apple.com/article.html?artnum=304952