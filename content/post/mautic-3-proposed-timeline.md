+++
author = "DB Hurley"
categories = ["Mautic", "Open Source", "Community"]
date = 2018-05-11T17:00:00Z
description = ""
draft = false
image = "/images/2018/10/mautic-3-proposed-timeline.jpg"
slug = "mautic-3-proposed-timeline"
tags = ["Mautic", "Open Source", "Community"]
title = "Mautic 3 Proposed Timeline"

+++


The next major topic everyone is very interested in relating to Mautic 3 is the proposed timeline for when things will be worked on...and maybe more importantly when they’ll be available to user. I totally understand this desire and want to do my best to answer this question but I truly hope that everyone understands this is not a black-and-white topic and something that can be easily answered. Why? I’ll answer that quickly and with two words: because developers. I say that in jest but the reality is not too far off from that joke.

In an open source community the release of new versions of Mautic are completely and totally reliant on the time and attention of the volunteers in the community. This is a massive strength for us because we have such a large number of volunteers, but can quickly become an Achilles’ heel when it comes to timeframes. Volunteer work as they are able to. This means while I will propose a series of steps below for the Mautic 3 timeline I will not attach highly specific deadlines or timeframe (at this stage).

Now in the future as we begin to move through this process and as we begin to accomplish certain milestones or goals we will have a better understanding of how things are flowing and can at that time begin to establish some rough timeframes for completion.

With this disclaimer in place let’s take a look at the various steps in a Mautic 3 release timeline and what is involved with each step.

### Discussion Phase

This is where we’ve been living. This is the active ongoing discussion that has occurred in the core channel of our Slack group and if you haven’t been involved in that process, I recommend logging in and sharing your thoughts. This phase is anticipated to have controversy, differences of opinions, and different strategies proposed for how everything comes together.

