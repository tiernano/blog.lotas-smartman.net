---
title: Weight Watchers Code
author: admin
layout: post
permalink: /weight-watchers-code/
dsq_thread_id:
  - 26011364
  - 26011364
categories:
  - Uncategorized
---
So, the mammy and the sister has gone on the weight watchers plan, and brough me and the daddy along with them. so, i decided to see if i could find a forumula for getting the points in something. so here is some VB.NET code that does the job: 

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">Private</span> <span style="color:blue">Sub</span> Form1_Load(<span style="color:blue">ByVal</span> sender <span style="color:blue">As</span> System.Object, <span style="color:blue">ByVal</span> e <span style="color:blue">As</span> System.EventArgs) <span style="color:blue">Handles</span> <span style="color:blue">MyBase</span>.Load</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:green">'weight watchers code</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:green">'read http://www.healthyweightforum.org/eng/articles/weight_watchers_points/ for more info</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Dim</span> p, c, f, r <span style="color:blue">As</span> <span style="color:blue">Double</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; c = InputBox("enter Calories")</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; f = InputBox("Enter grams of Fat")</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; r = InputBox("Enter Dietary fiber grams, or 0 if unknown")</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; p = (c / 50) + (f / 12) &#8211; (minimum(r, 4) / 5)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MsgBox(p)</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Sub</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">Public</span> <span style="color:blue">Function</span> minimum(<span style="color:blue">ByVal</span> a <span style="color:blue">As</span> <span style="color:blue">Integer</span>, <span style="color:blue">ByVal</span> b <span style="color:blue">As</span> <span style="color:blue">Integer</span>) <span style="color:blue">As</span> <span style="color:blue">Integer</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">If</span> a > b <span style="color:blue">Then</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Return</span> b</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">Else</span></span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">If</span> a < b <span style="color:blue">Then</span> <span style="color:blue">Return</span> a</span>
</p>

<p class="MsoNormal" style="text-autospace: none">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">If</span></span>
</p>

<p class="MsoNormal">
  <span style="font-size: 10.0pt; font-family: Courier New">&nbsp;&nbsp;&nbsp; <span style="color:blue">End</span> <span style="color:blue">Function</span></span>
</p>

&nbsp;

The website i got the info from, [Healthy Weight Forum][1] has the info i needed: the formula: P=(c/50)+(f/12)-(min(r,4)/5) where p = points, c=calories, f=fat grams and r=dietary fiber grams. the min(r/4) is the minimum of 4 or the fiber grams. Coding of a .NET app should be easer for you now! <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" /> working on a PPC and Smartphone client just becasue i can!

 [1]: http://www.healthyweightforum.org/eng/articles/weight_watchers_points/