+++
author = "DB Hurley"
categories = ["Mautic", "Technology", "Open Source", "Marketing"]
date = 2018-05-10T17:01:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1497005367839-6e852de72767?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=3f03b3ffa6b14c7a7cac4cce68648b07"
slug = "the-business-benefits-of-mautic-3"
tags = ["Mautic", "Technology", "Open Source", "Marketing"]
title = "The Business Benefits of Mautic 3"

+++


Longer posts are always an undertaking. It involves a lot of thought and attention to detail to make sure the information I share is clear and easy to understand. There’s a lot of work that goes in behind the scenes for a finished post to come across as simple. So, usually before undertaking a post like this I like to take a deep breath, a big stretch, and smile. Something about staying positive before wading into the deep end once again.

I should say also, the smile comes from the amazing volunteers in this outstanding community. Together we are building an **amazing platform** that stands out from the crowd and **differentiates** us in a number of critical ways.

One of the biggest ways we can demonstrate our expertise lies in our ability to push the envelope and advance new thinking in the landscape of marketing automation. Yes it may be a daunting task, but I would suggest that our community, and our open source approach to marketing automation is the only way this level of growth can be achieved in a stable fashion. We have an opportunity that no one else has. And it’s our duty to push this space forward. It’s our obligation to change the world of marketing and give everyone the tools to market effectively using the latest in technology.

With that quick bit of motivation to get us started, let me dive into the business benefits of Mautic 3. I’ll follow that up with a proposed timeline for this product improvement as a separate post.

## Business Benefits

Let’s start by exploring the business benefits by making this shift to the next major release of Mautic software. I want to highlight that these six benefits I’ll suggest are not necessarily distinct only to a Mautic 3 release. However, in each case I believe the greatest growth and leap forward would be realized in a major version release.

> _Stay with me to the end; I’ll discuss in a little more detail tomorrow the idea of migrations and how those would and should be handled with a transition like this._

**Speed (Should I say Agility)**At the risk of sounding extremely cheesy I noticed as I typed up these benefits that many of them ended in the same suffix and sounded like they fit together. The marketer in me could not help but then adjust the one outlier (Speed) to also fit this same mnemonic. Thus, for point 1, we have agility, or speed, as an improvement that the end user would experience and thus become our first business benefit. Faster is better (in almost everything - yes, I realize there are exceptions to every rule). Moving to Mautic 3 for our platform will enable us to completely gut parts of the system that have experienced significant slowdowns in the past. Those areas where we see bottlenecks in processing times can be alleviated and the problems with overall system performance can be improved.

Of course we could see improvements in the current branch (Mautic 2), however, due to the discussion that has been held it has become evident that the greatest improvement to speed can be done with a re-write of several areas of the platform. This begs the question - if we must re-write core parts of the platform regardless of the branch in order to improve our speeds, should we not make the necessary improvements to improve speed everywhere and better structure our underlying architecture for the future at the same time? The argument is an easy one to make, in particular when considering our existing infrastructure is reaching end of life for support and we have fallen significantly behind the latest current release (by multiple versions). This must be addressed.

An improvement in our overall speed continues our competitive advantage as we already enable businesses to complete processes in a faster manner than other marketing automation platforms today. This furthers our lead in this area.

**Flexibility**The second area where a Mautic rewrite gives us a business benefit lies in the flexibility of the platform. We already built Mautic in an open source way that allows businesses to create a marketing automation workflow that suits their unique business needs but that was always step one in a multi-step plan. The next step in that journey involves giving the business even more flexibility to manipulate and control their data.

