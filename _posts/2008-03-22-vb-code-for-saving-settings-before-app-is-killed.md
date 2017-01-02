---
title: vb code for saving settings before app is killed
author: admin
layout: post
permalink: /vb-code-for-saving-settings-before-app-is-killed/
dsq_thread_id:
  - 26005620
categories:
  - Uncategorized
---
Right. im going to add this to the [project][1]. its allows you to save code and saves it to the registery.

**this is for the form load event**

Me.Width = GetSetting(&#8220;SaveAppTest&#8221;, &#8220;startup&#8221;, &#8220;Width&#8221;, 5000)

Me.Height = GetSetting(&#8220;SaveAppTest&#8221;, &#8220;startup&#8221;, &#8220;Height&#8221;, 5000)

**This is for the queryunload event**

SaveSetting &#8220;SaveAppTest&#8221;, &#8220;startup&#8221;, &#8220;Width&#8221;, Me.Width

SaveSetting &#8220;SaveAppTest&#8221;, &#8220;startup&#8221;, &#8220;Height&#8221;, Me.Height

Right. he is the info from microsoft IDE: SaveSettings(appname as string, section as string, key as string, setting as string). the getsetting is as follows: getsetting(app name as String,section as String, key as String,default as string). so there you have it. handy.

 [1]: http://www.sf.net/projects/lsnosbrowser