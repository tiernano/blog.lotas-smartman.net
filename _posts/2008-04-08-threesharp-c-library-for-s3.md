---
title: 'ThreeSharp: C# library for S3'
author: admin
layout: post
permalink: /threesharp-c-library-for-s3/
dsq_thread_id:
  - 26016517
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
I have been using [Amazon S3][1] for some bits and peices for the last while, like my Image Site for example, and i am always looking for new and more interesting ways of using it. one way i have started to think about, especially over the last few days, is a backup medium for my photos. i wont go into details about how i will be doing this, yet, since its not planned out, but i do know how i will be uploading to S3: [ThreeSharp][2].

ThreeSharp is a C# library for Amazon S3 hosted on [CodePlex][3]. the description of the project is as follows:**Project Description  
**An advanced C# library for interfacing with the Amazon S3 system. Among its powerful features are:  
&#8211; Full support for data streaming. No need to load data into memory before sending to S3.  
&#8211; Data encryption.  
&#8211; Thread safety and live statistics. Perform multiple simultaneous uploads and downloads and show progress in real-time.  
&#8211; A powerful, unified object model that simplifies maintenance and extensions.  
&#8211; Support for EU buckets.

this was leached directly off the Project site. The multiple simultaneous uploads and downloads with progress is something i am VERY interested in, and the EU bucket suport will also come in handy. Since i have nearly 40Gb of RAW images, and each image is about 8mb (give or take) i would like some sort of statistics info, and % completed.

Once i have more, i will post about it, but check out the project page.

 [1]: http://www.amazon.com/s3
 [2]: http://www.codeplex.com/ThreeSharp
 [3]: http://www.codeplex.com