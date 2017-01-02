---
title: My trials with DasBlog
author: admin
layout: post
permalink: /my-trials-with-dasblog/
dsq_thread_id:
  - 26016253
categories:
  - Uncategorized
---
On [Friday I made the decision][1] that I wanted to move the blog and use new software for the front end. I have been thinking about this for a while now, and finally stepped up and posted about it here. There where 2 contenders: DasBlog and BlogEngine.NET and, after a bit of fiddling, I settled on DasBlog. 

I have a server sitting here in Virtual Server on my workstation, and it has IIS and everything required to get this to run. I have been fiddling around with it, and there are some things I have to work out before it goes into production.

some of my notes:

  * the URL rewriting feature is very handy, but because of the way community server stores its URLs and DasBlog stores them, there may be some pain points for users. the way I am currently testing it is as follows: 
      * say a current blog post of: <http://blog.lotas-smartman.net/archive/2007/10/12/thinking-of-changing-this-blogs-software.aspx>. this will get you directly to that post, but once DasBlog is implemented, hopefully it will get you to the list of all posts for that day. unfortunately, it is also giving other posts from about 4 days or so previous. not sure why, but it is&#8230; I will look into this. 
          * the other problem with above is that if the post your actually looking for was posting first in a day, and 3 others after, the post you are looking for will be on the bottom, not the top. 
              * This only applies to old posts with old links. new posts will looking something like <http://blog.lotas-smartman.net/2007/10/12/ThinkingOfChangingThisBlogsSoftware.aspx>. needless to say, that link does not work currently.</ul> 
          * still looking into which way I should store the data. default, out of the box solution, is XML Files. this is handy since they are quite small (my 3500+ posts and comments weigh in at about 8mb uncompressed). This also allows easy moving to different boxes since its just a xcopy deployment. Problem is first time the application loads, it can be slow. I have seen spikes of 100% processor load while reading all the files. looking into other options, or speedier loads&#8230;
          * look and feel: still looking into this, but I will defiantly want a similar look and feel as the current blog has. </ul> 
        I will post more later once it completed. I will also explain how I got my data from Community Server into DasBlog in the first place!
        
        <div class="wlWriterSmartContent" id="0767317B-992E-4b12-91E0-4F059A8CECA8:ad786744-4ca9-4701-9b5b-99dc1416594a" contenteditable="false" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
          Technorati Tags: <a href="http://technorati.com/tags/DasBlog" rel="tag">DasBlog</a>, <a href="http://technorati.com/tags/Community%20Server" rel="tag">Community Server</a>, <a href="http://technorati.com/tags/BlogEngine.NET" rel="tag">BlogEngine.NET</a>, <a href="http://technorati.com/tags/Migration" rel="tag">Migration</a>, <a href="http://technorati.com/tags/Blogging" rel="tag">Blogging</a>
        </div></p>

 [1]: http://blog.lotas-smartman.net/archive/2007/10/12/thinking-of-changing-this-blogs-software.aspx