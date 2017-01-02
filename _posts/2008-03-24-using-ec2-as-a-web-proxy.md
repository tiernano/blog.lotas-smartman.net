---
title: Using EC2 as a Web Proxy
author: admin
layout: post
permalink: /using-ec2-as-a-web-proxy/
dsq_thread_id:
  - 26016292
  - 26016292
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Software Voices.com has a post about how to use [Amazon EC2 as a proxy sever for surfing the web, privately and securely][1]. Its a very interesting post, and I have tried this out on my home machine for testing, and it works perfectly. basically, it creates an SSH tunnel between your machine and the EC2 instance. the EC2 instance has a copy of Squid installed, and a port on your machine is forwarded to the Squid port on EC2. once IE or FireFox is setup to use the proxy, all web traffic will get encrypted and sent over the wire securely. and same with what you download.

This is very cool. Could of things I have found out:

  1. because of the encryption and over head, your max download speed will be reduced slightly. Normally, on my 6mb connection, I can download at about 725-750kbps.with this, its down to about 650-675&#8230; 
  2. sites in Europe may load slower, but US files may load faster. this is because EC2 servers are hosted in the States. Since my connection is homed in Europe, my requests are going a lot further.
  3. interestingly. sites like [Pandora][2], which don&#8217;t work with my normal connection, do work with this. So, in theory, any site limited to US only connections should work.

That&#8217;s all well and good for web traffic, but what about the rest of your network traffic? Email, NNTP, etc. How do you get that to work? Well, I am thinking VPN&#8230;

Mind you, I cant seem to get it working correctly. and I cant find the info I need either&#8230; I found this [tutorial on the bit-tech.net forums][3]&nbsp;which talks about using pptpd,&nbsp;and this one over at [techimo.com using OpenVPN][4], but both mention editing IP addresses for clients. since EC2 has dynamic IP addresses, and I don&#8217;t have spare ones, this is a bit of a problem.

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:e37f19ce-a604-4398-9fef-142ab2c6c85f" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/EC2" rel="tag">EC2</a>, <a href="http://technorati.com/tags/SSH" rel="tag">SSH</a>, <a href="http://technorati.com/tags/Tunnel" rel="tag">Tunnel</a>, <a href="http://technorati.com/tags/OpenVPN" rel="tag">OpenVPN</a>, <a href="http://technorati.com/tags/VPN" rel="tag">VPN</a>, <a href="http://technorati.com/tags/PPTPD" rel="tag">PPTPD</a>
</div></p>

 [1]: http://www.softwarevoices.com/archives/54-ssh-tunnel-to-Amazon-EC2-as-a-temporary-web-proxy-for-privacy-and-security.html
 [2]: http://www.pandora.com
 [3]: http://forums.bit-tech.net/showthread.php?t=132029
 [4]: http://www.techimo.com/forum/showthread.php?t=176687