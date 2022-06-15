+++
author = "DB Hurley"
categories = ["Mautic", "Open Source", "Community", "Marketing"]
date = 2018-05-01T17:10:00Z
description = ""
draft = false
image = "/images/2018/10/meiying-ng-71590-unsplash.jpg"
slug = "looking-ahead-to-mautic-3"
tags = ["Mautic", "Open Source", "Community", "Marketing"]
title = "Looking Ahead to Mautic 3"

+++


Mautic 1.0 was released out of beta on March 10, 2015. Then Mautic 2.0 was officially released on July 5, 2016. And that's where we have continued to make improvements. This means we have been improving and iterating within the 2.x release for almost 2 years. This holds both positive and negative connotations. I’ll start with the positive.

This duration of a major release demonstrates the significant improvement to overall platform stability we have seen. It also speaks to the flexibility of the existing platform to be improved and built on top of, without major breaking changes needing to be introduced.

But there are also negatives resulting from a lengthy release cycle like this. We’re building software for the internet, the rate of change of software on the internet is growing exponentially; the technology is changing; and the landscape is shifting — **drastically**. By remaining in a single major version we limit the ability to take advantage of those technological advances (if we are unable to make those changes without breaking backwards compatibility).

I’ve discussed the versioning for Mautic previously, if you want to review that information but the tl;dr is we use semantic versioning.

For these reasons the time has come to begin exploring the benefits (and potential downsides) to beginning development of a new Mautic 3.0 release.

## Current challenges

The first thing we need to identify is the **reason why** we would want to move forward with a Mautic 3.0 release. We don’t take these large transitions lightly and there must be sufficient difficulties needing to be overcome and/or new features made available by such a move. To that end, the following are the areas (in part) where a 3.0 release may prove beneficial to the Mautic product.

### Symfony Versioning

