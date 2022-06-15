+++
author = "DB Hurley"
categories = ["Mautic", "Open Source", "Community"]
date = 2017-12-11T16:43:00Z
description = ""
draft = false
image = "/images/2018/11/merit_currency_symbol.png"
slug = "creating-the-mautic-credit-system"
tags = ["Mautic", "Open Source", "Community"]
title = "Creating the Mautic Credit System"

+++


Recently I published a blog post [Recognizing Mautic Code Contributors](http://dbhurley.com/recognizing-mautic-code-contributors/). If you haven’t read that post I’d recommend taking a few minutes and reviewing it before continuing. I want you to review it because there are good things and bad things in that article. While any level of tracking and metrics is better than none there is always room for improvement.

In fact, one of the things that I have been most focused on in recent months has been properly tracking volunteer activity across Mautic. As you read Github does provide some nice metrics to allow for some level of acknowledgement and recognition (purely as it relates to issues and pull requests) but this is such a fractional and minor view of the Mautic community I knew we still had a long way to go. I also knew my good friend Dries Buytaert recently [shared a blog post about the credit system implemented in the Drupal community](https://dri.es/who-sponsors-drupal-development-2017) and this reminded me of the work that had already been done in this area. (What better way to build a system then on the [shoulders of a giant](https://en.wikipedia.org/wiki/Drupal).) And so we began crafting a Mautic credit system.

## The Idea of Merit

As with any system we wanted the Mautic contributions to be recognized in a special and unique way. After consideration of both fun names as well as common names we settled on something that made logical sense and also had a fairly nice benefit of being an ‘M’ word. In the Mautic community a volunteer can earn Merit through a number of different ways. Below I’m going to outline some of the ways a community member can earn Merit.

## Community Involvement: GitHub

We wanted to look at community involvement across a wide range of metrics beyond just GitHub, but at the same time recognized that there was much more activity going on in our repositories besides just issue creation and pull requests. And so we set out to create something special. I’d like to share with you some of what we’ve created so far and then outline what we plan to create next. *Please keep in mind that everything is still very much in a beta stage and changes will continue to be made as the system evolves.*

**Issues**In the beginning we recognized those volunteers who contributed issues simply as a matter of volume and frequency. With the introduction of Merit we have taken that rather rudimentary beginning and created something much more intelligent. A volunteer can receive Merit based on a number of factors when opening, editing, or closing an issue. These factors include the level of difficulty of the issue, the thoroughness of the issue report, the adjusted status of the issue, the number of comments on the issue at the time of the status change and other factors. Sounds incredible? That’s because it kind of is.

**Pull Requests**Similar to issues the early days for pull request attribution and recognition revolved almost entirely around the creation of a pull request. The Mautic credit system again allowed for a fairly massive improvement to this basic implementation. Mautic contributors can receive varying amounts of Merit based on complexity of the pull request, the creation, and subsequent merging of the pull request (and other factors as well).

**Comments**The very nature of comments on issues and pull requests is a tricky one as this can be the most abused area within a credit system. Volume of comments does not necessarily equal quality contributions. Merit attempts to intelligently recognize the value that a comment brings to the issue or pull request. I will be the first to point out that this area will require the most refinement and improvement as we learn what represents value. Merit will get better over time.

## Community Involvement: Forums

But I knew we couldn’t stop with just the code in Mautic. In fact, this was only the beginning. The second area where Mautic needed to create some reward system was in the forums. Just as with the GitHub facet of the community I was interested in gaining a much more detailed understanding of how the community was growing and improving as it relates to our forums. And as I have shared before - the better our knowledge the better equipped we are to improve.

**Forum Posts**In the Mautic Credit System we provide Merit for a wide range of activities. One of the most obvious ways to gain Merit through the forums is by creating a post. Each post creation gives a certain amount of Merit to the forum poster. While this is the most obvious way it is also the lowest weighted method (again due to the nature of determining value associated with a specific post).

**Forum Post Solutions**The greatest way to earn Merit through the forums is by solving another posters question. When a forum post is marked as a solution Merit is credited to the solution’s author.

## Community Involvement: Slack

There is also value to the Mautic community knowing the activity of volunteers as they engage in conversations within the community. Volunteers in Mautic receive Merit when they log in to the Mautic Slack team, when they log in for consecutive days, and when they login and post messages to channels. As with other ways of gaining Merit the Slack engagement method is a constantly changing algorithm and will improve over time.

## Community Involvement: Meetups

Mautic Meetups are offline events but they can still be (_and should be_) a way for community volunteers to gain Merit. Clearly a community member that attends a Mautic Meetup, or even better organizes and leads a Mautic Meetup should receive Merit for their involvement. The Mautic credit system accounts for these events and offers Merit for them.

## Community Involvement: Translations

Translations in Mautic are a huge part of our community and an aspect that makes Mautic truly impressive. As a result we wanted volunteers to be rewarded for the value their translations bring to Mautic’s global initiative. We use Transifex for managing language translations and the Mautic credit system will be deeply tied into this platform so Merit can be given based on involvement on translations as well.

**Translation Merit**New strings added to an existing language, language string reviews, new languages created, and language moderation are all parts of the Transifex translation system that are monitored for Merit.

## Community Involvement: Blog

Mautic volunteers are active in many parts of Mautic and writing articles that are published on Mautic.org is an additional way to help share the Mautic name and be involved in the community. As a result Merit can also be earned for blog article contributions.

## The Future of Merit

As you can probably begin to tell from the above list; Merit is a constantly growing and improving concept. I don’t claim it to be perfect and I certainly don’t think the work on this new Mautic credit system is complete. Every day brings new challenge as well as new opportunities. I have numerous other ideas where we can implement Merit. The beautiful thing about our current technology is the seemingly never-ending list of APIs.

And so the Merit system will continue to evolve and grow and improve. We will learn which of our existing systems needs to be tweaked and make changes based on our understanding and how the community grows.

**Merit Implementation Team**Because openness and transparency is a cornerstone principle within our community and because (as I just shared) the future of Merit involves constant improvement and growth, a team is being created within the Mautic community help establish this initiative and make the result something the entire Mautic community can be exceptionally proud of.

**Merit Open Source**You had to know this last paragraph was coming right? **Mautic is one of the leading open source companies in the world.** We build incredible open source software and we distribute it to the world for everyone to benefit from. Open source is in our DNA. Open source is how we see the world.

> **We are building the Merit platform as an open source tool** so that other communities in the future can also implement what we believe will soon be one of the most robust volunteer recognition system ever built.

If you’ve ever experienced the Mautic community or used the Mautic marketing automation product you will already know that the products we create and that our community is responsible for are beautiful, sophisticated, powerful and yet easy-to-use. The Merit system is no different. This means it may be a little while before we tag a version 1.0 but it doesn’t mean we won’t be sharing our progress and incorporating feedback along the way.

## Next Steps with Merit

I am excited to lead the Merit Implementation Team and help organize volunteers around this effort. I shared in the beginning of the post that we had already begun this initiative and I will be sharing frequent updates on this blog as progress is made. If you are involved in the Mautic community you will begin to see signs of Merit appearing in the various channels I outlined above. And finally your community member profile on Mautic.org will begin to showcase all your volunteer work.

I hope you will be as excited as I am about Merit as you begin to see the system we’re building and the ways it will recognize the invaluable contributions of our volunteers. Mautic is one of the best open source communities in the world and now we will have a practical and specific way to recognize and reward the great volunteers that make it up.

