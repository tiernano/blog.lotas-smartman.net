---
title: iSCSI Stuff
author: admin
layout: post
permalink: /iscsi-stuff/
dsq_thread_id:
  - 26015967
  - 26015967
categories:
  - Uncategorized
---
Well, this iSCSI stuff has intrigued me for a long time now. and its starting to make more and more sense. I have started to see more advantages of using it, and better ways of implementing it on my network. 

Take for example my PowerEdge server running as Exchange/Web/SQL box. this machine is on 24/7 and is pretty important to have live. but its limited in the amount of storage I can physically add to it. If I stick in a new GigE net card (it has one already) and leave it alone, I can remotely add extra storage by placing it in a larger server and let the PowerEdge take&nbsp;storage from that. If I want to migrate my SQL Server to a new box, just take the SQL server down on the PowerEdge, disconnect the iSCSI drive, reconnect it on the new box, and let SQL server do its magic. its now on a new machine, and that&#8217;s it. 

Mind you, I do know there will be problems. 

  1. even GigE network can be slow. it will max out at 125mb/s (if your lucky) and cached reads from hardware can be faster.&nbsp;
  2. More points of failure. now if the iSCSI drive does down, the network is screwed.

but there are more advantages.

  1. Single place for backups.
  2. Only one RAID array, on the storage box, is required.

Anyway, here are some links, which might be handy:

Byte and Switch has an article on [How to build an iSCSI Disk Array][1]. 

Josh Maher has a post talking about [Exchange 2007 on iSCSI storage][2]. again handy.

[EmBoot][3] is a company with a couple of interesting products: winBoot/I and netBoot/I. These allow a machine to boot over iSCSI using just a standard network card. 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:3f4a3840-6571-46fb-b58b-da2921de0da9" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/iSCSI" rel="tag">iSCSI</a>, <a href="http://technorati.com/tags/EmBoot" rel="tag">EmBoot</a>, <a href="http://technorati.com/tags/Exchange" rel="tag">Exchange</a>, <a href="http://technorati.com/tags/Disk%20Array" rel="tag">Disk Array</a>, <a href="http://technorati.com/tags/SQL" rel="tag">SQL</a>, <a href="http://technorati.com/tags/Storage" rel="tag">Storage</a>
</div>

 [1]: http://www.byteandswitch.com/document.asp?doc_id=96342&WT.svl=spipemag2_1
 [2]: http://joshmaher.wordpress.com/2006/08/03/exchange-2007-on-iscsi-storage/
 [3]: http://www.emboot.com/