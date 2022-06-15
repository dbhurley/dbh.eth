+++
author = "DB Hurley"
categories = ["Technology"]
date = 2018-06-12T15:30:00Z
description = ""
draft = false
image = "/images/2018/10/chaos_monkey_simian_army_netflix.jpg"
slug = "my-favorite-netflix-open-source-code"
tags = ["Technology"]
title = "My Favorite Netflix Open Source Code"

+++


We're kicking off **Tech Tuesday** with this post! I will probably post code discussion (_I had a second post I wanted to share but is 2 just simply too many for one day?_) on these days. I'll also post some topics that are more studies of other technical projects, or as in today's example, share a tech resource I find useful, instructive, or otherwise helpful. In this post we're going to explore one of my favorite _brands_. Let's examine [**Netflix**](https://medium.com/netflix-techblog) as a brand and a company **separate** from the ubiquitous service they provide.

For the uninitiated, Netflix has **149 open source projects** listed on [Github](https://github.com/Netflix). _Clearly they believe in the philosophy of open source._ It’s certainly exciting and refreshing whenever large organizations demonstrate their transparency by open sourcing their various tools. In my opinion this is a great example of a “rising tide raising all boats"…or to use another popular analogy “sending the elevator back down”.

Anyway, the difficulty of selecting a favorite project is dramatically increased by the sheer number of projects to choose from. In an attempt to give a fair representation first, I’ll share some general stats based on their existing projects statuses and then I’ll share my personal favorite. (_**Spoiler**: my favorite is different than the general population._)

There’s a number of ways to explore popularity of projects on Github (where Netflix and millions of others store their open source code), but the main ones are **forks** and **stars**. I would go further to say their order of relative importance is also as I have listed them here. By this I mean, someone who has forked the code is more likely to be demonstrating an intent to _do something_ with the code, while a starred repository may simply be a _bookmark_ to reference later or merely to "favorite" the open source code. Regardless, I think it’s not a bad idea to look at both of these metrics in regards to Netflix’s repositories (open source projects) and by this get a feel for which projects are considered the most popular by the open source world.

> As a bit of background, I did some digging to begin with to ensure I was looking at the best way to gather this data, because I certainly wasn’t going to attempt to build a list of stars and forks from their main repository page by hand…**I’m a programmer by heart, so I’m lazy** (although others consider this brilliance). As a result of my Google-fu and my somewhat lacking Github website knowledge, I finally came across the pages I link to below which made my job ridiculously easy.

## Forks:

[https://github.com/search?o=desc&q=user%3Anetflix&s=forks&type=Repositories](https://github.com/search?o=desc&q=user%3Anetflix&s=forks&type=Repositories)

_Based on this filtering here are Netflix’s 5 most **forked** repositories._

1. **[Netflix/Hystrix](https://github.com/Netflix/Hystrix) (2,814)**: Hystrix is a latency and fault tolerance library designed to isolate points of access to remote systems, services
2. **[Netflix/eureka](https://github.com/Netflix/eureka) (1,361)**: AWS Service registry for resilient mid-tier load balancing and failover.
3. **[Netflix/zuul](https://github.com/Netflix/zuul) (1,044)**: Zuul is a gateway service that provides dynamic routing, monitoring, resiliency, security, and more.
4. **[Netflix/SimianArmy](https://github.com/Netflix/SimianArmy) (929)**: Tools for keeping your cloud operating in top form. Chaos Monkey is a resiliency tool that helps applications tolerate random instance failures.
5. **[Netflix/ribbon](https://github.com/Netflix/ribbon) (517)**: Ribbon is a Inter Process Communication (remote procedure calls) library with built in software load balancers. The primary usage model involves REST calls with various serialization scheme support.

## Stars:

[https://github.com/search?o=desc&q=user%3Anetflix&s=stars&type=Repositories](https://github.com/search?o=desc&q=user%3Anetflix&s=stars&type=Repositories)

_Based on this filtering here are Netflix’s 5 most **starred** repositories._

1. **[Netflix/Hystrix](https://github.com/Netflix/Hystrix) (13,920)**: Hystrix is a latency and fault tolerance library designed to isolate points of access to remote systems, services
2. **[Netflix/falcor](https://github.com/Netflix/falcor) (8,814)**: A JavaScript library for efficient data fetching
3. **[Netflix/SimianArmy](https://github.com/Netflix/SimianArmy) (6,544)**: Tools for keeping your cloud operating in top form. Chaos Monkey is a resiliency tool that helps applications tolerate random instance failures.
4. **[Netflix/eureka](https://github.com/Netflix/eureka) (5,570)**: AWS Service registry for resilient mid-tier load balancing and failover.
5. **[Netflix/zuul](https://github.com/Netflix/zuul) (5,323)**: Zuul is a gateway service that provides dynamic routing, monitoring, resiliency, security, and more.

As you can see from the above, the two lists are remarkably similar, and yet they aren’t identical. I’ll leave the debate and resulting inferences for these deviation as an exercise for you. Now, I’ll share with you my personal favorite open source project from Netflix.

My all-time favorite has been around a little while and most recently is also bundled in one of the repositories above in addition to being a standalone project.

[**Netflix/chaosmonkey**](https://github.com/Netflix/chaosmonkey): Chaos Monkey is a resiliency tool that helps applications tolerate random instance failures.

To understand why this is such **an incredibly brilliant repository and something which demonstrates the sheer genius of the Netflix operations team**, you should read this article: [Netflix Chaos Monkey Upgraded – Netflix TechBlog – Medium](https://medium.com/netflix-techblog/netflix-chaos-monkey-upgraded-1d679429be5d). Here’s a highlighted quote from this post:

> "We created Chaos Monkey to randomly choose servers in our production environment and turn them off during business hours."

…I can’t even begin to explain how cool this is from a programmer’s standpoint. (_"Cool" after the utterly terrifying part has been resolved _and there’s a sense of confidence in the infrastructure and codebase_._) Basically, the name comes from the idea of unleashing a wild monkey in the Netflix data centers to randomly rip apart instances and destroy connections — all while Netflix continues serving customers **without interruption.**

Now, to be fair, the **Simian Army** repository above is the evolution of this concept, as in this project they have also included the **Latency Monkey**, **Conformity Monkey**, **Doctor Monkey**, **Janitor Monkey**, **Security Monkey**, **10-18 Monkey**, and finally the upgraded **Chaos Gorilla**.

If you’re interested you can [find a write-up of each of these simians on the Netflix Tech Blog on Medium](https://medium.com/netflix-techblog/the-netflix-simian-army-16e57fbab116) (one of my all-time favorite Medium blogs to read…_voraciously_).

Because their desire is to create a resilient, faultless environment and they are willing to subject their production environments, in real-time, under load, to these types of random chaos tests, this is by far my favorite open source project from Netflix. And then they made it open source so everyone can benefit. **This improves (_or should improve_) the code quality and infrastructure of every major company, product, and team working on the internet.**

