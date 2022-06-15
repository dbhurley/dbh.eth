+++
author = "DB Hurley"
categories = ["Marketing", "Mautic", "Technology", "Open Source"]
date = 2018-05-16T16:55:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1487621167305-5d248087c724?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=d182301b76273a044751897a1206c297"
slug = "marketing-automation-microservices"
tags = ["Marketing", "Mautic", "Technology", "Open Source"]
title = "Marketing Automation Microservices"

+++


Recently I was on the phone with a good friend of mine, he’s not directly involved in a technology sector and as such it makes our conversations incredibly fun, light-hearted, and many times _not focused_ on the highly technical discussion and debates I normally find myself sucked in to. This particular chat however ended up steering into my work and some of my recent blog articles and he made a comment that caught my attention. He said, “Hey man, at some point can you explain **what exactly are you talking about with Mautic 3** and this new version you’re constantly getting excited about?”

I’ve written a good deal lately about Mautic 3, from [my initial thoughts on the subject](http://dbhurley.com/looking-ahead-to-mautic-3/), a [business benefits piece](http://dbhurley.com/the-business-benefits-of-mautic-3/), to a pretty [technical introspective](http://dbhurley.com/headless-marketing-automation/), and even [a timeline for how I think it might unfold](http://dbhurley.com/mautic-3-proposed-timeline/) (yes, it’s aggressive). Being a good friend he had read all these articles, and this meant he knew what I was talking about and what I was doing, but he didn’t necessarily have a strong understanding of what it meant and what it actually would do. What he was asking was a very good question and _exactly what I like to hear_.

I get great advice from lots of people, but some of the best advice comes in the form of a question, and comes from those that are **not** too close to the situation. Those questions are the best for me. They help me to re-focus, or maybe to state it better, they help me to step back and see the forest, not just the trees.

## The Marketing Forest

I hope this post will be a less technical and better view of the marketing automation forest as I see it. First, I think this is an extremely important point to not overlook. Maybe you don’t call it a forest, necessarily, maybe you prefer to call it a ‘landscape’.

> I need to take a quick moment to tip my hat to the incredible work done by Scott Brinker ([@ChiefMartech](https://twitter.com/chiefmartec)) and his team creating the marketing landscape each year. If you haven’t taken a moment to appreciate it - [do it](https://chiefmartec.com/2018/04/marketing-technology-landscape-supergraphic-2018)).

Regardless of what you call the space, it’s overwhelming, and as Scott suggested in a [recent blog post](https://chiefmartec.com/2018/05/martech-consolidation) the space is only going to continue to grow. There will not be a mass consolidation of marketing tools but instead a proliferation as more and more are introduced. This leads Scott down an interesting line of questioning and thinking. I call it interesting because he begins to touch on the very thing I have been [speaking and writing about](http://dbhurley.com/headless-marketing-automation) . I’ll touch more on that in a second, but first, let’s talk about the implications of such an expansive (and constantly expanding) marketing space.

### Expansion means competition

What we see occurring in the marketing space is not uncommon nor should it be something to be afraid of. Instead, the increasing number of companies entering this market improves the customer experience. As more and more services are offered the customer will (hopefully) find a better and better solution to their problems. At least that’s the idea. If businesses happen to overlap, competition comes into play and the product will improve. (also there is the side effect of potentially lowered prices as well!) .

I’m always a fan of competition, I believe it has been well proven that such competition results in a better environment and experience for everyone. This also encourages companies to be better and better.

There’s a second outcome I see as a result of this massive and somewhat exponential growth. As Scott suggested, and as I’ve talked about many times previously - with so many options and companies available in this space there becomes a greater problem to be solved, a greater need to be met. This is where Mautic is uniquely and (dare I say it) perfectly poised to meet the need.

## Marketing Disconnected

I recently read an article published by [KPCB](http://www.kpcb.com/) recently which shared the number of marketing tools that a single enterprise business uses. It’s mind-blowing. Care to take a guess? If you guessed 10-15, you’re off by a mile. If you thought 25-50 you’re getting closer (_and by closer I mean halfway to right_). The number of different marketing technology services, platforms, or products that an enterprise uses is nearing 100 unique systems. This is the product of an 8,000 tree “marketing forest”. But while some may see a problem; I see an opportunity - a massive opportunity.

I see an opportunity of epic proportion that only an open source, agile, API-driven marketing automation platform can attain. You see, a proliferation of tools means there needs to be some manner for communication between them, some exchange platform for the data to be shared, and other advanced data transformation to be performed.

What this marketing disconnect needs is a connector. Something that can seamlessly integrate with all those tools, fluidly fill the gaps between them, complement them, and improve the marketer’s experience. But this shouldn’t be another app with a fancy UI. Even more importantly this can’t be another platform seeking to be the “data holder”. The one place where all data must be kept (i.e [single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth))

> **Side Note:** This is a point worth more consideration. Almost without exception every existing platform seeks to be the source of truth. They believe only by _owning the data_ are they able to “win” the competition to be best. Therefore, _everything_ they do is to protect and extend this perceived trophy.

### Big Data Is Not the Answer

This point is a big one. Many businesses today focus on big data (or at least they used to). _What do I mean by big data? I’m glad you asked. Big data means collecting as much information on as many people as possible._ Once all that data is held the theory is that predictive analysis and data scientists can extrapolate potential results and thus make smarter marketing decisions. But there is a shift in the tide and this commonly held belief is wavering.

> **Interesting Read:** If you’d like to learn more about what causes this change in thinking, I’d suggest reading this article: [Mastering the game of Go without human knowledge](https://www.nature.com/articles/nature24270.epdf?author_access_token=VJXbVjaSHxFoctQQ4p2k4tRgN0jAjWel9jnR3ZoTv0PVW4gB86EEpGqTRDtpIz-2rmo8-KG06gqVobU5NSCFeHILHcVFUeMsbvwS-lxjqQGg98faovwjxeTUgZAUMnRQ).

If the collection of more and more data is not the answer, what is? What is the solution that makes marketers more successful and handles the overabundance of different and disparate tools currently existing in the marketing forest? **Enter marketing microservices**.

## Marketing Microservices

I realize there are some that fully understand what a microservice is and what value it offers. For those I apologize if I make it sound too simple or oversimplify the technical nature of the definition. My goal is to summarize in such a way that everyone feels comfortable talking about marketing microservices.

Personally, I’ve always seemed to learn best with examples and clear instructions. The simpler the better. ( _The popular subreddit: [explainlikeimfive](https://www.reddit.com/r/explainlikeimfive/) is a personal favorite of mine as you might guess._) And so I’ve picked a **hypothetical marketing microservice** to be used. And as you might imagine this is something Mautic is preparing for part of M3.

### A Marketing Microservice Example

Almost every marketer I know and every system of record (you know, the place that wants to be the source of truth we explored earlier) has a common dilemma. In fact, marketing automation platforms in particular struggle with this issue on a daily basis. The problem is recognized but the problem is not easily solved. Curious? For our example, we’re going to assume the issue is _contact record de-duping_. The ability to recognize and remove (or merge) duplicate contacts in a database.

This is a problem everyone wants to solve but everyone takes a slightly different approach and everyone has found equally varying levels of success. A marketing microservice would allow a marketer to send contacts to a headless, marketing automation microservice provided by Mautic, which would de-dupe the records and return the result. Everyone wins.

The result is a marketer with a cleaned database of contacts, existing platforms don’t have to worry that another tool is “fighting” to be the “source of truth” and Mautic has provided a valuable microservice to fill-in a gap. Once again we have the idea of filling in the gaps. A clear opportunity for a fluid connecting of marketing microservices providing highly relevant, extremely efficient, valuable, results.

> **Side note**: Interesting side effect, when the data storage is irrelevant the marketer is empowered to do things better, without worrying about switching costs, data privacy concerns, and which platform is /the/ platform for their data. _This changes everything._

And this is only one very simple example of the power and capabilities of a headless marketing automation platform. Don’t let the slightly unusual terminology throw you off - it’s only a technical way of saying, **a platform which fits in with other existing tools seamlessly and painlessly, complementing, strengthening, and simplifying existing marketing stacks and allowing the marketer complete control over where and how their data is stored, manipulated, and displayed.** But that's a lot of words! So I shortened it to headless marketing automation.

---

I hope this has helped to showcase what a marketing microservice is and how it can completely revolutionize the industry. All of the incredible power of marketing automation where and when its needed. No more data security and storage concerns. An improved experience for marketers. Finally, a solid, robust way for 100 different and disparate systems to begin effectively talking to one another and improving each other. This is the type of thing Mautic 3 is prepared to handle. This is the opportunity Mautic, an open source marketing automation platform, is uniquely able to address.

If you haven’t taken a look at [Mautic](https://www.mautic.org), I suggest you do so now! Maybe after reading this you have some great ideas for other ways marketing microservices can add value in the overwhelming marketing landscape. [Join in the discussions being held](https://mautic.slack.com), add your voice to the Mautic 3 development process and become a part of something bigger than yourself, something that will truly improve the lives of marketers everywhere, and change the way the landscape is viewed.

