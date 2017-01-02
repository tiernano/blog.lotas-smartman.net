---
title: 'This website should hopefully be more responsive&#8230;'
author: admin
layout: post
permalink: /this-website-should-hopefully-be-more-responsive/
dsq_thread_id:
  - 26016212
categories:
  - Uncategorized
---
&#8230;Hopefully! Over the last couple of months, I have noticed the website has been very slow. after some firefighting over that amount of time, I didn&#8217;t really help anything. well, I have been playing with Windows 2003 Server this morning, and realized that IIS was set to load 2 processes to run the site, and there where a couple of App Pools that has similar settings.

This is all well and good if you have a proper multiprocessor machine, and tones of ram, but in the case of this box, I don&#8217;t. it has a single Xeon processor running at 2.4Gz, but it is only HyperThreaded, not dual core. I have heard that Hyperthreading can degrade performance on certain tasks, and this must be one of them. Also, because it started 2 instances of the process, each took the same amount of ram (about 120mb, give or take). So, that&#8217;s 240Mb running, just for this site! The machine only had 768Mb ram (I have been meaning to upgrade this box, but never got around to it).

So, setting different app pools to only run on a single instance seems to have saved quite a lot of ram. time will tell how well it has worked though&#8230;

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:bba61f36-c5ad-40f6-967a-60b4fb4df3cf" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/PowerEdge" rel="tag">PowerEdge</a>, <a href="http://technorati.com/tags/Xeon" rel="tag">Xeon</a>, <a href="http://technorati.com/tags/Hyperthreading" rel="tag">Hyperthreading</a>, <a href="http://technorati.com/tags/IIS" rel="tag">IIS</a>, <a href="http://technorati.com/tags/Windows%202003%20Server" rel="tag">Windows 2003 Server</a>
</div></p>