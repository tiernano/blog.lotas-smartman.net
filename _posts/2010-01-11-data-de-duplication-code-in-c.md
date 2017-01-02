---
title: 'Data De-duplication code in C#'
author: admin
layout: post
permalink: /data-de-duplication-code-in-c/
dsq_thread_id:
  - 57487465
  - 57487465
dsq_needs_sync:
  - 1
categories:
  - Uncategorized
---
So, i have been looking at Data De-Duplication, and have built a little demo app in C# for this idea&#8230; [The code is on GitHub][1] and if you have better ideas around the code, please leave comments or update the block.

**This code is not intended for Production use. it is purely experimental! **

One idea i would like to look into though is using a proper backing store for this data: MSSQL DB, Amazon S3, RackSpace Cloud Storage, Azure Blob Storage, etc. the theory would go as follows:

  * user points de-dupe tool to a folder
  * folder is processed &#8211; each file is broken into 512byte blocks (could be more or less, configurable in code) and check-summed (currently using SHA512, but been told its over kill!) an Index file is created for every &#8220;real&#8221; file on the system. they contain the block IDs in order for the given real file.
  * after each block is check-summed, it is checked against the backing store. If the checksum exists in the backing store, the id is written to the index file. if not, a new block is added to the backing store and that ID is added to the index.
  * When a user wants the file, the index file is checked, all the blocks are pulled from the correct locations, and built up for the user to work with. Any changes go though the same process. if the user only changes a couple of sections at the end of a file, only those couple of sections should be changed&#8230;

You get some problems with changes, in that you dont really want to change all instances of that particular block, incase you break something else&#8230; you also need to have something cleaning blocks also, just to remove dead or orphaned blocks&#8230;

Running this on some XML files on my drive (about 3200 XMP files from Adobe Lightroom) the code finds 43k blocks duplicated, with an estimated 21mb duplicated. it does no de-duplication at the moment&#8230;

Ideally, this should be built as a FileSystem (showing as a hard drive, backed to, say, SQL server or a single large file) or as a SMB share, which can be mounted in Windows&#8230; Now to figure out if its possible&#8230;  
[<img src="http://www.dotnetkicks.com/Services/Images/KickItImageGenerator.ashx?url=http%3A%2F%2Fblog.lotas-smartman.net%2Fdata-de-duplication-code-in-c" border="0" alt="kick it on DotNetKicks.com" />][2]

 [1]: http://gist.github.com/273880
 [2]: http://www.dotnetkicks.com/kick/?url=http%3A%2F%2Fblog.lotas-smartman.net%2Fdata-de-duplication-code-in-c