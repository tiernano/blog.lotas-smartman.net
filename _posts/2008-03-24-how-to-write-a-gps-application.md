---
title: How to write a GPS application
author: admin
layout: post
permalink: /how-to-write-a-gps-application/
categories:
  - Uncategorized
---
One of the things I have always wanted to do is GPS Logging and Analysis. I don&#8217;t know why, but its something I have always wanted to do. I have a piece of software on my pocket PC, [GPS Gate by Franson][1], which I use sometimes. It has the option of logging all GPS data to a text file for later use. So with this, I recorded quite a lot of log files (about 10mb of files, all text). So, I wanted to be able to parse the data in it, and get some info. The bits of info I wanted where Max Speed, and Average speed. I do want more, like distance traveled per LogFile, etc, but that&#8217;s for later. Its very easy, but I just haven&#8217;t coded it yet. 

So, how do you parse the data? Well, Developer Fusion.co.uk has the following 2 articles: [How to Write a GPS application][2], and [Writing your own GPS applications, Part 2][3]. With the help of this, I managed to read all the text files, parse each line, and work out the speed, etc. Very cool stuff. Now, all I need is a dedicated GPS logger&#8230; something small that can sit on my dash, get power from the car (cigaret lighter) and takes a memory card&#8230;.

&nbsp;

[tags:GPS, Programming, C#, NMEA]

 [1]: http://franson.com/gpsgate/
 [2]: http://www.developerfusion.co.uk/show/4634/1/
 [3]: http://www.developerfusion.co.uk/show/4652/1/