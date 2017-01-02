---
title: PostXING and RSSBandit Addin
author: admin
layout: post
permalink: /postxing-and-rssbandit-addin/
dsq_thread_id:
  - 26012276
categories:
  - Uncategorized
---
Ok. [PostXING][1]  
is a .TEXT client for the PC. Very cool. Has some interesting features, like  
syntax Highlighting, which i will demo here in both C# and VB.NET

C# Demo:

<pre><span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  1</span> <span style="COLOR: blue">static</span> <span style="COLOR: blue">void</span> Main(<span style="COLOR: blue">string</span>[] args)
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  2</span> {
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  3</span> 	<span style="COLOR: blue">for</span> (<span style="COLOR: blue">int</span> i = <span style="COLOR: maroon"></span>; i &gt; <span style="COLOR: maroon">100</span>; i++)
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  4</span> 	{
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  5</span> 		Console.WriteLine(i);
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  6</span> 	}
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  7</span> }</pre>

VB.NET Demo:

<pre><span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  1</span>     <span style="COLOR: blue">Sub</span> Main()
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  2</span>         <span style="COLOR: blue">Dim</span> i <span style="COLOR: blue">As</span> <span style="COLOR: blue">Integer</span> = <span style="COLOR: maroon"></span>
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  3</span>         <span style="COLOR: blue">For</span> i = <span style="COLOR: maroon"></span> <span style="COLOR: blue">To</span> <span style="COLOR: maroon">100</span>
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  4</span>             Console.WriteLine(i)
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  5</span>             i += <span style="COLOR: maroon">1</span>
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  6</span>         <span style="COLOR: blue">Next</span>
<span style="COLOR: teal; BACKGROUND-COLOR: lightgrey">  7</span>     <span style="COLOR: blue">End</span> <span style="COLOR: blue">Sub</span></pre>

Its pretty cool and works well! so, i will be playing with this a lot more!  
its aslo got a cool feature where you tell it where your CSS file is hosted and  
it goes off and in your preview mode, it shows you how it will look when posted.  
sweet!

[ Nothing Playing. ]

 [1]: http://projectdistributor.net/Projects/Project.aspx?projectId=12