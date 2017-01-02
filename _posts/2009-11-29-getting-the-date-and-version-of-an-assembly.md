---
title: Getting the date and version of an assembly
author: admin
layout: post
permalink: /getting-the-date-and-version-of-an-assembly/
dsq_thread_id:
  - 48726104
  - 48726104
dsq_needs_sync:
  - 1
categories:
  - HowTo
---
So, i have been busy working on code for [Torrent Helper][1] (still looking for a proper name and URL) and one of the things i wanted to add was a version number footer&#8230; ust for the laugh, just cause i could&#8230; But how? So, this is how you do it&#8230;

First, you need to modify the AssemblyInfo.cs file in your project (I have 2 projects, my website and my backend service). In here i set the AssemblyVersion and AssemblyFileVersion to 0.1.\*. The \* tells the compiler to magically build the number&#8230;

Next, how do you get it back out programatically? (click to see the larger version)

[<img src="http://images.lotas-smartman.net/image.ashx?id=3fb7bd06-a325-446f-8cdd-d76761be6299" alt="Version Info Code" width="400" />][2]

As you can see, i have 2 functions here. one (PrintBuild()) is called by the web site where i want to put the data (I know this is not pretty, but its working&#8230; maybe some dat i will changed it&#8230; the second functions only job is to get the information about the assembly and work out the date and time it was built&#8230; Any questions, leave a comment.

 [1]: http://torrents.lotas-smartman.net
 [2]: http://images.lotas-smartman.net/image.ashx?id=3fb7bd06-a325-446f-8cdd-d76761be6299