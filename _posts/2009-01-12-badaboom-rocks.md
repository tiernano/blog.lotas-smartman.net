---
title: Badaboom rocks!
author: admin
layout: post
permalink: /badaboom-rocks/
dsq_thread_id:
  - 26016778
  - 26016778
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
Well, i finally managed to install Windows 7 on my MacBook Pro, and, well, it rocks, but that’s another post for another day. today, i want to talk about something that i can only currently do on the MacBook Pro and that&#8217;s try out NVidia [Cuda][1] enabled applications. 

My Mac Pro has an ATI Radeon X1900GT card, and although ATI/AMD have software for running code on the GPU, none has caught my attention as much as [BadaBoom][2] by [Elemental Technologies][3]. Basically, its a video encoder, but it does not use your CPU for the encoding. it uses CUDA to offload the encoding to the GPU, in my case, the NVidia 9600M GT. the results are quite impressive: i managed to get about 70FPS encoding with a DivX file to MP4 for the iPod touch. it slows down quite a lot (between 10 and 18fps) when encoding to AppleTV quality, but given it is encoding at 720p, i am not too surprised…

my next test, which i will try do tomorrow, will be to encode some video from the 5D MKII (full 1080p) to the iPod touch and AppleTV formats and see how quickly it can do it. if i get a chance, i will try run the same with just the CPU (Dual core 2.4Gz) and see how quick it does it. Results to come later…

 [1]: http://www.nvidia.com/object/cuda_home.html#
 [2]: http://www.badaboomit.com
 [3]: http://www.elementaltechnologies.com/