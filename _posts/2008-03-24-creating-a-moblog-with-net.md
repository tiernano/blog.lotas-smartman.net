---
title: Creating a moblog with .NET
author: admin
layout: post
permalink: /creating-a-moblog-with-net/
dsq_thread_id:
  - 26012609
categories:
  - Uncategorized
---
So i had this idea a while back after Text America stoped their RSS feeds for their mob logs. I wanted to create my own MobLog software. Now, i though about it but never got around to doing anything. but after watching [this video over at channel 9 (Chris Gray &#8211; Building your own home server)][1], i started thinking a bit more about it. The idea of uploading the photo though a web service is interesting to me. You, in theory, could have a Pocket PC Client, Smartphone and Desktop client, and all use the same webservice. Using [this EXIF VB Class][2] you an get infomration about the camera that took the photo, time/date, info about the photo and more, and put that in a DB too. And using either help from [this article][3] or [this one][4] you can do image resizing on the fly and create thumbnails, etc. Finally, using the .TEXT webservice, you can then make an auto post to the site with the photo in the page. This is now a project i will have a look at working on. Now if only my camera wrote to SD cards or my Pocket PC or Smartphone read from them i could post full 3.2Mp photos on the road! I will start coding this up soon and start posting stuff here!

 [1]: http://channel9.msdn.com/ShowPost.aspx?PostID=43064
 [2]: http://blog.lotas-smartman.net/archive/2004/06/10/TheExifReaderclassVBNET.aspx
 [3]: http://aspnet.4guysfromrolla.com/articles/012203-1.aspx
 [4]: http://aspnet.4guysfromrolla.com/articles/012203-1.2.aspx