Mautic 3 enables businesses to take advantage of existing data stores, and other sources of truth beyond the Mautic database by enabling the separation of frontend from backend code and functionality. Any database that incorporates the necessary API endpoints will be able to take advantage of the Mautic 3 frontend (and vice versa). I spoke specifically to this point in a [separate blog post](http://dbhurley.com/headless-marketing-automation/) which I would encourage you to read if you’d like to know more about this point.

**Integrability**Mautic was created from the beginning with the concept of mixins - the addition of functionality to the core platform through a Mautic Marketplace which closely resembled a CMS extension directory. This was a fantastic first version and demonstrated that the desire and interest from a community and business perspective clearly existed. With the launch of the new [Mautic.org](https://www.mautic.org) website at the beginning of 2018 we saw a massive uptick in the number of integrations and their downloads.

Businesses wanted this ability to integrate. We wanted to continue in this direction with an overhaul to the existing mixin (plugin) infrastructure and architecture in Mautic 2. But this is still only a step in the journey. Extraction of the existing mixins from core and the unique repositories linked to each mixin allowed for faster development and release of individual integrations. Mautic 3 pushes the software even further in this regards. This is done by doubling down on the API integration layer and the manner in which these mixins talk to the backend (and frontend) of the platform.

I’ll touch on this point in greater detail below as this serves to become a very unique selling point for Mautic and a massive differentiator for our platform in the market. Let’s look at that next as we discuss defensibility.

**Defensibility**One of the most challenging obstacles in any company (or community) is understanding and identifying the manner in which the software being created is defensible.

> **Side note**: When I use the term defensible I am referring to our ability as a community to offer something unique that our competitors will never in reality be able to achieve or offer to the same extent as we can.

Understanding what makes a product defensible is a challenge in and of itself and often is very difficult to do in the earliest days of a community. Therefore Mautic 3 is the opportunity where we can begin to apply our learnings in the marketing automation space and begin to clearly define those areas and functionalities where we are unique and defensible.

And this is where the excitement builds for me. This is the culmination of our learning, our open source core, and our ability to push the marketing technology landscape further. Our defensibility is found tucked into many of these business benefits I’ve shared already and will share in the next two points. The underlying mechanism and ability for our open source platform to be split and used interchangeably either from a frontend UI or as a backend API gives us the unique and defensible ability to be the **first ever truly open source, API driven, suite of marketing automation micro services.**

I know you’re probably very interested in hearing more about this but I’m going to simply say, you’ll have to wait for that specific blog post if you’re interested in digging in. _I promise you I’ll publish it soon, because when something is this exciting I have a very hard time keeping quiet for long._

**Extensibility**The concept of extensibility as different from integrability is nuanced and tenuous at points. But I would suggest the differentiation is clear enough to allow extensibility to be a separate business benefit. Just as integrability allows the software to work seamlessly with other tools “plugged into it” the idea of extensibility allows for the core functionality of the Mautic platform to be extended to additional areas and implementations.

This underscores the notion that an open source API driven marketing automation micro services platform can do far more than any monolithic platform ever could and allows for the functionality of the platform to extend far beyond the limited reach of existing tools.

Extending the platform requires an API first approach as recommended for Mautic 3. This level of abstraction provides the tools and system interoperability necessary for this business benefit to be properly realized.

**Stability**The final point I’d suggest as a business benefit for moving to Mautic 3 is a tricky one, particularly because it requires more than simply creating new software. In order for Mautic 3 to be substantially superior to the existing latest release of Mautic and provide additional business value in the sense of a superior stable product implies several fundamental truths. First, Mautic 3 can’t be merely “new code” - it must be _tested code_. By this I mean while the code may be new, this does not require it to be either untested or unstable.

New Mautic code will not be merged into Mautic 3 until it has the appropriate unit test coverage and functional tests. Otherwise we run the risk of experiencing the same flaws and bugs as Mautic 2. Very fast releases of new features but this surpasses the number of fixes provided to reported bugs.

Therefore, in a release of Mautic 3 we can create a solid, and fully-tested platform capable of being improved upon as needed without fear of the potential to break something unrelated with each new feature release. Overall the stability of the platform is massively improved, the documentation excels, and the usability demonstrates an excellent product. (_[Read this post I shared recently on the topics of stability, why I think it’s important and what benefits it will provide us](http://dbhurley.com/balancing-startups-and-stability/)._)

