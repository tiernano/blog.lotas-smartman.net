---
title: BITS transfer over Remote Desktop with Powershell
author: admin
layout: post
permalink: /bits-transfer-over-remote-desktop-with-powershell/
dsq_thread_id:
  - 
dsq_needs_sync:
  - 1
categories:
  - HowTo
---
So, I have a dedicated server and the machine acts as a Hyper-V host. Only Remote Desktop is enabled on the box, for security, but the VMs have their own ports open (HTTP, SSH, etc). Transferring files between the Dedicated Server and my home network is a bit of a pain&#8230; one way is to open a port locally (SSH or FTP) and download the file from home to the dedicated box&#8230; bit of a pain, but it does work&#8230; But now i have found some magic in BITS Transfer!

Bits Transfer allows you to download and upload files in the back ground, intelligently&#8230; Hence the full name of Background Intelligent Transfer Service&#8230; So, how to you get this to work with Remote Desktop? 

In the Remote Desktop Client, under the Local Resources Tab, under Devices and Resources, click the &#8220;More&#8221; option and select the drives you want to share out to your server. Remember, the server has access to these files&#8230; I am not sure if everyone on the server can see them, so be careful. Connect to your server and go into Computer&#8230; you should, by default, see your extra drives&#8230; they dont have real drive names though&#8230; So, what you need to do is go to the address \\tsclient (should be always the same&#8230;) and you will see the drives you have shared. find the drive your interested in, find the exact file you want to copy over an Shift+Right click on the file. You will see an option to Copy As Path. Click this. Next, Open PowerShell (Should be installed on all servers, if not [Google for it with Bing][1] and find out how to install it. Once powershell is either opened or installed and opened, type &#8220;Import-Module bitstransfer&#8221;. now for the magic commands: 

  
**Start-BitsTransfer -source $sourceFile -destination $localtionFile**  
That is it&#8230; set $sourceFile to the URL of the file you want to download, and $locationFile to the place you want it placed. Powershell will show an progress bar of how the transfer is doing&#8230; But, what happens if the connection drops before the download finishes? Simple. Open your connection again, you should see your original powershell window. In here type:  
Get-BitsTransfer | Resume-BitsTransfer  
Now, this is looking for ALL bits transfers on the system, and then resuming them&#8230; You may want to check and see what Get-BitsTransfer shows as a result&#8230; In my case, i only want to start the jobs which are marked as having an error &#8220;TransientError&#8221; so my PowerShell Command is:  
**Get-BitsTransfer | Where-Object {$_.JobState -eq &#8220;TransientError&#8221; } | Resume-BitsTransfer**  
You could also use the Job ID if you have one (in my screen, its being truncated&#8230;) 

So, What about downloading FROM the server to your local machine? Well, in the Start-BitsTransfer, swap the source and destination&#8230; Source is a local file on your server and destination is the fileshare on TSClient you want to upload to&#8230; and the resume upload and download will work to.

Another interesting option is to add the -Asynchronous option to the Start-BitsTransfer command. This will run the command fully in the background. there is aslo the option of using the -Suspend, which only adds the job, but does not start it immediately. In this case you can see some info about the download using the Get-BitsTransfer command. Finally, you need to run one final command: Complete-BitsTransfer. So, You would call  
**Get-BitsTransfer | Where-Object {$_.JobState -eq &#8220;Transferred&#8221; } | Complete-BitsTransfer**  
As the [MeerKat says, Simples! ][2]

**[UPDATED]** Want to monitor the progress of the download? **bitsadmin /monitor** will show you the status of your transfer! Handy!

 [1]: http://www.bing.com
 [2]: http://www.comparethemeerkat.com/