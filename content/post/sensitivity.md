+++
author = "DB Hurley"
categories = ["tl;dr"]
date = 2018-07-12T12:57:00Z
description = ""
draft = false
image = "/images/2018/10/elastic_sensitivity.jpeg"
slug = "sensitivity"
tags = ["tl;dr"]
title = "Sensitivity"

+++


The concept of data privacy and security grows daily in importance and urgency. I'm personally heavily focused on these topics and I find particular interest in relating them to things such as open source code. There's a lot to be learned and there are many different paths which could be taken. This recent paper took a novel approach and I loved the concept of **elastic sensitivity**.

Elastic sensitivity introduces the idea of _approximating local sensitivity of queries with general equijoins_. This elastic sensitivity is an upper bound on local sensitivity and thus can be used to enforce differential privacy using any local sensitivity-based mechanism. Ultimately, this yields generalized results with negligible performance loss and increased privacy without significant loss of accuracy in query results.

If you only read one research paper this week. Make it this one. Here's a snippet to make you more curious:

> This paper proposes elastic sensitivity, a novel approach for differential privacy of SQL queries. In contrast to existing work, our approach is compatible with real database systems, supports queries expressed in standard SQL, and integrates easily into existing data environments. The work therefore represents a first step towards **practical differential privacy**.

The best part? The researchers have released their work as an open source tool for computing elastic sensitivity for SQL queries.

_**Research Paper**: [https://arxiv.org/abs/1706.09479](https://arxiv.org/abs/1706.09479)__**Open Source Code**: [https://github.com/uber/sql-differential-privacy](https://github.com/uber/sql-differential-privacy)_

Want me to elaborate further? Drop me a note and I'll expand this one into an actual post. I think the idea is incredibly interesting.

