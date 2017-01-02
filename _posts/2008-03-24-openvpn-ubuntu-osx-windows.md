---
title: 'OpenVPN +  Ubuntu + OSX + Windows'
author: admin
layout: post
permalink: /openvpn-ubuntu-osx-windows/
dsq_thread_id:
  - 26016390
categories:
  - Uncategorized
---
I have been playing around with VPN stuff for the last few days, and today, finally, I have a VPN up and running! There are a couple of reasons you might want a VPN. Your ISP may be blocking or restricting access to some ports, you may need to access resources (either in your house or in the office) remotely, or you may want a secure connection while on the road (from public hotspots, etc). My reason is the last 2.

I recently got my hands (so to speak) on a Virtual Server in the US, from a company called <a href="http://www.vpslink.com" mce_href="http://www.vpslink.com">VPSLink</a>. This server is very cheap (about $7 a month) but comes with more than enough bandwidth. So, I picked <a href="http://www.Ubuntu.org" mce_href="http://www.Ubuntu.org">Ubuntu</a> as the OS, and set about setting up my VPN.

At first I was looking at [PoPToP][1], which is a standard PPTP server. The reason I wanted this was because no client software would be required for most Operating systems (PocketPC, MacOSX, Windows, etc). I had it working, to an extent (I could connect) but none of my data was getting though. I could not ping the remote server, or get anywhere for that matter. I will eventually go back and look into fixing this, but until then I will use OpenVPN.

<a href="http://openvpn.net/" mce_href="http://openvpn.net/">OpenVPN</a> is an SSL based VPN server. it can tunnel over <a href="http://openvpn.net/howto.html#http" mce_href="http://openvpn.net/howto.html#http">HTTP proxys </a>which may come in handy (<a href="http://www.vodafone.ie" mce_href="http://www.vodafone.ie">Vodafone</a> offer 500mb of bandwidth a month, but only though their proxy server. this could be a way around it).&nbsp; it uses Key Exchange, so no passwords are exchanged. Its very cool, and so far so good. 

If you want to read info on how to get it running, check out the [OpenVPN How to][2]. Also, the Bakers have a post on [how to get it up and running too][3], and [this post has more too][4]. It took me about 3 days to get it up and running, but now it works on both a Windows box (with the help of the [OpenVPN GUI][5]) and on my PowerBook (with the help of [Tunnelblick][6]).

Some notes. On a Mac, Safari does not connect over VPN, or at least on my Mac so far. Firefox, Terminal, Mail, Entourage and the Software Update all do, but Safari is picking my local router&#8230; very strange. Next is the speed. because your packets are being encrypted, etc, there will be an over head on them. because of this you will not see your full bandwidth potential. For example, my connection at home is 6mb/s and I regularly see 650-720kb/s. With this I expect to see 600kb Max, or maybe even less. 

As a final note, VPSLink&#8217;s TOS allow VPN access, but only if its secure, and you are responsible. it is mentioned in [this forum post][7]. the only gripe I have with VPSLink at the moment, and its something I am not completely complaining about due to the price, is the speed of the connection to the outside world on my machine. its more than likely my box, but I am getting a max of around 300kb a second, and that&#8217;s not over VPN. this is using wget on the terminal.

Other than that, for the price, this is very cool. If anyone is interested in getting a copy of my client or server config files (since i had such a hard time getting them to work) drop me a mail (tierno [at] lotas-smartman [dot] net) and i will send them on.

 [1]: http://www.poptop.org/
 [2]: http://openvpn.net/howto.html
 [3]: http://www.thebakershome.net/?q=node/56
 [4]: http://openvpn.se/bb/viewtopic.php?t=77
 [5]: http://openvpn.se/
 [6]: http://www.tunnelblick.net/
 [7]: http://forums.vpslink.com/showthread.php?t=2362