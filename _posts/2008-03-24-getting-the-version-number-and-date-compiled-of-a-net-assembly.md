---
title: Getting the Version number and Date compiled of a .NET assembly
author: admin
layout: post
permalink: /getting-the-version-number-and-date-compiled-of-a-net-assembly/
dsq_thread_id:
  - 26015058
  - 26015058
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
</p> 

[**update**] After some investigation, i have found some issues with the way i have calculated the dates. firstly, the day is off by a day (leap year?) and the time is now off by a little more. its now off by over 50min. If i find more info, i will post it. 

I have been building a new web site for a while now ([www.tiernanotoolephotography.com][1]&nbsp;which is semi live) and i have been thinking of different things to add to the about page. Well, here is one of them: The version info about the assemblys, and when they where built. so here is how it works: 

&nbsp; 

using System.Reflection; 

//You need to include the reflection section to get this to work 

[assembly: AssemblyVersion(&#8220;01.00.\*&#8221;)] //this will give you 1.0.2420.32394 for today. you can have a 1.00.01.\* if you 

//prefer, but it wont work for the following solution.

&nbsp;

public partial class About : System.Web.UI.Page  
{  
protected void Page_Load(object sender, EventArgs e)  
{  
double build = System.Reflection.Assembly.GetExecutingAssembly().GetName().Version.Build; //gets the build number 

//(this is the .2420 section above

double minorRev = System.Reflection.Assembly.GetExecutingAssembly().GetName().Version.MinorRevision; //gets minor

//this is the .32394 above.

DateTime CompiledDate = new DateTime(2000,1,1); //new time starting from jan 1 2000  
CompiledDate = CompiledDate.AddDays(build); // add the build as days  
CompiledDate = CompiledDate.AddSeconds(minorRev * 2);&nbsp;//add the time in seconds, multiplied by 2&nbsp;(dont ask) 

Response.Write(&#8220;Version: &#8221; + System.Reflection.Assembly.GetExecutingAssembly().GetName().Version); 

//retuns the version number

Response.Write(&#8220;<br>&#8221;);  
Response.Write(&#8220;Compile Date and Time: &#8221; + CompiledDate.ToString()); //displays compiled date  
}

&nbsp;

so, the version info is based on time. interesting theory. the build is based on the&nbsp;number of days since jan 1 2000, and the revision is based on the number of seconds since mindnight, which all is cool. So, hopefully this helps you as much as it helps me! (well, i havent figured out how it can help me, just yet, but lets not go into that&#8230;) Also, there is one issue i have noticed. what ever way the seconds is calculated, it is off by an hour. so, for the above time it is showing a little before 6PM, but its really a little before 7PM. Whats an hour between friends though? <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

This code is here with no garentee, just showing you how this works, bla bla bla&#8230; <img src="http://blog.lotas-smartman.net/wp-includes/images/smilies/icon_smile.gif" alt=":)" class="wp-smiley" />

bk_keywords: programming, c#

 [1]: http://www.tiernanotoolephotography.com