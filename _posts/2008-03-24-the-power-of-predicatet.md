---
title: 'The Power of Predicate&lt;T&gt;'
author: admin
layout: post
permalink: /the-power-of-predicatet/
dsq_thread_id:
  - 26016200
categories:
  - Uncategorized
---
Randy Patterson has a post on his blog, entitled the [power of Predicate<T>][1]. this is something I was looking for a while back, and ended up building my own tools for the job.

The problem was I had a list of objects, and I was looking for a particular object in that list to update. Well, the way I ended up doing this was something like &#8220;for each object in list, if object = the one I want, update, else, next&#8221; (very bad Pseudo code there). that&#8217;s grand for maybe one or 2 objects in a list, but if your talking hundreds or thousands, then performance issues occur. 

Hopefully this helps someone out there. I know it will help me in my daily life! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

[[kick it][2]]

[tags:Predicate<t>, List, Programming]

<div class="wlWriterSmartContent" id="scid:0767317B-992E-4b12-91E0-4F059A8CECA8:c6f3740e-e0f9-442e-97a2-0ba69adf41b1" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  Technorati Tags: <a href="http://technorati.com/tags/Predicate<T>" rel="tag">Predicate<T></a>, <a href="http://technorati.com/tags/List" rel="tag">List</a>, <a href="http://technorati.com/tags/Programming" rel="tag">Programming</a>
</div>

 [1]: http://randypatterson.com/2007/09/19/ThePowerOfThePredicateltTgt.aspx
 [2]: http://www.dotnetkicks.com/csharp/The_Power_of_the_Predicate_T