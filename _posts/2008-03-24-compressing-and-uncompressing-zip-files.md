---
title: Compressing and uncompressing ZIP files
author: admin
layout: post
permalink: /compressing-and-uncompressing-zip-files/
categories:
  - Uncategorized
---
&nbsp;

[Link to The Codecruncher :: Compressing and uncompressing ZIP files :: January :: 2007][1] 

&nbsp;

First i posted about [extracting and compressing files into and from CABs][2]. now, we have Zips. all this compression is making me confused! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> I have an idea, but the question is would it work as im thinking. Lets say, for example, we have a multi teir app (DB, App Server (either .net remoting or web services) and your front end (web app, smart app and mobile)). and your app server is sending relitivly large amounts of data. would sticking it in a CAB stream and sending it over the wire be a good idea? its more compressed then ZIP and GZIP, but you have compression and decompression time. I supose if its on Mobile or something like that, the few extra miliseconds to compress or decompress would a good tradeoff for data usage. Any thoughs?

 [1]: http://codecruncher.blogsome.com/2007/01/04/37/
 [2]: http://blog.lotas-smartman.net/archive/2007/01/09/19150.aspx