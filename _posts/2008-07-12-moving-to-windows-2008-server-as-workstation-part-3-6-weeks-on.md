---
title: 'Moving to Windows 2008 server as workstation: Part 3: 6 weeks on'
author: admin
layout: post
permalink: /moving-to-windows-2008-server-as-workstation-part-3-6-weeks-on/
dsq_thread_id:
  - 26016655
  - 26016655
categories:
  - Windows Server 2008 Workstation
---
Ok, so, this post has been delayed for quite some time. in part 1 of this series, i talked about [Media][1]. And in part 2, i talked about [Photography][2]. these where both looking forward, at what could go wrong. Well, part 3 is now looking back. The upgrade of the Mac PRo to run Win2k8Srv happened about 6 weeks ago, and so far, so good. some notes below.

  * Some things i want to play with (Channel 4 On Demand, Sky Player) wont work, but thats not because of Windows Server. thats because they dont play nice with 64 bit machines. This sucks! When will Channel 4 or Sky get proper developers in and fix the problem? 
  * Hyper-V rocks, but as a solution to the above problem, well, its not. Hyper-V does not have a sound card, so, no sound&#8230; In reality, makes sense. how many times have you installed a sound card in a server? 
  * the speed of this thing rocks! everything seems faster, responds quicker, and runs more stable. ok, i have had no crashes with Vista, but i have a sense that its more stable&#8230; probably just me&#8230;
  * The iPhone, iPod touch and iPod classic all sync well with iTunes. no problems there. it even talks with my Apple TV without issue! 
  * I havent used the big DSLR camera in a while, but my small point and shoot one works perfect. plug in, download and see everything recorded! very nice.
  * Back to Hyper-V and speed. I currently have 3 VMs running under Hyper-V: Win2k8 Enterprice, Win2k8 Web and a Virtual [Cacti][3] install. Everything still responds quickly, and the only slow down i have is if all 3 VHDs and the host need something of the HDD. Since all are sitting on one single spindle&#8230; This is my problem, and adding more drives should solve it&#8230;
  * all my coding tools work grand on this, and because its a Server OS, i can install a Full SQL Box directly on the machine, which has its advantages!

So, there you have it. all is going well after 6 weeks, give or take. if anyone has any questions, leave a comment!

 [1]: http://blog.lotas-smartman.net/archive/2008/03/21/moving-to-windows-2008-server-as-workstation-part-1.aspx
 [2]: http://blog.lotas-smartman.net/windows-server-2008-workstation/moving-to-windows-2008-server-as-workstation-part-2-photography/
 [3]: http://www.cacti.net/