+++
author = "DB Hurley"
categories = ["Technology", "Open Source", "Saelos"]
date = 2018-03-14T14:04:00Z
description = ""
draft = false
image = "/images/2018/11/what_do_you_with_an_idea_saelos.jpg"
slug = "introducing-saelos-a-personal-project"
tags = ["Technology", "Open Source", "Saelos"]
title = "Introducing Saelos: A Personal Project"

+++


Some of you may have noticed that it’s been a little while since I posted a longer piece on my blog. That’s not because I haven’t wanted to but because of some other things I’ve been pouring every spare second into. Literally every spare second. We won’t get into a discussion on the topic of sleep habits (maybe I’ll come back to that one - it’s interesting) but suffice it to say, the time I’ve spent has been all-consuming.

But that’s what happens when I am passionate about an idea and want to see it developed. I lose myself in it. I can’t help but think that’s normal though right? Don’t you do the same thing when it’s something you’re incredibly excited about? Regardless, I’ve come up for air now and decided it’s worth taking a few minutes and letting you in on my personal project. This is just something I personally believe the world needs and a shift in a current status that I think can improve lives and business for everyone.

> If you’ve never read the book [What Do You Do With An Idea?](https://www.google.com/search?q=what+do+you+do+with+an+idea) you should stop right now and pick up a copy). _It’s a children’s book so don’t fret - you can finish this one in a few minutes._

So, what do I start with? The solution? The problem? Oh, wait, I know. I should [start with why](https://www.google.com/search?q=start+with+why). Let’s do this:

**I’ve watched people keep lists my whole life.** I’m a list maker. I love making lists of things and keeping track of how I’m doing as a result. So when computers came around people wanted to create lists on it. Natural progression. As is always the case with software one list became multiple lists. Then people dreamed up the fabulous idea of using those lists for showing more information. What a beautiful thing. Now my list of a sentence could be an entire paragraph or more. What if I wanted to define fields and then allow other people to edit and update my lists. **At a very high level this concept of a list item gradually turned into the idea of a single record with lots of data in it.**

Okay, everyone with me so far? I’m going to jump ahead a few steps so keep up we have to start moving faster (I have a thing for speed). Companies began to create software to help with managing these records. They all started with this idea of building a list and adding more and more fields to each record. Display the record differently, use different names for the list items (or objects) then package it as a different software product. Rinse and repeat. This was the state of the world and then the internet came along and these companies all moved their products to the web. Same product, same thinking, but a different medium. _(C’mon people, this is “the internet”)_

But the thinking that built these platforms was inherently the same (for the most part). One company even went so far as to attempt to use a [“No Software”](https://www.forbes.com/sites/adrianbridgwater/2014/10/06/salesforce-splits-the-application-atom-customer-engagement-apps-vs-employee-apps) logo, which attempted to suggest a new paradigm shift in business work, but this was the same thinking, different platform. The software was never the only problem. The thinking about how it was built and the implementation of how it functions is.

This problem of record management was something that I both heard about and experienced myself. A world of “apps” all performing the same CRUD tasks ([Create, read, update and delete - Wikipedia](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete)). Then you could even build your own app on top of an app to add more of the same with different fields you wanted to track or different functionality you wanted to have. But the underlying system was faulty. And though the underlying code was constantly being added to and tweaked, it was the same framework. And I believe people need a change. I believe software today is fundamentally different from software of yesterday. Below are my fundamental principles about software.

Software should:

1. Be modular not monolithic.
2. Be extensible.
3. Solve specific problems.
4. Be active.
5. Be open.

Those five fundamental beliefs shape the work I do and the projects I work on. I absolutely believe this. Let’s look at each very quickly.

## Software should be modular and not monolithic.

My statement here is more than just the concept or idea of bolting more pieces onto a base. That’s the app tacked on to an app tacked on to an app idea which businesses today attempt to do. By modular I mean the core functionality should be able to be removed, replaced, rebuilt and improved upon.

> An example of this lives in the Mautic platform. Mautic functions as an omni-channel marketing platform. Fancy words, simply put, Mautic lets you market across email, sms, social, web, mobile and more. The channels are fundamental to the software, but they are completely modular. Want to use SendGrid instead of SparkPost to send your email, no problem? Have a different ESP? Drop in your credentials and go. What about SMS, Team Twilio or Team Plivo, the choice is yours. Mautic is fundamentally modular in it’s approach.

## Software should be extensible

I believe the idea of extensibility is broken in many cases. This idea is commonly misconstrued in the world through the proliferation of “App stores” within product companies. (_I’m not referring to Apple or Android which provide applications to be run on an operating system._) Software being extensible means something quite similar to the first point. **Modular software can be easily extended to include additional functionality while not losing its core purpose**. But extended to a different ecosystem (or app) through the open exchange of data.

## Software should solve specific problems

Too many software companies today try to be all things to all people. The world is not your target market. I believe in the idea that software should be accommodating and flexible but this doesn’t mean it’s a one-size-fits-all approach. Flexible means the software should fit your business rather than your business conforming to the software; but the problems to be solved are unchanged. This means the processes might vary, but the solutions remain the same.

## Software should be active

I know this point sounds funny but the majority of today’s software is passive. It responds to requests, it dumbly regurgitates what it has been given and spits out a mangled version of an answer ... _when asked a question._ I call this passive software. In contrast, I believe software should be active. It should proactively assist me in performing a task or reaching a goal. _(These many software assistants are absolutely passive but that’s another post.)_ Software should be helpful and active in enabling the user to move faster and do more, intelligently.

## Software should be open

I left this one to last because it’s the foundation. It’s the belief on which everything thing else is built. I believe software should be open. There are countless studies, reports, and white papers on the reason why so I won’t sidetrack this discussion. I believe in open. An open software empowers people and enables the other points above.

## Relationship Management

All of that brings me to a problem I face. I needed something to help me manage relationships. But everything that existed in the world was old, bloated, slow, inflexible, and closed. Yep, pretty much the exact opposite of everything I listed above. It’s frustrating. But solvable. I believed I could create a platform that managed relationships but was built on the principles I believed in. So I started working.

I wanted to create something blazingly fast (regardless of the number of people) being managed. Something modular that could be easily extended, something that solved some very specific problems, something active in its interactions, and most importantly something open.

I’d like to introduce **Saelos.** An open platform built on the software principles I shared. The purpose: customer relationship management. That’s a tricky one to say because instantly I’m sure you conjured up one (or more) companies that offer a solution under this label. But Saelos is different. Very different. Because Saelos is something I’m calling **active software**. By this I mean that not only does it manage customer records differently but it also actively helps you maintain connections, build relationships, and accomplish your goals by actively assisting you. Task completion, recommended actions, process improvements, and intelligently created reminders are just a few ways that Saelos will do things for you.

Let me be clear: Saelos does far more than just incorporate another workflow builder and follow simple step-by-step procedural tasks created by a user. **Saelos builds them for you, _and then executes them_.** And informs you along the way, all the time enabling and empowering you to do more of what you should be doing with the right person at the time you should be doing it.

Possibly the best part of this entire project is that Saelos is built on the right foundation: **open**. This means Saelos can be downloaded, self-hosted, installed, configured, and improved upon by everyone.

I have so much more to share and I can’t wait to show you what’s been created. I’ll be giving early access to the project I hope by the end of the month. (Friday, March 30 2018). I know it’s forbidden to set a date in software development…but I’m feeling pretty good about this.

Are you interested? Do you believe in the same fundamental principles as me? Would you like to experience something different in how you manage and interact with people? [Sign up for early access here](https://saelos.org/), and let me know. Oh, and subscribe to notifications on my blog to be on the insider’s list. I’ll be posting more information and (hopefully) screenshots in the days and weeks leading up to the release. It’s coming fast, I hope you’re as ready as I am.

