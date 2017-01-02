---
title: 'New Backup plan&#8230; out with Jungle Disk and ZManda Cloud Backup, in with CrashPlan, MySQLBF and SqlBF&#8230;'
author: admin
layout: post
permalink: /new-backup-plan-out-with-jungle-disk-and-zmanda-cloud-backup-in-with-crashplan-mysqlbf-and-sqlbf/
dsq_thread_id:
  - 467475264
dsq_needs_sync:
  - 1
categories:
  - Articles
tags:
  - Backup
  - CrashPlan
  - GodBox
  - iSCSI
  - Jungle Disk
  - Jungle Disk Server
  - MySQL
  - SQL
  - ZCB
  - Zmanda
---
[**UPDATE**: After a few days, i tried CrashPlan Pro on a 30 day trial&#8230; Now i find out that its not available outsite the US and Canada&#8230; Its a bit hiden in their FAQ&#8230; So, back in search i go!]  


My current backup strategy is a long and convoluted one, but it did work… until i shut a lot of stuff down… now i am starting to re-think my plan… first the existing “plan”…

  * my main laptop, a Mac Book Pro, is backed up to my Main Workstation (AKA the GodBox) via iSCSI. The [GodBox][1] is running Windows 2008 R2 Server, and has the [free Microsoft iSCSI Target][2] installed. I am sharing 2 300Gb VHDs to the MacBook Pro, and those are in RAID 1 on the laptop. Time Machine then backs up to this drive. Also, the iTunes Music, Movies, Apps and TV Shows, and also photos from my camera are also backed up to Jungle Disk. Currently this weighs in at about 160Gb…
  * The GodBox itself has a couple of RAIDed Drives (I know, i know… RAID is not backup…). So, my Photos are stored on a RAID 1 array, which is then backed up using Jungle Disk. The photos college is weighing in at about 180Gb or so… probably more.
  * I have a dedicated server in Germany (this is where this site is being served from… Hello from Germany) and that has the actual contents of the site, database, images, etc. these are currently backed up regularly (every 3 hours for a incremental backup, nightly for a Full backup). I am using [ZManda Cloud Backup][3] for this. ZManda has the advantage of backing up SQL and MySQL server, as well as SharePoint and Exchange.
  * There is a machine in the house which acts as an internal Git server (Linux, SSH, Git… simple). [JungleDisk][4] was installed on this and backed up the folder where Git lived. works grand…

So, there are a couple of outstanding issues with this setup:

  * for the amount of data i am storing (About 500Gb give or take) with JungleDisk, its costing me about $80 a month. Its costing me about the same for a Dedicated Server, and it is **about the same cost of a 1Tb drive, every month**!
  * I have logged into the Dedicated server a few times over the last while and found that ZManda was using 900Mb of RAM. Restarting the service solves the issue, but its still a bit of a pain to restart every few days. ZManda released a Version 4 of their ZCB software. I am still on 3.x since MySQL backup was not added to Version 4 yet…
  * If i want to use the same software to backup files around the house, but not in the cloud, ZManda can do it, but JungleDisk cannot.
  * I am using 2 different backup systems…
  * JungleDisk charge $2 per client machine per month, and $4 per server per month (includes some storage with that price… check their site for the latest). Storage is then either charged at about $0.15 per month if you use their API key, or if you use your own, Amazon will charge you… They also use with Amazon S3 or RackSpace Cloud for storage.
  * ZManda is a one off fee per month ($4.95) and you can use that one license to backup as many machines you want. storage is charged at $0.15 per GB, and they are offering 25Gb free… the 25Gb is based on each AWS Region giving you 5Gb free… I suppose since a [new Region just opened in Oregon][5], that could now be 30Gb…

So, i went looking, and i think I found a solution… Some investigation still needed, but we are getting there… here is the plan.

  * The MacBook Pro will still be using TimeMachine to backup to the GodBox using iSCSI, but the plan will be the GodBox gives it 500Gb of storage already RAIDed… Music, Movies, Photos and Apps will be backed up to [CrashPlan][6]. They plan i am looking at will cost me about $12 per month and give me the ability to backup up to 10 machines and gives me Unlimited space… We all know what Unlimited means, but it should be enough… Also, CrashPlan gives me the option to backup to my own machines. So, these files will also get backed up to the GodBox.
  * The Photos and important files on the GodBox will also be backed up to CrashPlan. Less important files, but files i want “safe” will be backed up to my [Drobo][7], which currently has about 4Tb usable. The MacBook Pro files will also be dropped in here.
  * The Server in Germany will get backed up to CrashPlan too…. I am liking this idea already… Very simple. I am going to use 2 pieces of software to backup SQL and MySQL: [SQL Backup and FTP][8] and [MySQL Backup and FTP][9]. Been using the free version for a while, and they do a nice job. Would need to go for the Pro Version (About $50 for MySQL edition and $60 for the MSSQL Edition) but that will backup to a location that CrashPlan will watch, and all the magic will be done then. Any files i want backed up will also end up in CrashPlan.
  * Since CrashPlan allows me to backup up to 10 machines in the cloud, i can add more as needed. Also, machines in the house that would not require cloud or offsite backup can be backed up to other machines in the house without any issues.

This should save me a bit of money over time… My first months outlay will be a little more than my usual JungleDisk bill…. After next month, things should start paying for themself…

Ohhh, and while i am at it, the FREE CrashPlan software allows you to do 95% of what i mentioned above… Actually, more than 95%… the only things it wont do is Cloud Backup (you can still backup to your own machine offsite or a friends machine somewhere) and Backup Sets (Say you want your **Documents in the Cloud, but your Music on internal machines, they could be different backup sets**).

[**Full Disclosure** I am paying full price for the service and software above at the moment (on a 30 day trial for CrashPlan, and looking into the SQL and MySQL backup software currently) so this is just what i am planning on doing, not an advertisement&#8230;]

<table>
  <tr>
    <td>
    </td>
    
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
    
    <td>
    </td>
  </tr>
</table>

 [1]: http://blog.lotas-smartman.net/category/workstation-v-next
 [2]: http://blogs.technet.com/b/virtualization/archive/2011/04/04/free-microsoft-iscsi-target.aspx
 [3]: http://www.zmanda.com/cloud-backup.html
 [4]: http://www.jugneldisk.com
 [5]: http://aws.amazon.com/about-aws/whats-new/2011/11/08/Announcing-new-us-west-oregon-region/
 [6]: http://www.crashplan.com
 [7]: http://www.drobo.com
 [8]: http://sqlbackupandftp.com/
 [9]: http://mysqlbackupftp.com/