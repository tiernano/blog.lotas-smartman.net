---
title: Populate Datagrid on Background Thread with Data Binding by Using VB.NET
author: admin
layout: post
permalink: /populate-datagrid-on-background-thread-with-data-binding-by-using-vbnet/
dsq_thread_id:
  - 26011226
  - 26011226
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
When large queries to a database are executed, the application may become unresponsive for a long period of time. To avoid this behavior and decrease the waiting time of the user, the query can be executed on a background thread, releasing the application for other tasks until the data is returned from the database and databinding is performed.   
[318604 &#8211; HOW TO: Populate Datagrid on Background Thread with Data Binding by Using Visual Basic .NET][1]. Very handy article. I was trying something where my dataset was updated using a thread, but i kept getting an error &#8220;**Controls created on one thread cannot be parented to a control on a different thread**&#8220;. this solves that problem.

 [1]: http://support.microsoft.com/default.aspx?scid=kb;en-us;318604