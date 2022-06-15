+++
author = "DB Hurley"
categories = ["Technology"]
date = 2018-06-09T16:01:00Z
description = ""
draft = false
image = "/images/2018/10/old_ibm_mainframe_multics.jpg"
slug = "tech-tuesday-history-repeats-itself"
tags = ["Technology"]
title = "History Repeats Itself"

+++


I'm certainly not suggesting anything about your age if you know specifically what machine is shown in the above picture, but I suspect there are a few of you reading this post who know exactly what this was and what it represented in tech history. If you are one of those lucky few, I ask your forgiveness for any potential errancies in the post that follows or any assumptions made which are not entirely accurate.

These Tuesday posts are my chance to [highlight technology](http://dbhurley.com/improving-mautic-query-speeds/). Usually they take on a [more technical form](http://dbhurley.com/importance-multi-tenancy/) and discuss topics on a more [programmatic](http://dbhurley.com/importance-of-indexing/) or [procedural basis](http://dbhurley.com/headless-marketing-automation/). (_In fact, some of my posts have  been labeled downright boring as a result of the amount of math involved._) I hope this Tech Tuesday post will take a rather complex topic and make it slightly less technical. Before I get into how the picture above applies to technology today and what I consider a highly relevant topic, let me tell you a short story.

## Once upon a time...

Once up on a time a group of incredibly bright mathematicians and early computer programmers got together to discuss a problem. Rather, they wanted to explore the possibility of making some of their theories a reality. You see, there was a project at MIT called Project MAC (no relation) and a few engineers from a company called General Electric and Bell Labs got together and began to talk. They were excited to see about the potential of building a super computer. A massive undertaking capable of solving all manner of problems and storing data. This new system was called Multics and was an operating system designed to handle complex situations, dynamic linking, procedural calls, and live part-swapping. Multics even supported multiple processors (rare in this day and age).

The list of features found in Multics continued to grow and expand and as you can no doubt begin to tell pointed to the scope and magnitude of this operating system. It was grand and magnificent and _all-inclusive_. But that's where things began to become a problem.

## Multics vs. Unix

As the Multics operating system grew and expanded it became larger and more monolithic in its framework. It added functionality and features for dozens of different applications. Around this same time a new operating system began to take shape as well, one entitled Unix. This OS was simpler. Still powerful and in fact in many cases derived a great number of features and functionalities from the discoveries and work done on Multics. But Unix did something very different.

Rather than creating an operating system that contained all the features in a single package, Unix was built with the concept of a package manager. The ability for an engineer (or systems operator) to selectively add the packages and features desired for their unique application. In this way the power of Unix was delivered in smaller discrete packages and distributed independently rather than as a single all-inclusive package.

And as you are probably very well aware, Unix exploded in growth. Not only Unix, but Linux, MacOS, and even indirectly Windows NT all came about as operating systems offering different features and appealing to different audiences. But Multics? Well, as you may surmise, Multics slowly disappeared from use. the shortcomings of the monolithic all-inclusive platform giving way to the lightweight microservice approach of it's successors.

## Monolith vs. Microservices

This leads me to my thought for today and the the associated title of this post, _History Repeats Itself._ You see, what we have come to see in many modern software packages or SaaS products is this same concept that a singular monolithic platform is somehow superior. There's the misconception that a sole all-inclusive product must provide a better experience because it "does it all". But in this way I am reminded of a quote:

> History repeats itself, but in such cunning disguise that we never detect the resemblance until the damage is done.- **Sydney J. Harris**

Just because we are now calling this solution **SaaS** (it's the latest and greatest iteration of software delivery systems) it must be superior in all ways to anything else. And just like that, we have taken for granted this suggestion because it's wrapped in such a clever disguise. And if we don't recognize the truth we will repeat our past.

Instead, we can be smarter, w**e can demonstrate wisdom and we can keep the damage from occurring by simply stripping away the disguise and recognize the similarities of our situation.**

## Modern Microservices

If we are to learn from our past and create a brighter future we should begin now to push the limits of what our software systems do. I refer in this case to **microservices**. We've discussed this previously here in recent posts. And though the concept might be intimidating at first glance (new things often are) the results are powerful and forward-focused. We can create lightweight, fast, and powerful software systems that take advantage of what we've learned in the past, both the earliest operating system achievements as well as the recent learnings from SaaS solutions.

And this is an interesting point that should be mentioned. One of the most well-known voices in today's software development has written [some fascinating articles on this subject,](https://martinfowler.com/bliki/MonolithFirst.html) Martin Fowler, one of the personal guides in my thinking has said it like this:

> A more common approach is to start with a monolith and gradually peel off microservices at the edges. Such an approach can leave a substantial monolith at the heart of the microservices architecture, but with most new development occurring in the microservices while the monolith is relatively **quiescent**.**- Martin Fowler**

He goes on to make a statement which at first glance may make some very concerned and even sad, but I think it's important to realize there is an end that is better for everyone; the product, the community, and the people using the software. There is a purpose.

> Another common approach is to just replace the monolith entirely. Few people look at this as an approach to be proud of, yet there are advantages to building a monolith as a [SacrificialArchitecture](https://martinfowler.com/bliki/SacrificialArchitecture.html). Don't be afraid of building a monolith that you will discard, particularly if a monolith can get you to market quickly.- **Martin Fowler**

This resonated with me deeply. This is how we have begun developing things at Mautic. We have created a strong foundational platform, we've identified what works and what doesn't and we've created a codebase tested and constantly improved structurally. **Now as we [look ahead at Mautic 3](http://dbhurley.com/looking-ahead-to-mautic-3/) we can be proud of Mautic 2, how it helped us arrive at the point where we are today and how we can [go boldly forward into tomorrow](http://dbhurley.com/marketing-automation-microservices/).**

Mautic isn't perfect. _I'm not sure it ever will be_. But we have been following a plan, a process by which we can continue to improve and [dominate the MarTech](http://dbhurley.com/creating-martech-glue/) space. We have [set a course for success](http://dbhurley.com/looking-ahead-to-mautic-3/) and we have determined to become progressively better each day, each commit, each release. I hope this helps others see the path we have set, the reason why I believe we will be incredibly successful, and offers to all the assurance that this is a course we have crafted with forethought and purpose.

