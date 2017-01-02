---
title: Damn internet connection!
author: admin
layout: post
permalink: /damn-internet-connection/
dsq_thread_id:
  - 26007891
categories:
  - Uncategorized
---
right. i got in today&nbsp;and tried to go to slashdot.org to see what was up. and nothing. the connection was on, but there was no stuff happening. so i&nbsp;went in search for a reason. somewhere between me and about 6 hops away, the net is dead. well actually its either an NTL router or a Cable and Wireless router. reason i know this is as follows:

> C:\Documents and Settings\lotas>tracert slashdot.org   
> Tracing route to slashdot.org [66.35.250.150] over a maximum of 30 hops:   
> 1 1 ms 1 ms 1 ms 192.168.1.254   
> 2 23 ms 14 ms 11 ms 10.135.39.254   
> 3 10 ms 11 ms 19 ms dub-cam1-b-fa30.inet.ntl.com [62.254.98.21]   
> 4 17 ms 11 ms 27 ms dub-core-b-pos1100.inet.ntl.com [62.254.96.201]   
> 5 20 ms 19 ms 26 ms lee-bb-b-atm010-225.inet.ntl.com [62.253.187.54]   
> 6 \* \* * Request timed out.   
> 7 45 ms 27 ms 26 ms ycr2-so-3-0-0.Manchester.cw.net [208.175.252.89]   
> 8 \* \* * Request timed out.  
> 9 \* \* * Request timed out.   
> 10 162 ms 177 ms 176 ms bhr1-pos-0-0.SantaClarasc8.cw.net [208.172.156.1 98]   
> 11 164 ms 174 ms 180 ms csr1-ve243.SantaClarasc8.cw.net [66.35.194.50]   
> 12 \* \* * Request timed out.   
> 13 \* \* * Request timed out.   
> 14 \* \* * Request timed out. 

and it contniues till it reaches 30 hops and dies. so, my solution? simple. cheating! im now connecting to the NTLs proxy server in Oxford. this is not affected by the Cable and Wireless problem. dont know why, but it aint. so it works. im using this though my [Squid proxy][1] and i had the help of the [this site][2] to show how to set Squid up for the job.

 [1]: http://www.squid-proxy.org
 [2]: http://www.greenend.org.uk/rjk/2002/03/squid.html