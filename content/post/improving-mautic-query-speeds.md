+++
author = "DB Hurley"
categories = ["Mautic", "Technology", "Open Source"]
date = 2017-12-06T16:51:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1517694712202-14dd9538aa97?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=3eab1f496c398631541005fd0f911787"
slug = "improving-mautic-query-speeds"
tags = ["Mautic", "Technology", "Open Source"]
title = "Improving Mautic Query Speeds"

+++


Creating robust applications capable of scaling to handle millions of records in any industry is difficult. Often as a startup there is a focus on speed and agility in development, but that same speed comes at a cost. Fastest development does not always equate to best development. In the startup life we are focused on creating a product people want. Actually, scratch that, **we start by thinking about creating a product people want; but in reality we quickly realize we have to create a product that people will love.**  _And we have to do it immediately._

And whenever a startup moves that fast they focus on today’s issues. Most of the time that’s valid. Very rarely does a startup have to face massive scale problems. Those are tomorrow’s problems solved another day. Mautic was no different. We built our _Minimum Lovable Product (MLP)_ and began an incredible journey. The speed at which Mautic accelerated while exciting is not (or should not be) surprising. **Powerful free software performing tasks never before offered as an open source downloadable product is certainly something to be excited about.** And the world was excited. But this acceleration has happened to others before and so in that sense Mautic wasn’t alone. Which means the problems and challenges we have faced (and the solutions we arrived at as a result) are also not unique.

I don’t say any of the above as an excuse, but instead as background. An introduction because Mautic developers are some of the finest in the world. My previous post recognizing the Mautic code contributors attests to the work they have done and continue to do. But there is a different type of thinking that comes into play when taking software to the next level. Things like query language becomes critically important. Here’s an actual example from Mautic.

> $q->from(MAUTIC_TABLE_PREFIX.'leads', 'l') ->andWhere(sprintf('NOT EXISTS (%s)', $dncQb->getSQL())) ->andWhere(sprintf('NOT EXISTS (%s)', $statQb->getSQL())) ->andWhere(sprintf('NOT EXISTS (%s)', $mqQb->getSQL()))

[_mautic/EmailRepository.php at GitHub_](https://github.com/mautic/mautic/blob/856b6a9cd2ba90088948f6cd290ff3e5c441fd3d/app/bundles/EmailBundle/Entity/EmailRepository.php)

This partial query is used whenever you attempt to load up a list of emails in Mautic. Normally this isn’t a big concern and the query above would have no issues. However, when dealing with a large number of contacts the above query results in significant slowdowns. What’s the solution? Well in this specific case,

[howlinghuffy (Nick Hough) · GitHub](https://github.com/howlinghuffy) came up with a rather simple and seemingly equivalent query that yielded drastically different results.

> $q->from(MAUTIC_TABLE_PREFIX.'leads', 'l') ->andWhere(sprintf('l.id NOT IN (%s)', $dncQb->getSQL())) ->andWhere(sprintf('l.id NOT IN (%s)', $statQb->getSQL())) ->andWhere(sprintf('l.id NOT IN (%s)', $mqQb->getSQL()))

That’s right, by replacing `NOT EXISTS` with `NOT IN` the query yields the exact same results. But from a speed perspective the results are far from the same. Before the modification when Mautic managed 500,000 contacts this page took approximately 200.5 seconds to render. After the query was changed the same query takes 1.04 seconds. That’s right, 200 seconds down to 1 second. **That’s a 200x speed improvement.**

Are there other queries within Mautic that should be evaluated and re-written? Absolutely. And the Mautic community is best equipped to handle this challenge if they know what they are looking for. This was one example. Let’s go find others!

