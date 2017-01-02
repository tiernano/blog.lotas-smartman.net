---
title: 'Idea: using Mechanical Turk for image processing work'
author: admin
layout: post
permalink: /idea-using-mechanical-turk-for-image-processing-work/
dsq_thread_id:
  - 26016157
  - 26016157
categories:
  - Uncategorized
---
I have had an idea. Before anyone posts comments about how good an idea this is, but why did I post it and not try it out, this idea only came to me a few minutes ago, and I may start working on it. 

In a post I mad a couple of months ago, I talked about [Amazons Mechanical Turk][1] and [how to use it with Windows Workflow Foundation][2]. Well, it got me thinking: why not use this for Photography work? here is the idea:

I shoot all my photos in RAW, and some of these require work to get them to perfect quality (minor light tweaks, cropping, etc). Get MT to do the job! 

  * Requester&nbsp;sends the RAW image to the service (use S3 for the storage say) and each HIT include the link to RAW image, and a place to upload the completed work. places a price on each image of, say, 25c or 50c. 
  * Turkers take the RAW image, process it, tweak it, take the XMP (sidecar) and the RAW image, aswell as the processed JPEG and upload to the server, telling the requester it is completed.
  * Requester&nbsp;QA&#8217;s the work and then&nbsp;pays, if they are happy.

This all sounds well and good, and there is a mechanism to get it to work, but what does anyone else think?</p> 

<div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:28ce1fcf-ec1a-45b4-aceb-6cc0f0bee789" style="padding-right:0px;display:inline;padding-left:0px;padding-bottom:0px;margin:0px;padding-top:0px;">
  Technorati Tags: <a href="http://technorati.com/tags/Mechanical%20Turk" rel="tag">Mechanical Turk</a>, <a href="http://technorati.com/tags/photography" rel="tag">photography</a>, <a href="http://technorati.com/tags/Windows%20Workflow%20Foundation" rel="tag">Windows Workflow Foundation</a>, <a href="http://technorati.com/tags/RAW" rel="tag">RAW</a>, <a href="http://technorati.com/tags/Image%20processing" rel="tag">Image processing</a>
</div>

 [1]: http://www.amazon.com/Mechanical-Turk-AWS-home-page/b/ref=sc_fe_l_2/002-2787390-9969626?ie=UTF8&node=15879911&no=3435361&me=A36L942TSJ2AJA
 [2]: http://blog.lotas-smartman.net/archive/2007/02/07/integrating-amazon-mechanical-turk-into-windows-workflow-foundation.aspx