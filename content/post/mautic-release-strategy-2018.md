+++
author = "DB Hurley"
categories = ["Mautic", "Open Source", "Community"]
date = 2018-05-04T17:06:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1449586919022-f3dfddc48a71?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=b2467b115021e6db8cc87e07a6b452f1"
slug = "mautic-release-strategy-2018"
tags = ["Mautic", "Open Source", "Community"]
title = "Mautic Release Strategy 2018"

+++


The Mautic community has a history of various release schedules and timings as we’ve sought to find the best strategy that works for our devs and our users. This tends to be one of the biggest ongoing challenges facing software projects everywhere regardless of the size. We don’t want to create a strategy that is too intensive for the users to maintain and stay current. We don’t want to stuff too much into a single release and hurt our testing strategies or sacrifice our QA process. And on the other end of the spectrum no one wants to wait for years for a release.

This constant back and forth struggle will more than likely continue and I don’t anticipate that we will solve it here today. But I want to share what I believe is the best release strategy for Mautic today.

> **Side note:** Mautic follows semantic versioning. If you need a refresher on what this means, [read this article](https://semver.org/). In summary, Mautic releases three types of releases (X, Y, and Z) and our versions are numbered accordingly: X represents a major release (1.0, 2.0 etc…) this release may break backwards compatibility. Y releases are minor point releases (2.1, 2.2, etc..) these releases introduce new features but maintain backwards compatibility. Finally, Z releases (2.1.1, 2.1.2, etc…) are sub point releases which address bugs and fix issues without introducing new features.

Now, rather than going into the historical study of what Mautic has done in the past we’re going to look at a strategy for future releases. I’m basing the following on discussions I have held with many in the community, observations from other successful open source projects, and my personal experience releasing software to large audiences. I

**Major Releases** (X) are released on a bi-annual to annual strategy. This time frame may fluctuate depending on the volume of work to be undertaken and the code to be modified. Sometimes this process may require extensive testing and significant discussion. Due to these factors major releases are scheduled for either every 6 months or 12 months.

**Minor Releases** (Y) are released on a monthly basis. There isn’t a set in stone date specific for these releases either, but rather a relative time. Minor releases, when they are released are always released on the last Tuesday of the month. Some months may not have a minor release.

**Point Releases** (Z) are released bi-weekly. These releases are quick, really quick. These releases only touch bug fixes. There are no new features being added through a point release. Some of these releases may have only a handful of fixes, and others may be packed full of quick fixes. These point releases should be easy to apply and even easier to test.

This should give everyone a clear understanding of what we are doing and when we release new versions. Now since we’re all on the same page let’s get out there and push Mautic forward faster.

[Recently I wrote about Mautic 3.0 as the next major release for Mautic.](http://dbhurley.com/looking-ahead-to-mautic-3/) While this is an important step forward for our community and our code there’s something that we have to be very mindful of in the process.

**Mautic 3.0 will not happen overnight.** While that phrase may seem obvious here’s what it means. Just because we’re talking about and building excitement around the next major release does not mean we are ignoring Mautic 2.x or discontinuing development on the next Minor and Point releases of Mautic. Because the time to development for a major release undertaking (like Mautic 3) will be significant and lengthy we won’t be halting development on the current series during that process. I told you it sounded obvious but it’s worth remembering.

Mautic 2.14 is the next release to be announced and it includes a great number of new features and bug fixes. All of these need to be tested and applied before we can merge and release. And then we will begin working on 2.14.1 (or 2.15 depending on the features we want to include as a community).

Simply put, even while Mautic 3 is exciting and on the horizon we will continue to fix issues, release new features and improve Mautic through the current release 2.x until 3.0 is announced Stable. Are you interested in learning more about how to get involved in Mautic? Testing the next release is an excellent way to start to learn the codebase. _Need help setting up a testing environment? Let me know and I can point you in the direction of good resources._

As we move forward in our community-lead releases it becomes more and more important that we test and re-test each new feature and each bug fix to ensure it meets the quality that our community demands.