I’ve written a fair bit lately on this topic as we discuss different options. Starting with [a discussion about what Mautic 3 might look like](http://dbhurley.com/looking-ahead-to-mautic-3/), to [the technological advances Mautic 3 might achieve](http://dbhurley.com/headless-marketing-automation/), to [the business benefits created by Mautic 3](http://dbhurley.com/the-business-benefits-of-mautic-3/).

The desired outcome from this phase is a shared understanding and an agreed upon vision for what we want to accomplish as a community. And I would merely suggest compromise is important to keep in mind as we all work together for the good of the whole (_I’m speaking that admonition to myself as much as anyone else_.)

### Team Formation

The next phase after the discussion phase is a team formation. This shouldn’t take very long but there will be a time period where we want to evaluate who is involved in this team. Anyone in the community can be involved but there are certain traits which will provide greater value to the team. Things such as a strong ability to see solutions in addition to problems. We want problem finders, but not without being solution finders too.

> **Side note**: Problem finders are _critically important_ to our success but if there are only problem finders are also /critically detrimental/ to our success. We must have problem solvers.

Secondly, having technical abilities and interests are vital to this team as well. I’ll try not to make this sound too obvious, but without developers we can’t create Mautic 3. I’ll be the first to tell you, I’m not writing this one on my own!

### Consensus on Course

I know it sounds silly to appear that we’re returning to the discussion phase but that is not the idea behind this step. In this step we are taking the outcomes from the discussion and beginning to outline how we (as a team) tackle those challenges and begin development. We also identify what is possible and not possible to complete in a timely manner.

_Did you catch that? This is the point where we begin to discuss overall timing for successful release of Mautic 3._

We discuss where we want to go, what resources we have, and what is a reasonable time frame to get there. This is what I mean by consensus on course. The direction is set previously; here we focus on timing and specifics.

### Core Areas And Distribution Of Tasks

Next the team begins to identify those specific items that each developer or couple of developers is interested in focusing on. I think this is a particularly important phase because we will make the most progress and find the greatest success when everyone is working on something they love. If you feel passionately about a particular area you will put everything you can into it, and will be able to take incredible pride in the end result. And you’ll know that the end result is something that has been done well. Because you care about it.

I am driven by this mentality on seeing others doing what they care about because I do what I love every day. I am committed to seeing others in our community free to focus on the things they are passionate about as well. Do what you love or move on to something else. This isn’t a duty, Mautic isn’t a chore, it’s an opportunity. Yes, at times Mautic may be a /challenge/ but that only makes the outcome better.

Key things to be examined at this stage will be specific areas and leaders for each: _Every functional and foundational part of Mautic will need to be addressed._ Examples: Campaigns, Segments, Contacts, Companies, Email Builder, Landing Page Builder, Messaging and Channels, Plugins, etc... Let me be clear that is not an exhaustive list. Not by any stretch.

### Technology Proof of Concept

Once all the areas have been identified and work is clearly defined the next step takes place rather quickly. In my opinion this is a key validation step in the entire process. The idea of a proof of concept is focused on creating a representative example of the final product.

The goal of a proof of concept should be to confirm the path and technologies chosen to be implemented _or_ clearly identify the ways the current approach is wrong and what should be done instead. That last sentence is super important. It’s more than just showing something doesn’t work. In the case where there is a misalignment of expectation and outcome, an alternative approach should be identified. (_Remember earlier? It’s not just problem finding, it’s problem solving_)

Once as a core team we are able to evaluate whether the proof of concept has given us the necessary results we can move on to the next step. Keep in mind that each major component must meet a minimum level of expected result for the progress to continue.

### Go Go Go

This is the exciting phase. This is where everyone is turned loose to start creating Mautic 3 code. We have a direction, we have a plan, we have a solid proof of concept and we are prepared to create the future.

As we create new things it is critically important that we include testing at every step. This something that was not done as effectively as well as it should have been done during Mautic 1 and even Mautic 2. I can only imagine there was a collective groan emitted by everyone when reading this part. Writing the unit tests and functional tests associated with new code is only interesting to a very select few. (_I hold massive respect for those who find pleasure and personal fulfillment in creating these test processes and procedures._)

This phase is also where collaboration is important. Without proper collaboration we will find ourselves working in silo’s too much. We can’t work without collaboration and sharing of information. Do not let the importance of this collaboration be lost as we look at the next phase below.

### Silo Alpha Testing

Because we will be creating tests as we build new software we should be able to test our code as we go as well. I’m referring to this as silo testing because it can be done within each functional unit without having to be applied to the greater product at the same time. Again, an [API driven micro-services marketing automation platform](http://dbhurley.com/headless-marketing-automation/) gives us the ability to do this silo’ed testing

During this stage we will also be refining and modifying this code as we go either to make sure it functions optimally or because we have seen additional improvements we can make as we create Mautic 3.

### Bringing It All Together

Everyone gets excited at this particular step. Here we are bringing each of the individual pieces together and begin to evaluate what Mautic 3 looks like. This community core team gets the first sneak peek at what Mautic 3 will present to the world. Yes, this will be an exciting day.

As part of the process of bringing all the pieces together we will repeat some of the steps we undertook during the Silo Testing phase above. We will again evaluate and refine the product based on the interactions between the various parts and identify ways in which the whole of Mautic 3 can be improved to be more than just the sum of the parts.

> **Important**: This should not yield any massive surprises to the team because it is understood that communication and collaboration has been occurring frequently through each of the previous stages.

### Alpha Release Deployment

This is the first of several celebration stages! Here the core team wraps up and presents to the community the alpha version of the brand new Mautic 3. This is a milestone moment not just for the core team, and not just for the Mautic product, but for the Mautic community and the world of marketing automation at large.

The Alpha release is the first fully packaged version of the final Mautic 3 product. It will not be without issues. Did you read that? If you’re following the process of Mautic 3 development and you’re not part of the community core team creating this product it can be easy to miss everything that has gone into this process. And it can be easy to point to problems. May I encourage you to exercise discernment and caution as you do so. Feedback is of course welcomed and encouraged. But everyone should maintain the proper perspective and understanding of the status of Mautic 3 at this point. This is an Alpha release with known issues to be found. **Do not use in production.**

---

### Recap

So, if you’re skimming through this article looking to find specific dates I’m sure you’re disappointed. But you shouldn’t be. Instead let me encourage you to scroll back up and read through the points with a bit more intentionality. Then you’ll understand why the dates are not listed. It will not be until we have reached Consensus on Course that we will have a better understanding and a first attempt to outline specific dates.

Let me reassure you, when we get to that phase, we will absolutely and unequivocally share some preliminary dates and deadlines. Without a clear goal we will meander without enough of a sense of urgency.

Now, if you’re _still_ reading and want just a ballpark idea of dates, the following is **my opinion** on dates and relevant release points.

* Discussion: May 15
* Team Formation: June 1
* Consensus on Course: June 7
* Core Focus: June 15
* Proof of Concept: July 15
* Go: September 30
* Silo Testing: October 7
* Alpha Release: October 30

**Disclaimer**: This is my personal opinion only and is _not_ a finalized roadmap. If anyone attempts to quote these dates as “official” you’ll be immediately and unequivocally corrected!

Please also notice I am **not** showing beyond the Alpha, as we get this far into the future it becomes more and more difficult to identify deadlines and milestone dates. I have ideas and goals in my own opinion which I think would make for an amazing 2018 but will not share those with you yet. I believe as we move along these steps we will be able to gain more clarity into what is possible and along that path I will feel more comfortable to share specifics on other areas of Mautic 3.

I hope this helps give you greater visibility and understanding into what I believe would give us an incredible future and the path I believe would help us get their. Don’t be disillusioned this will not be easy; but I am confident that the rewards we will reap will be well worth every day spent, and every problem tackled. I hope you’ll agree and you’ll join me as we create the future.

