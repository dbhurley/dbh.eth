+++
author = "DB Hurley"
categories = ["Technology", "Personal"]
date = 2018-05-06T17:04:00Z
description = ""
draft = false
image = "/images/2018/10/github_graphql.jpeg"
slug = "growing-with-github-and-graphql"
tags = ["Technology", "Personal"]
title = "Growing with Github and GraphQL"

+++


I wrote yesterday about [Learning Something New](http://dbhurley.com/learning-something-new/) and thought that maybe a great example would be living by example and take just a very quick post today as a follow-up to share what I learned!

## Picking a problem

I’ll start with the problem. Mautic is growing at a tremendous pace and has a great foundation. (_I laugh as I write that because doesn’t that sound like the most perfect problem to have?_) But those words are the “pretty” way to say what is very much more real and more raw. Mautic is growing so quickly that it becomes a massive chore to keep things organized and focused. (_And that’s a very real problem, for quite a few reasons._) In addition, a great foundation suggests longevity. The Mautic Community is getting some history.

**Fast Growth**Fast growth comes with all types of growing pains, and without being in state of constant and continual focus **things will get lost**, or **broken**, or simply **done ineffectively**. Yep, growth has its downsides.

**Longevity**Longevity comes with the implications of technology problems. And this can mean a variety of things: **outdated**  **technologies**, or **non-standard implementations**, or just flat-out **missing software**. A history and a “way of doing things” can be problematic for the future.

Okay, so now we’re on the same page (at least a little I hope) about a few of the struggles that a growing and solidly built community encounters. As I wrote the article yesterday these are some of the things also floating around in the back of my mind. So I decided to see what I might be able to learn to help with those problems.

## Sorting out a solution

I fully recognize I’m not going to solve all the things in a single Saturday learning exercise. Nor am I going to be able to learn everything on a topic that I need to learn for my own personal edification and since I’m hate feeling like a failure I wanted to pick something manageable. It didn’t take me long to find something to settle on: metrics.

For those who know me, I love facts, snippet-style facts, and specifically numbers. Therefore, having an easy dashboard for viewing statistics about the Mautic community and software. I am also particular about design and the user interface/user experience. And so I set my sights on my target for my project: **Build a dashboard view for Mautic metrics made available on GitHub.**

And so I started by creating a plan. Here’s the very, very simplified version of what I scribbled down:

1. Understand GitHub and what it provides
2. Pick a technology for consuming GitHub data
3. Display that data beautifully.

Wow, that sounds so incredibly simple. (I thought) I’ll be done with this in 30 minutes! (_I was wrong, but that’s another blog post on project estimating probably._) Hindsight is 20-20 and truly ignorance is bliss; all of which is a very good thing because I felt confident and unstoppable (an important way to begin any project). And so armed with a problem, a solution and a plan of attack I got started.

### Grokking GitHub

I have a secret…for some rather undefinable reason, I don’t like the word grok ([definition here](http://www.dictionary.com/browse/grokking)). Regardless, it fits here so I’ll use it. I wanted to get to know how GitHub stored and shared the data from the repositories I was keeping with them. I was fairly familiar with GitHub already due to the amount of time I spent on the platform but didn’t really know as much, at least not detailed, about what information GitHub made available for reading programmatically.

I knew they had an API so I started my journey (and eventually my code) from this source. I would later come to realize something else (as the title suggests) but this is the first example of where for my personal knowledge set I was evaluating their bleeding edge offerings, and starting with what I knew. Remember - the goal with bleeding edge is to move fast and break things. So I set out deep-dive exploring their REST API endpoints and beginning to figure out what data I wanted to retrieve and display eventually.

### Designing the Data (The Tech)

Designing the data involved how to store the information I retrieved. I wanted real-time information and I believed most everything could be either pulled directly or done so with very little programmatic modifications. As a result I decided on going database-less and using a true API-backend (in this case GitHub) as my only datasource.

This meant I could look at technology stacks that were more javascript-centric and frontend focused. Now, truth be told in this moment, I wasn’t going to fall into the trap of losing my day analyzing frameworks. I’ve been having these types of discussions a lot latest as it pertains to [developing Mautic 3](http://dbhurley.com/looking-ahead-to-mautic-3/) and [headless marketing automation](http://dbhurley.com/headless-marketing-automation/) and I knew I’d lose my entire day if I went down that path. So, I continued on by picking an easy one (React) and moving on. (_I would later add different packages in that would be new and different for me and force me to “learn something new” in this world as well._)

At this point I was building a very simple React App that interacted with Github’s REST API and would then display the information in an easy to ready, beautiful manner. Next slide please…

### Displaying the Data (The Look)

Once I had a good idea what data might be available I set out to figure out a way to lay it out and make it beautiful … while still being highly relevant and meaningful. There are thousands of resources available for frontend design so this part of the process is of course highly subjective and I chose to create something that appealed to my tastes and layouts. As with several other spots in this project, I had the advantage of taking creative liberty.

This point is truthfully the one where I recognize my own tendencies to get lost completely. I know the look in my head and will take as long as necessary to get there … pixel by painstaking pixel.

### Putting the Pieces Together

All the pieces were in place, it was time to implement. I created code, designed pages, and built my proof of concept app for what I wanted it to do. And I was pleased with it, but ran into roadblocks. (Not surprising) First, roadblock to overcome was the limiting of API calls done by GitHub. I was working with a React app on my local machine that would hot-load any changes to my local site every time I saved a file. Every time it hot-loaded the page it would re-call the API calls. Thus (as you can imagine) I very quickly hit the non-authenticated API endpoint limits.

**First Challenge**: Implement a more advanced API call that included a personalized authentication token.

After that was resolved I continued on my quest for data supremacy and the all-knowing snapshot of our Github repository. Things continued along nicely but I found that I was retrieving far more data in some instances than I needed and in other cases I was simply unable to pull out the information I needed. I was getting frustrated.

**Second Challenge**: Data was incomplete or too much in the wrong instances and was not allowing me to do what I wanted.

So I [walked away](http://dbhurley.com/learning-something-new/). That’s right, pushed my chair back, went for a stroll, cleared my head. And came back with a fresh outlook. I knew the end result I wanted so I started to step back and [re-think my thinking](http://dbhurley.com/learning-something-new/) about how I was building things out…and that’s when I decided to explore [GitHub’s GraphQL implementation](https://developer.github.com/v4/).

And here, this is where I had to give up my own comfort of a very familiar REST API and look at doing something different. And so I began to break things. I quickly commented out all of my REST calls and began building out [GraphQL](https://graphql.org/) calls instead.

> Pro Tip: I always start with a soft delete whenever possible so as to be able to use my knowledge again later should it prove to be helpful.

**Third Challenge**: Learning GitHub’s GraphQL implementation

That challenge feels very short but let me tell you, it packs a punch. And it took me some time to implement — partly this is due to the fact that every software product is different and thus their implementation of something rather standard (GraphQL) still involves understanding all the data available and the manner by which you navigate their structure to retrieve it. GitHub’s documentation was incredibly helpful in this area.

> **Bonus**: Documentation will make your break your product. As much as you like to think it’s intuitive. It’s only intuitive to you. Good documentation wins wars.

I’ll save you a significant amount of time at this point and fast forward to my current status in this “quick” creation and my “learning something new” experiment.

## Displaying the Data (The Product)

I’m excited to share with you this screenshot of what I built. It’s not complete…quite yet. There are still improvements to be made and I certainly want to explore ways to continue to optimize performance. I’ll be putting the actual site up for everyone to use in the coming days as a contribution to the community. So keep your eyes peeled for that announcement.

{{< figure src="http://dbhurley.com/media/uploads/2018/05/mautic-stats-dashboard.png" >}}

As I said before, there’s certainly more to add and even as I share this I am thinking of improvements I want to make.

It’s important though to achieve small victories. Find the win. I think this was a successful Saturday and certainly forced me to learn something new. Finally, I debated back and forth about including various sources, websites, repositories, example code snippets, that I found useful along the way but decided against this due to the sheer volume of links that would involve. _Not to mention the many , many dead ends and wrong examples I followed as well which might be more difficult to suss out of anything I were to share._ If however, you are interested in knowing more leave a comment and I’ll be happy to answer. Oh, and there’s a bit of an Easter egg in that screenshot too. But I’ll leave you to figure that one out.

I’m off to enjoy the rest of my weekend and I look forward to seeing what you create as you continue to grow and become better. Don’t be afraid to **learn something new**.

