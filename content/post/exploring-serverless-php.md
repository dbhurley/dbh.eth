+++
author = "DB Hurley"
categories = ["Technology"]
date = 2018-02-15T15:59:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1484557052118-f32bd25b45b5?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=50d27f3c17bcb1b8102f17b64668b092"
slug = "exploring-serverless-php"
tags = ["Technology"]
title = "Exploring Serverless PHP"

+++


I love reading about cutting edge technology and exploring what will be coming next in tech. Most recently I have been reading everything I can about serverless architecture given the growing number of articles and discussions surrounding this trend.

Most recently I read this article, [Rise of Functions as a Service: How PHP Set the “Serverless” Stage 20 Years Ago](https://medium.com/@keithwhor/rise-of-functions-as-a-service-how-php-set-the-serverless-stage-20-years-ago-ccb560c5f422) which very clearly discusses the changes in our technology even if it is several months old. I really liked the comparisons to the early days of PHP and how it relates to where we go from here.

I am eager to see how things like serverless architecture can be implemented in modern software applications like Mautic, or others, but continue to struggle with the fundamental disconnect between these FaaS platforms and a PHP-based software application. I am beginning some exploration in this regard through the use of some different connectors (like the one shared in the article above).

Anyone interested in learning with me (or showing me what they have already done) I have begun my experimenting with this framework: [Serverless Framework - Build applications on AWS Lambda, Google CloudFunctions, Azure Functions, AWS Flourish and more](https://serverless.com/framework/) and plan to update my blog with my progress as I explore this in greater detail. So far I’ve discovered several libraries that offer integrations and/or frameworks for PHP and have settled on using [GitHub - araines/serverless-php: PHP for AWS Lambda via Serverless Framework](https://github.com/araines/serverless-php) as a place to start (don’t hold me to it as I may change this later). I liked this one because it uses Symfony components which is what Mautic uses in core already.

I don’t know if this will be something that we use with Mautic, but I am proud that we currently use the most well-recognized (and still considered cutting-edge) software with Kubernetes. There are always challenges when building out large-scale applications particularly when you want to balance contributing to an open source distributable platform and also create a world-class SaaS platform based on that same code. Kubernetes and Docker containers have given us the ability to do this and I’ve been incredibly pleased with the results so far. (_If anyone is interested in hearing more about that I think it might make for an interesting topic for a future post_).

For now, I’ll continue to explore how Mautic (and other PHP applications) might be able to take advantage of Functions as a Service frameworks to scale even faster.

