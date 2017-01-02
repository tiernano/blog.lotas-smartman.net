---
title: Using Dropbox as a personal Git and Mercurial Storage area
author: admin
layout: post
permalink: /using-dropbox-as-a-personal-git-and-mercurial-storage-area/
dsq_thread_id:
  - 458700326
dsq_needs_sync:
  - 1
categories:
  - HowTo
tags:
  - dropbox
  - git
  - mercurial
  - Source Control
---
This is something i have been using for a while now, and though it might be an idea to write a quick post explaining how to set Dropbox up as a folder to push your Git and Mercurial files to… But first, why would you want to?

So, you have a project you want to work on with multiple machines, and you want a source control system to easily manage files and state. You decided to use Git or Mercurial. I am not going to tell you which one to use… I use both for different projects. Anyway, you have decided to use Git or Mercurial, and you now want to be able to access the files from multiple locations. Since these locations are all your machines  (hopefully), you need to have a location that all machines can access. so, with the help of this tutorial, you can use Dropbox as your shared location. the following steps will need to be setup only once. When adding extra machines, follow the steps further on down.

  * First, you will need a Dropbox Account. If you don&#8217;t have one, [click here and sign up][1].
  * download the Dropbox installer, and link your machine. when installing, you will be asked to set the default location of your Dropbox folder, or a custom location. I picked the default location, and as i am running Windows 7, my Dropbox location will be at c:\users\tiernano\dropbox. yours will be different…
  * next, you will need either Git or Mercurial for Windows. [msysgit][2] is what i use for git on Windows. [Mercurial have a Windows installer also][3].
  * so now, we will branch out into either Git or Mercurial tasks:
  * for GIT:
  * Open Git Bash from the Start menu
  * you are now in a Unix-ish style command prompt… if you are not familiar with Unix… this might be interesting…
  * first, your Dropbox location will be at ~/Dropbox (~/ being your home directory)
  * cd into your ~/Dropbox folder, and create a folder called git (this is what i did, you may want to be different)
  * cd into your git folder, and create a new directory called yourproject.git (again, change it to your liking…)
  * cd into the yourproject.git folder and type **git init &#8211;bare.** this creates a bare repo for you to use. since this is in your Dropbox folder, all your machines synced with Dropbox will get this folder soon…
  * next, create a working folder.
  * decided where you want to put this (ideally, not on your Dropbox folder)
  * so, in my case i have a folder in my Documents folder in my home directory called project. I type **cd ~/Documents/project** to get to this folder.
  * when in this folder, type **git init**. this folder is now a git working folder.
  * add your files as needed. **git add <filename>** will add a file to git. **git commit –m “your message” –a** will commit all modified files on your repo with the message “Your Message” to the repo… Have a look for a [git Tutorial][4] to find more.
  * next, add a remote to your current repo. **git remote add dropbox ~/Dropbox/git/yourproject.git** will add your dropbox as a remote repo.  typing **git push dropbox master** will push your master branch to Dropbox .
  * that&#8217;s most of what you need to know.

  * For Mercurial, the following needs to be done
  * open a command prompt, and cd into your Dropbox folder.
  * create a folder, i called mine hg (the mercurial command is HG…)
  * in your hg folder, create a folder called myproject.hg.
  * cd into the folder and type **hg init.** this creates a Mercurial directory.
  * next, go to the directory you want to use for your project.
  * type **hg clone <full path to your myproject.hg folder>**. if hg is setup correctly, all should be grand. hg add and hg commit files, and then hg push to the Dropbox location.

  * if you want to add a new machine to your git repo, find your directory you want to clone to and type **git clone ~/Dropbox/git/yourproject.git yourproject**. your working directory is now in the yourproject folder. **git push** will push back to Dropbox . **git pull** will pull from Dropbox.
  * the **hg clone <full path to your myproject.hg folder> **will also work for adding extra machines to your repo.

hopefully this explains everything… any questions, leave a comment.

[<img src="http://dotnetkicks.com/Services/Images/KickItImageGenerator.ashx?url=http://blog.lotas-smartman.net/using-dropbox-as-a-personal-git-and-mercurial-storage-area/" alt="kick it on DotNetKicks.com" border="0" />][5]

 [1]: http://db.tt/j0Bv5y7
 [2]: https://code.google.com/p/msysgit/
 [3]: http://mercurial.selenic.com/wiki/WindowsInstall
 [4]: https://duckduckgo.com/?q=git%20tutorial
 [5]: http://www.dotnetkicks.com/kick/?url=http%3a%2f%2fblog.lotas-smartman.net%2fusing-dropbox-as-a-personal-git-and-mercurial-storage-area