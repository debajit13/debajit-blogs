---
title: Deep Dive Into Git(Part I)
date: "2020-07-07T22:40:32.169Z"
description: What is Git? Why understanding it is so much important? In this article, we are going to understand it.
---

Git is a distributed version control system. Now we are going to understand what is the meaning of each word in this definition.

Before that, there are two things that you need to know. They are client and server. So the client is the computer which you use like your PC and server is a big computer which provides or takes the data from the client. It is not the proper definition of client and server. But for the seek of understanding Git you can also think it like this.

There are two types of systems:

1.  Centralized System
1.  Distributed System

![centralized system](https://miro.medium.com/max/700/1*sk12XX2YQUVAinZnpRZUTw.png)

In Centralized systems, there is a central server and other client machines are connected with it. Let us take an example, in a company some developers write codes in their computers and at the end of the day they send all their code to the server. This kind of systems are great but also have some problems. Just if somehow the server fails then all the code have vanished and all hard work they have done just gone forever. That is the primary cause of why Distributed systems came into the picture.

![distributed system](https://miro.medium.com/max/700/1*t5Zf0lQtXAggNXz5NtQXFw.png)

In Distributed systems, there is a central server and clients are connected with it just like the Centralized system, but the main difference in this system is all the client machines have their copy of the code that they wrote previously. So if the server crashed they have all the code in their computers. For that, they do not face too much loss like a Centralized system. Git system based on this distributed approach, so we always have a local copy of the code.

![before and after learning git](https://miro.medium.com/max/700/1*ERQU99MvNvEKpT8jaLAegQ.png)

Now the other term is called version control, what is it? Before understanding that let us consider a situation where you have a project and you don’t know anything about version control. Then first you create a project and named it “Project”. Some days later you add or delete some code and renamed it to “Final Project”. After some days you again change some code and renamed it “Final Final Project” and this process goes on. Now if you want to go to a particular version of your project, it’s not easy for you to go and find a project folder where you have certain features or deleted some of them. It is not practical at all.

So what Git does is it creates a version for your project and change it after some changes you have made in that project. So now you have created a project that is initially at v1.0. After some change, turns into v1.1 and so on. Now if you want, it just takes your one command to go back from v10.9 to v1.9 or vice versa using Git. So now your project is much easier to manage.

So why version control or Git is so much important? Firstly, it helps you to keep track of the changes you have made in a project over time. Secondly, It gives you the ability to go back to a particular version. Most importantly, You can easily contribute to someone else’s work.
