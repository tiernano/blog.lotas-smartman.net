---
title: Reverse Tunnel in SSH
author: admin
layout: post
permalink: /reverse-tunnel-in-ssh/
dsq_thread_id:
  - 26013281
categories:
  - Uncategorized
---
Check out this Tech Republic article on how to [setup a reverse tunnel in SSH][1]. I have played with this before and got it to do some interesting things. i used it when i was on a slow 56k dialup link. i connected to a college network i had SSH access to, forwarded port 8080 on my local machine to their proxy server, and compressed the link. when i visited a page, i got a lot faster download because of the compression. mind you, it only worked on text pages and the like, but made browsing a lot faster. it might have helped because of the request comming from the colleges 100mb/s pipe and my compressed SSH connection, insted of over just a standard 56k pipe. Actually, here is [the article i wrote up showing you how to do it][2]. I was going to post this with a question asking was there a way to use this idea on a pocket pc, since my connection on my XDA is limited to 48k/s. Well, i searched google and found [this article showing you how][3]! i will be trying this out, but first i need an SSH server and my own proxy server (which i can probably use my ISA2004 box at home for). This could nearly also act as a &#8220;poor mans VPN&#8221;&#8230; [**update**] Related update. Check out this article showing you [how to install SSHD on your windows machine][4]! very handy. i was actually looking for something simular a while back because i wanted an SFTP server on my LAN for blogger updates to a new page i want to build. This will make life easer! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://techrepublic.com.com/5100-10879-5779944.html?tag=nl.e011
 [2]: http://blog.lotas-smartman.net/archive/2004/02/21/TunnellingoverSSH.aspx
 [3]: http://www.informit.com/articles/article.asp?p=366700&rl=1
 [4]: http://pigtail.net/LRP/printsrv/cygwin-sshd.html