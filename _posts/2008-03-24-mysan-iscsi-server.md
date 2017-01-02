---
title: MySAN iSCSI Server
author: admin
layout: post
permalink: /mysan-iscsi-server/
dsq_thread_id:
  - 26006787
  - 26006787
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
**[Updated 2011-08-05]** This is quite a popular post, so i though i should update it. Seems that Nimbus Data has made MySAN dead&#8230; I have found 2 Free alternatives though: Starwind Software have a [free edition of their iSCSI Target][1]. Has some nice features on their site (Disclaimer: I have NOT tested it, yet) and you cant argue with FREE! Also, Microsoft have released their iSCSI target for Free also. More details on the [Microsoft Virtualization Blog here][2].

iSCSI is one of these thing I have heard about, but for one reason or another, always though "too expensive". Well, I was wrong. Very wrong. Check out [Nimbus Data System&#8217;s MySAN iSCSI Server][3]. Its FREE! download, install of a Win2k3 server, tell it what you want to share out (I think you share out Full drives, not partitions, but I have to check that out) and its good to go.

you then use your client ([Windows Server 2003][4] and [Vista][5] have one in box, and I would think [Longhorn Server][6] would too&#8230; OSX, that&#8217;s another question for later) to mount the share, and your good to go. I wonder (since I haven&#8217;t installed it just yet) is it shared? Like could I have 2 machines mounting the same disk? Cause I have an idea, and here goes the rant!

Right, so I have 2 (at the moment, soon to become 3) media centers in the house. They all record TV shows, and all are plugged into different Digiboxes. Each machine has a finite amount of storage (my media center in my room has 3 hard disks: 2 120gbs and an 80gb. the MCE down stairs has 250Gb. the third has about 400&#8230;).

Anyway, what I would like set up is a large(ish) server somewhere with, say, 4 500Gb hdds (plus an OS drive) and a RAID card. the 4 hdds are setup in RAID 5, and the storage is then served over iSCSI. Each MCE then mounts the iSCSI storage over network, and uses that as a place to record and view TV shows.

So, I set something to record in my room, get home, be too lazy to go upstairs and watch it, but can watch from the comfort of the front room. Or, see something I want to record for someone else (with an MCE in the house) and record it, so they can watch later.

Its defiantly a cool idea. Other things that it could be used for: Backup of VM&#8217;s. Moving of VM&#8217;s between servers. so, you would have some sort of monitoring system, and watch the load of your VM&#8217;s. You then have 2 or 3 Virtual Server systems that run these VM&#8217;s. You find that the load on one of these boxes is getting too high, so you shut down one of the VM&#8217;s, and boot it on a different box. GigE Networking would be needed for most of this&#8230; it could be handy if a VM Server machine has to go down for malignance too.

[update] fixed their URL, since this is quite a popular post.

<table>
  <tr>
    <td>
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td>
    </td>
    
    <td>
    </td>
  </tr>
</table>

 [1]: http://www.starwindsoftware.com/starwind-free
 [2]: http://blogs.technet.com/b/virtualization/archive/2011/04/04/free-microsoft-iscsi-target.aspx
 [3]: http://www.nimbusdata.com/products/mysan.php
 [4]: http://www.microsoft.com/windowsserversystem/
 [5]: http://www.microsoft.com/vista
 [6]: http://www.microsoft.com/windowsserver/longhorn/default.mspx