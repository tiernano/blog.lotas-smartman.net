---
title: Amazon announces persistent storage for EC2
author: admin
layout: post
permalink: /amazon-announces-persistent-storage-for-ec2/
dsq_thread_id:
  - 26016521
categories:
  - Uncategorized
---
over at the AWS blog, Jeff has posted info about an upcomming feature for AWS, known only as [EC2 presistent storage][1] (maybe it will go by the name EC2PS&#8230;). anyway, the idea is simular to their [Elastic IP addresses][2]: You create an volume, any size between 1gb and 1tb, and its added to your account. you can have as many of these as you want. you then attach them to your instance as required. this is going to be very handy. if it was setup correctly, your DB could be hosted on a volume, and anytime you load up your DB server, just give it a volume to host the DB on. if there is one already there, it would just load it up and your away to go! no info on pricing just yet, but very very cool!

 [1]: http://aws.typepad.com/aws/2008/04/block-to-the-fu.html
 [2]: http://aws.typepad.com/aws/2008/03/new-ec2-feature.html