---
title: Mac Mini as a HPC compute cluster
author: admin
layout: post
permalink: /mac-mini-as-a-hpc-compute-cluster/
dsq_thread_id:
  - 26016615
  - 26016615
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
I have always known that the [Mac Mini][1] was a great little computer. i have been wanting one (or 2 or more) of these for a while now for different reasons. and now i have a new reason!

VolkerW has a post on [how to turn a Mac Mini into a virtual HPC 2008 Compute Cluster][2]. Given that the Mac Mini has a Core 2 Duo processor, which has Intel VT enabled, this is a great little machine for Virtualization. And given its size, you can fit a lot of these into a very small amount of space. if you have a few of these sitting on their side, you can get 9 in the same width of a RACK server (they are only 2" high), and given that they are 6.5 incles wide (which in our test is 6.5" high") these are only has high as 3 units. now, given, they are not the most powerfull boxes, but they are a LOT smaller. and if you wanted to mount them in a proper RACK you can do it deep wise too, as long as you have the cooling&#8230;

right, so enough of the raning, this is very cool! take, say, 6 of these, sitting in 2 "towers" of 3 each, and your taking up very little desk space. less than an average machine. but, in reality, you have 12 cores and, if you max the RAM out, you have 24Gb of ram. Starting to make me think&#8230;. <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

 [1]: http://www.apple.com/macmini/
 [2]: http://blogs.msdn.com/volkerw/archive/2008/03/19/turning-a-mac-mini-into-a-virtual-windows-hpc-server-2008-compute-cluster.aspx