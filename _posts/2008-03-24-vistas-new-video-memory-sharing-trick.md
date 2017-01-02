---
title: Vistas new (Video) memory sharing trick
author: admin
layout: post
permalink: /vistas-new-video-memory-sharing-trick/
dsq_thread_id:
  - 26015195
categories:
  - Uncategorized
---
[This post over at JKOnTheRun][1] tells you some info about WDDM drivers now being able to use system memory for video memory. This is extreamly interesting. the screen shot on their site shows the graphics card with a dedicated 30mb RAM, and it using 128Mb of system RAM. Well, check out this for a screen shot:

[<img height=459 alt=959mbGraphicsRam src="http://static.flickr.com/108/253388469\_0ffb741e0b\_o.jpg" width=417 border=0>][2]

The graphics card in my laptop has 128mb dedicated, 128mb of system memory (set in the bios) and now vista takes another 703mb of my system memory (i have 2Gb ram) to use. I actually havent noticed a difference in speed, so it must only take it when needed, but that is cool! My laptop has nearly a Gig of Video RAM! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://jkontherun.blogs.com/jkontherun/2006/09/microsoft_worki.html
 [2]: http://www.flickr.com/photos/lsmartman/253388469/ "Photo Sharing"