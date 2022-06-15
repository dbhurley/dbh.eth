+++
author = "DB Hurley"
categories = ["Open Source", "Personal", "Technology"]
date = 2018-07-03T13:47:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1428895009712-de9e58a18409?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=8e75a4ee481d63f10742fad4feb97ad5"
slug = "improving-usability-with-simple-javascript"
tags = ["Open Source", "Personal", "Technology"]
title = "Improving Usability with Simple Javascript"

+++


If you read my blog much or listen to the podcasts you know I tend to talk a lot about **active listening**. _(In fact, I just [referenced this](http://dbhurley.com/three-lessons-from-a-sales-rep/)_  _Sunday_.) But the idea of active listening is only the first step in this journey. Beyond the act of [listening](http://dbhurley.com/learning-through-listening/) actively you need to follow-through with the next step. I consider this next step equally important. This next step is **applied** listening. This is where I take the listening I've been involved in doing and actually use it to affect something I am doing. I [apply the knowledge](http://dbhurley.com/demonstrating-wisdom/) I've gained.

Oh, but there's lots of room for learning still, and today is no different. What you're about to read is my **Tech Tuesday** post. Last week we dug in deep and explored [polynomial code computing](http://dbhurley.com/pardon-the-math-polynomial-code-computing/). I'll save you the mental struggle of wading through another concept at the same depth this week and instead explore a more applied technology. In fact, we're going to take things extremely simple this week and look at something I wrote over the weekend.

The idea is simple. I wanted to take my applied listening and do something with it for the purpose of making this blog in particular easier and better for my readers.

## The idea: applied listening

Real life example coming at you. My blog posts usually come in at around 1,000-1,200 words with some going even longer. That's a lot to read, not necessarily when taken individually, but when put into the context of a week's worth of daily posts...it can be overwhelming, and possibly a bit daunting. I was faced with a dilemma. The depth of each post is important, and there's valuable information I'm conveying typically without demonstrating an unnecessary verbosity.

But not everyone has the ability to devote the time required to read a long post each day. In fact, my best friend once mentioned no matter how much they hoped to be able to, they could never keep up with it all. _And this resulted in a negative experience for them!_ The exact opposite of what I hoped to accomplish. I want my readers to feel inspired, motivated, and most importantly in control of their time. When the length of my post dramatically and directly contributed to the opposite effect I felt _I was the one failing them_!

I wanted to find a way to resolve this conflict and provide a better user (reader) experience while at the same time not sacrificing the quality or content of my message. This leads to my proof of concept below.

## The proof of concept:

There are existing plugins which will report the average reading time of a post. These are somewhat helpful in providing information to the reader about the length of time to anticipate a particular post requiring. However, in my opinion this **reading time message** is merely **passive usability**. I've written a good deal about the notion of active vs passive. _(Don't get me started on this in regards to artificial_  _intelligence_!) I call this passive usability because the basic message is merely, "Here's what's happening, deal with it." Somewhat beneficial but not necessarily proactively helpful.

Instead, I'd like to draw your attention to the top of this post (_if you're not reading this on the actual post page, click through to the single post instead of the homepage_). As you can see, my subtext is slightly different and a bit more specific. There's an included link asking a question - got less? I believe these two little words and the included functionality take this usability from _passive_ to _active_. What you have now is **active usability** because the message now says, "Here's what's happening, _want to change it?"_ See the difference? Beneficial while also empowering and proactive.

At this point I was going to tell you to **try it out**. However I am 99% sure the minute I referenced the subtext in the previous paragraph you've already played with the technology and seen what it does. I hope your first response is delight mixed with a hint of intrigue. If that's the case then I've been successful in changing the experience to **a positive "reader experience".**

Okay, but like all magic tricks, this JavaScript to improve usability is so simple you'll shake your head when you learn how it's done. But I don't want to keep the secret to myself. I love to empower people and help them learn new things for their own benefit. Or as I've shown with [Mautic](https://www.mautic.org) I like to reveal what's behind the curtain. (_Open source for the win!_) Keep reading to learn how it's done.

## The prestige

I admit it, I stole this section header from [one of my all-time favorite movies](https://www.imdb.com/title/tt0482571/). In essence, **the prestige** is the secret; it's how the trick is done. So, here's how this JavaScript trick is done:

* First, I've written my post in its entirety as I normally would, then I use a special toolbar formatting option I wrote in the editor that allows me to wrap words, sentences, and paragraphs of text in _span_ tags. Each span tag includes a special class name, such as, **level-10**, **level-25**, **level-50**, **level-75**, etc... any digit between 1 and 100 can be used in association with the **level-** portion of the tag.
* The second step implements a rather standard jQuery UI slider element ( _I'll admit this was the first time in a **very long time** that I used jQuery UI...I almost didn't believe it was still actively used!)_. This slider UI begins at 1 and has a max value equal to **the total reading time** of the post.

> **Side note:** Total reading time as I mentioned previously is easy enough to figure out using an average words-per-minute read time. Nothing super special in here honestly. It's a basic equation.

* The final step involves using a little JavaScript _fadeToggle_ action to show or hide the spans based on the level- **XX** of the particular location of the slider.

It's really that easy. 3 simple steps and you have a "surprise and delight" experience for your readers. But since I'm all about the value of time and the essence of simplicity and convenience I wrote a plugin to perform all this work and all my job consists of is merely selecting the appropriate spans from the toolbar, the plug-in does everything else.

## And finally, let's open source everything.

Of course I plan to open source this plugin so everyone can see the code and have a go at it...and hopefully make it better! Before I do there are a few things I'm still improving before I want to share it, basically cleaning up the code and implementing something I added just yesterday (_take the page url and add an "anchor" such as #3 to be automatically given the 3 minute version of the post_). It won't be too much longer and I'll share the code and I'll be sure to post an update so you can try it for yourself!

Have a great Tuesday and remember, simplicity is key, sometimes the best usability is also the easiest to create. Finally, remember sometimes what looks like a magical user experience only takes a few lines of code and a little bit of extra thought.

