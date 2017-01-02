---
title: website speed issues
author: admin
layout: post
permalink: /website-speed-issues/
dsq_thread_id:
  - 26010447
categories:
  - Uncategorized
---
Ok. i have noticed some speed issues with this blog over the last while, and i think i know whats wrong. the database and the webserver are on the same system, and so is a proxy and dns server. the proxy is now being phased out (my win2k3server and ISA 2004 server are running that) but its still slow. there is a load time status text at the bottom of each page, and it is saying 3.5 seconds for generation. So, im going to try and move the SQL server off that machine, which is only running at 700Mhz with 256mb ram, which could also be a problem, and put it on the win2k3server which runs 1.3Gz and has 512mb ram. hope this helps. ill try that later tonight or tommorrow.