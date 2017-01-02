---
title: 'Grid Computing: why i want to play with this'
author: admin
layout: post
permalink: /grid-computing-why-i-want-to-play-with-this/
dsq_thread_id:
  - 26015678
  - 26015678
categories:
  - Uncategorized
---
Right, so about 2 weeks ago i posted about a peice of software called <a class href="http://blog.lotas-smartman.net/archive/2007/03/04/alchemi-net-based-enterprise-grid.aspx">Alchemi</a>. Its a .NET based grid computing framework. I have had some ideas on what i want to use this for, and have decided to post them here for reference. 

Firstly, how is grid compting usefull. Well, take my bedroom as an example. I have 4 running machines at the moment (a dual proc 32 bit athlon, a dual proc 64 bit opteron, a single proc, but hyperthreaded Xeon, and a dual proc, dual core Xeon). if i add the laptop to the mix, thats a 64 bit Turion. adding the rest of the machines around the house would include a 64bit athlon and a dual core 64 bit Pentium D. now thats a lot of horse power. but i cant use it all together without the help of grid computing. 

What grid computing does is splits the workload up so that little peices of the task can be done by different machines. Something along the lines of <a class href="http://setiathome.berkeley.edu/">Seti at home</a>&nbsp;but on a slightly smaller scale. So, how would the average person, or in my case, the not so average person, use a technology like this. Well, I dont know. Im still in the planning phase, but i have some theories&#8230;

1: Photography: Right, so my theory goes like this: you take a couple of hundred photos in RAW format, and want them accessable around the house. you upload them to your PC, do some minor changes to them, and then farm out the full converting from RAW to JPG to the farm. the farm would take the original RAW image and, lets say for arguments sake, a XML sidecar file which would hold your changes. then eah node would process the photo in a few ways: generate a full JPG version of the photo, a smaller 1280*1024 version and a backup format (<a class href="http://www.adobe.com/products/dng/">Adobe DNG</a> maybe). it could then copy them to different locations (full JPG to a directory that all machines can see, the smaller JPG auto uploaded to <a class href="http://www.flickr.com/">Flickr</a>, <a class href="http://www.smugmug.com/">SmugMug</a>&nbsp;or somewhere simular and the DNG and original RAW image placed in a storage archive). in reality, PCs are fast enough to do this workflow in about a half hour for 200+ photos, but farming all this out to machines which may otherwise be idle makes the process a lot faster, or at least in theory. 

2: Music: might be a stupid idea, but a farm for processing music. the theory&nbsp;goes one machine would rip the&nbsp;WAV&nbsp;from a CD, then place it somewhere for the rest of the nodes to get their hands on it. Each node would take a track, convert it to, lets say, Lossless AAC (for your Mac), Lossless WMA (for your Media Center),&nbsp;256k/b MP3 or AAC for your iPod and&nbsp;256k/b WMA&nbsp;for your Zune. again,&nbsp;in theory not needed, but could be usefull. then again,&nbsp;maybe not.

3: Video: would there be a way to farm out Video processing? would there be a need? 

I think of all the ideas, the photography is the closest one to needing this idea, but how do you process RAW images in C#&#8230; Hmmmm&#8230;&nbsp;

[update] ihave a 4th idea. this one, or at least the idea, comes from <a class href="http://www.bladewatch.com/2007/03/12/grid-computing-in-the-home/">Blade Computing</a>, who picked up on this post. the idea is for Media center usage. now, the theory i have behnid this is transcoding video. The video is recorded and left on your media center for your viewing plesure. but, lets say you want to keep some shows you record, or share them out around the house. Well, since Media center files are 2Gb per hour (give or take) this is a lot of bandwidth usage. so, break the files up, send them around the grid, and get the grid to transcode them. you could have your high def versions in WMV format for all meida centers and XBox360s around the house, a smaller wide screen WMV for, lets say, your Zune or PPC, and maye even a MP4 version for either your PSP or iPod video. the only question&nbsp;i now have: if you split a 2 hours TV show (4GB) into 4 bits and transfer it around the network, you get 4 30Min segments back. how do you 1: split the file so you dont Damage it, and 2: unsplit the file so you can watch it again&#8230;.