This might possibly be the greatest reason for beginning our discussion around a Mautic 3.0 release. Currently, Mautic requires Symfony 2.8 and only works within the 2.x series. This series of Symfony reaches end of support for bug fixes in November 2018. Meanwhile [Symfony current LTS is 3.4.9 and current released version is 4.0.9](https://symfony.com/roadmap). This is a very large problem that we need to resolve. A migration from the current Symfony requirement to even the long term support version (3.4.8) requires a large overhaul to our codebase and framework due to some of the deprecated methods. (I can elaborate on this in more detail in a separate post should it be of interest)

We’re learning as a community through this process and some of the design/architect decisions we made in the early days of Mautic have been improved upon and reconciled so as to not lock us in to specific releases of a framework in the future. Regardless, this upgrade plays heavily into the remaining evaluation of an imminent restructuring and release of a Mautic 3.0 version. And as such opens the door for further discussion around framework implementation.

### Frontend

The first item to be considered as an issue that Mautic 3.0 is capable of resolving involves the front-end interface. Mautic’s interface has remained relatively consistent - even through the Mautic 1 and Mautic 2 series transition. But as mentioned, the existing interface has been in place for nearly 3 years now. This clearly points to the success and clean approach that we took when designing the initial Mautic interface. However, at this point it’s time to consider an update, or facelift, to the user interface.

The frontend modifications are more than just surface level though. Currently Mautic 2.x frontend code is deeply integrated throughout the codebase. While we attempted to isolate the code to the /views folder within each bundle we have inevitably had HTML generated and output from other locations as well and this does not lend itself to a clear separation of frontend and backend. Only with a Mautic 3.0 can we overcome this and resolve this intermingling of views.

### API

Mautic’s API is fairly strong, and absolutely open and flexible - you can review it here: [https://developer.mautic.org](https://developer.mautic.org). But as mentioned in the first item above, Mautic is not truly architected as API first. It pains me to say this because our API is so strong, but it’s not complete. There is more we can do. We need to take our API to the next level and make it truly headless.

The modifications necessary to our API to enable this would also require modifications to many of the functions and classes within Mautic. Touching this many areas of the system is risky and poses additional potential problems which is best mitigated during a major version release.

### Database ORM

One of the greatest issues we’ve faced with Mautic 1.x and 2.x has been implementing at scale. I’ll address speed in particular in a future point but there are two main contributing factors (primarily) to our latency. Our current database ORM structure is one of those factors. Please understand what I’m suggesting. I don’t believe the ORM is necessarily the problem (though there have been open discussions about the implementation of an ORM as causing speed issues in other situations). More so I am referring to our specific implementation of Doctrine ORM. Many places suggest that ORM should be used for smaller projects with smaller amounts of data or for jumpstarting development as a scaffolding before moving on to a full-fledged data schema.

The three greatest problems with ORM-based development are as follows: First, performance degradation due to metadata, DQL, and entity processing (this adds greater overhead than simply fetching the data). An ORM often makes sacrifices in native performance features of a specific platform because of the way it “forces” a one-size-fits-all approach.

Second, Doctrine does a lot of things behind-the-scenes and without any control by the developer. In these instances, the ORM is treated as a bit of a “black box” where functions go in and data comes out with little to no idea how the actual queries are structured, or how they can be refined. Hours upon hours are quickly lost attempting to debug this data and extrapolate what’s happening “inside the box”.

The third point is closely related to the first: an ORM is quite limiting from a developmental perspective. You are unable to properly optimize your database platform for your specific use case and all queries are in this way forced to be “basic” while at the same time the associations are forced to be overly complex due to the way that the ORM manages the relationships.

### Entity Hydration

The second factor which has greatly impacted our speed relates to our entity hydration. The method by which we make our queries, hydrate the results and return them is often bloated and more than necessary. As a result of this overkill we experience latent page loads. Evaluating our use of entity hydration suggests we are doing far more than we should be and this drastically effects our API call query time.

This affects our API call time due to the way the entities are hydrated. Let me explain, when we fetch and format an API payload we create DQL that Doctrine then translates into SQL and then hydrates those entity objects using \Reflection which we then pass through a serializer that reverse-engineers the entities into arrays and removes the elements we don’t want. This process also involves going back into nested associations and removing those unnecessary items as well. Finally we then package up that outcome, encode it as JSON and return it. (Can you say overworked?)

This same process also goes into our forms and the majority of our UI output. Most of the time we only desire the data, but unfortunately we are returning full objects of data that’s been converted a half-dozen times into different PHP objects and arrays before it ever reaches the UI.

### Integrations

Our integrations is one item that understandably needs improvement in Mautic (either 2.x or 3.0). This is as a result of our incredibly fast-paced growth and our attempt to stay ahead of the curve. There’s no denying that as a result we sacrificed some of our “code beauty”. If you haven’t explored our integrations code existing in Mautic then I’d recommend taking a look. What has happened is understandable and yet inexcusable. We’ve added far far too much to the core package and not properly abstracted the integrations as they should be. This failure to decouple properly leads to several problems.

First, this makes plugin upgrades inextricably linked to a Mautic release. This means that at no point are we free to improve upon and release new versions of a particular plugin without waiting until the next version of Mautic is released. There’s no reason to continue this discussion as the problem here is blatantly obvious.

Second, the current integration situation adds bloat to core. There is no reason to bundle plugins with Mautic core while enforcing other plugins to exist in a plugin repository (or [Mautic Marketplace](https://www.mautic.org/marketplace)) to be downloaded and installed by the user. All plugins should function the same way, reducing the overall Mautic footprint and providing a clear path for installation of desired plugins without extra baggage for unused or unwanted integrations.

While there is a path where integrations can be improved upon iteratively within the 2.x series, this is yet another factor to be weighed when exploring the potential of introducing a 3.0 release.

### Speed

One final point to address when discussing existing challenges relates to the overall platform speed. I think it fitting to close this section with this point because ultimately this plays a major factor into the roadmap for Mautic in the future. Currently Mautic performs quite well in a variety of environments.

Mautic has been tooled very well to work for small to medium size databases and while the functionality services every business equally there were some limitations that began to emerge when working with large-scale database implementations. This had lead to a slowdown of various functions within Mautic and requires workarounds to improve.

Secondly, due to the entity hydration and Doctrine ORM implementations done within Mautic (partly to speed up release timing and create software faster) the overall architecture suffered. This isn’t immediately noticeable but does come to light with larger datasets and more intensive query objects (e.g. within campaigns or when creating complex segments).

Lastly, all of the above speed-related issues roll up into a degraded user experience. The goal has always been 300ms page load speeds within Mautic. While this may seem aspirational it does not necessarily mean its impossible. A rethinking of the underlying architecture gives us the opportunity to explore ways to achieve these aggressive goals and deliver an outstanding user experience.

## Potential solutions

Now that we’ve highlighted several of the challenges we’re facing in Mautic it’s time to explore how we solve them. This involves keeping an open mind and looking at every possible solution path. Some of these may be far-fetched, some may be irrelevant and some may seem overwhelming. The goal in this section of the document is to review all of them with an open minded approach.

I’m going to outline the four ways I see this being addressed and hope this serves as the beginning for further discussion. It’s also important to keep in mind that these solutions are not completely mutually exclusive. There is the potential for a combination of these solutions to be implemented for the final desired result.

There are both pros and cons to each approach and rather than attempting to highlight those options in this post I will leave that for either a future post or for group discussion. Instead I’ll merely outline what each solution entails so we have a better understanding of what each represents.

### Re-write on existing framework

The first option we have is to rewrite on the existing framework. At first glance this sounds the most logical and least stressful of the solutions for Mautic 3. This would involve a significant review of the existing code and a harsh look at what should be re-written or even removed. At this time, there’s not a definite answer on the amount of work involved with a framework re-write on Symfony and this will need to be explored to have a better understanding of the level of effort involved.

### Selecting a new framework

A second consideration at a major release point like this is to re-evaluate the framework that has been incorporated so far and determine whether it is the best framework moving forward. This also involves a great deal of work (obviously) as the code would need to be re-written. This is precisely why I suggested you keep an open mind at the beginning of this section. We need to objectively evaluate what is the best solution _with all things considered_. We must step back from looking at just the code but consider everything in its entirety that would be involved with something of this scale.

### Database architecture

Another area where we must evaluate current Mautic 2.x versus Mautic 3.0 is the database architecture. Our existing structure has served us well but if we are exploring the undertaking of a 3.0 series we are defining a release where we have the opportunity to make significant improvements and/or adjustments to the database architecture as well.

Currently our table schema has presented a few problems (though minor) which may be served well by a refresh. This will allow us the opportunity to improve indexing, table columns, and even the overall structure of data. (Need an example? Currently we refer to contacts, however the database table is called leads, while this may seem minor it is a remnant of a speedy release earlier in the 2.x series that should be rectified).

### API first architecture (headless)

The last item I recommend be considered as we explore this stage in our development cycle is a return to the topic of API’s. I mentioned this previously in the problems definitions section. We must reconfigure our existing structure and modify our existing product to be API first. This means we need to evaluate every endpoint, identify which are missing, and extract end-user code from the output (i.e. all responses should be JSON strings).

Mautic 3.0 is the first major opportunity we have to make this improvement. Regardless of the framework selected (after evaluation which we will discuss next) this is the time we should make the improvements to our API. We must make this a priority in order to ensure that Mautic is properly headless. (_Interested in why headless is important? Let me know and I can make a separate post describing the value._)

## Evaluation process

Next comes the step where I need your feedback. I’m looking for end-user feedback, always, but more importantly I would like technical feedback on specific solution outcomes. This discussion has begun in the [core slack channel of our Mautic Slack](https://mautic.slack.com/messages/#core). I would encourage you to join the discussion there should you be interested. While opinions are welcome, those with use cases, specific data, and or use cases based on historical data will be given greater credence.

Let’s explore a few of the items to be handled by this evaluation process.

### Benchmarking

Whenever there is discussion over switching a framework there is usual an instant and visceral response. This response comes from a good place but often times is not backed with the correct factual information. As a result, during the evaluation process in order for everyone to keep “feelings” out of the equation (as much as humanly possible) I want to make sure we back up our opinions with benchmarks and statistics (again, as much as humanly possible).

I recognize that the best benchmark is one that involves our own software written in different frameworks and other factors all kept as control in order to provide a clean comparison. I also recognize this is highly unlikely and presents numerous challenges and as such we must do our best to mitigate these other factors from contributing to the result. _This doesn’t take into account the impossible undertaking of writing the same code on multiple frameworks simply for the purpose of extracting benchmark data._

Based on this information it is deemed appropriate to find existing benchmarks for other platforms built on each of these framework at various degrees of scale and using those as a baseline for comparison.

### Specific use case evaluation

Once we have some basic benchmarks we can begin to explore specific use cases and implementations. This is where we take the best of the best and begin to build out a plan for how the various pieces might work together. Again, the goal is a non-subjective approach to the information and presenting varying use cases for evaluation.

This should not be extremely time-intensive but rather a precursory step prior to the next phase where a proof of concept is mocked up.

### Proof of concept

This step is often where I get most excited myself. Sometimes others may see me arriving at this step and not fully realize I’ve worked through all of the previous steps already. I trust in this particular instance we will make this journey together and share in the excitement of a proof of concept.

As a word of caution, the proof of concept is not a final or even functional application. We simply want to test our hypothesis and theories that we have drawn from the research, benchmarking, and use case evaluations. This is the point where we create code. We build out an example of what it would entail to create Mautic 3 using the solution as defined.

There are several key things to look for with a proof of concept. Code style, readability, implementation methods, and database architecture. This proof of concept should give us visibility into each of those areas as well as a good understanding of the implications of this solution as it relates to page speed and the API results speed.

### Subjective item scoring

The last part of the solutions exploration involves scoring the results from each of the solutions identified on a number of criteria. This will be certainly challenging for our community based on the first word of the heading: Subjective. It’s never an easy task (and an oft avoided one) attempting to rank outcomes where the answer is not a clear black-and-white, yes-or-no. Instead we have to consider all potential benefits and detriments to each solution. We have to weight them according to their perceived merit and potential value.

There are a number of factors that contribute to the success of a solution and while I have highlighted the technical solutions first in this particular post there are others to be considered as well. I will be writing an additional post that will focus on the extraneous factors and how they affect the Mautic product either through a 3.0 release or implementing an update to the 2.x series.

## Next steps

So, now that we have this outline for what we are looking to accomplish and evaluate from a code perspective with a Mautic 3.0 release potential we need to begin focusing on how we best accomplish these goals. Here are the first three steps I am recommending we take as a community as we push forward with exploring Mautic 3.0

### Organize a team

First, we need to organize an evaluation team. This should be a team with technical ability primarily as the majority of the items listed above are highly technical in nature. There will be a time and a place where the greater community will be able to voice their input and opinions and the subjective feedback from the community at large will be desired at that time. This initial team should be developer-centric given the tasks at hand.

### Formulate an evaluation matrix

Once we’ve gotten a team organized and we have carried out the steps for the potential solutions listed above we can begin to draw some results and conclusions. The best way to do so is to compare an evaluation matrix where we can properly identify the pros and cons for each solution recommended. This will help to remove the subjectivity and allow us to focus on the best and most strategic paths forward.

When creating this matrix we will also consider additional items such as time to implementation and community involvement. In addition to picking the most technologically sophisticated solution we must also match that with the existing skills of our community and determine if we need to reach out to other communities for assistance as we seek to grow properly.

The evaluation matrix will not be evaluated at this point and a conclusion drawn but rather be the culmination of the work done to date and distilled down to a meaningful format which can be easily shared in the final step.

### Prepare an RFC

The final step in this evaluation of the Mautic roadmap involves preparing an RFC for dissemination to the community. This is where we seek to get feedback, support and buy-in from everyone. We want to ensure that our community as a whole agrees with the decision made and more importantly agrees because they have received the proper factual information. This is where the evaluation matrix will offer a great deal of insight and information.

This will be a great milestone for the Mautic community as we continue to push the boundaries on marketing automation and the technology used in our software. We are capable and equipped for defining the future of the marketing automation space and this is our next big step in that direction. I hope you can tell the excitement I have not only for the outcome but also for the journey as we grow. I look forward to seeing what comes next!

_Special thanks to [Alan Hartless](https://twitter.com/alanhartless) for his feedback to this blog post_

