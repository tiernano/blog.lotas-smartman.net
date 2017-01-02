---
title: DNS and ISA
author: admin
layout: post
permalink: /dns-and-isa/
dsq_thread_id:
  - 26016020
categories:
  - Uncategorized
---
</p> 

ISAServer.org has some articles talking about DNS and ISA. There are 2 different topics, one on running internal DNS Servers and how to configure them, and one for publishing them publicly on the Internet. Both very handy for very different reasons.

  * [*DNS Publishing Scenarios (Part 1)*][1]
  * [*DNS Publishing Scenarios (Part 2)*][2]
  * [*The Definitive Guide to ISA Firewall Outbound DNS Scenarios Part 1: DNS Resolvers, DNS Forwarders, DNS Caching and Recursion*][3]
  * [*The Definitive Guide to ISA Firewall Outbound DNS Scenarios Part 2*][4]
  * [*The Definitive Guide to ISA Firewall DNS Scenarios Part 3: Outbound DNS Scenarios*][5]

The publishing articles would be very handy if you had, lets say, a dedicated line and a couple of IP addresses. you could run your own DNS server internally and when requests for DNS queries come in, your machines tell users which IP&#8217;s to go to. The guide on Outbound DNS has tips on how to get Active Directory running correctly, and how to use external DNS Resolvers (using DNS Forwarding) for queries. This is how my network is setup, and, as a tip, you may want to check out [OpenDNS.com][6] for some very fast DNS results!</p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:c37bd58b-a9f6-44bf-8e28-94d1922a524a" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/DNS" rel="tag">DNS</a>, <a href="http://technorati.com/tags/OpenDNS" rel="tag">OpenDNS</a>, <a href="http://technorati.com/tags/ISA" rel="tag">ISA</a>, <a href="http://technorati.com/tags/Active%20Directory" rel="tag">Active Directory</a>, <a href="http://technorati.com/tags/ISAServer.org" rel="tag">ISAServer.org</a>
</div>

 [1]: http://www.isaserver.org/tutorials/DNS-Publishing-Scenarios-Part1.html
 [2]: http://www.isaserver.org/tutorials/DNS-Publishing-Scenarios-Part2.html
 [3]: http://www.isaserver.org/tutorials/Definitive-Guide-ISA-Firewall-Outbound-DNS-Scenarios-Part1.html
 [4]: http://www.isaserver.org/tutorials/Definitive-Guide-ISA-Firewall-Outbound-DNS-Scenarios-Part2.html
 [5]: http://www.isaserver.org/tutorials/Definitive-Guide-ISA-Firewall-Outbound-DNS-Scenarios-Part3.html
 [6]: http://www.opendns.com/