+++
author = "DB Hurley"
categories = ["Technology"]
date = 2018-06-26T14:00:00Z
description = ""
draft = false
image = "/images/2018/10/polynomial_code_computing.jpg"
slug = "pardon-the-math-polynomial-code-computing"
tags = ["Technology"]
title = "Pardon the Math, Polynomial Code Computing"

+++


I feel obligated to begin this post with something that I will rarely due. I'm issuing a disclaimer. What you are about to read is intense. But before you get all titillated thinking I'm about to post something scandalous and make you blush - **don't panic**. I am not posting anything explicit. Rather, what follows is a deep dive into a topic I only recently learned about but am completely fascinated by. Okay, here's your disclaimer:

> **Disclaimer:** The post you are about to read contains math. And not your run-of-the-mill, basic, 1+1 arithmetic. We'll dive in deep into some advanced concepts. Don't let it scare you. Force your mind to think about the implications and expand your horizons.

## The high-level concept

Computers and information systems today process information in a typical somewhat linear fashion. In the early days problems of speed and scale were solved by throwing more hardware at the problem.

_This concept always brings to my mind the possibly mythical, certainly embellished, tales from the Google vaults. In the search engine's time of growth explosion they found it was cheaper to merely add more servers into their data centers in new locations then to take the time to remove and replace the dead ones as they failed._

Regardless the veracity of this seeming tall-tale, the underlying principle holds an element of truth. Everyone knows if your website is running slowly the first thing you do is add more RAM to the server (_followed closely by increasing your number of CPU's_).  That's your quick history correlation. **Bottom line: Adding more machines was the solution for slow servers and delayed processing.**

This is yesterday's solution applied to today's problem. This is wrong thinking. There's a better way, which brings me to the paper I've been studying and [the research being done](https://arxiv.org/pdf/1705.10464.pdf) around the concept of [polynomial coding](https://en.wikipedia.org/wiki/Polynomial) as it applies to optimal designs in matrix multiplication. And finally, we get to the high level concept:

Rather than taking the historical approach of adding more machines to continue the functional processing of slow or lagging machines and still limiting the solution until all processes across all machines have been resolved**, polynomial encoding creates a high-dimensional coded matrix to arrive at the solution in an optimized computational strategy where the minimum possible recovery threshold for the distributed matrix is determined to allow efficient decoding of the final output by the data requestor.**

## The product code matrix approach

I recognize that last sentence is an abomination to the English language but this is a mathematics-based post and not a grammar dissertation so I humbly ask for your clemency. Let's take a look at what this solution means in a diagram (_you knew it wouldn't be a math post without a diagram right?_)

{{< figure src="http://dbhurley.com/media/uploads/2018/06/1ds_vs_3x3.png" >}}

In this (_terribly drawn)_ example I've sketched a 1D maximum distance separable (MDS) code on the left (where we have 3 workers computing the solution) and a single worker failure; and on the right we have a 9 worker matrix based on a √ N by √ N layout with a 4 worker failure (this second example is considered _product code_).

These matrices lead to the following equation for recovery threshold:

{{< figure src="http://dbhurley.com/media/uploads/2018/06/product_code_computation_est_optimization.png" >}}

In essence we can see that the product code approach is a significant improvement over the 1D MDS exemplified above. But the question now becomes, is this optimal. **Does it naturally follow that an increase in the number of workers improves the optimization of the computation?**

The researcher discovers a surprising fact and upon some rather ingenious applied mathematics comes to a very different conclusion. [Qian Yu](https://scholar.google.com/citations?user=SxUNhucAAAAJ&hl=en), a PhD student proposed and then wrote a paper sharing his theorem and proof for identifying optimum recovery thresholds.

## Identifying optimum recovery thresholds

Through the use of polynomial codes Qian demonstrates the optimum recovery threshold can actually be achieved in as little as _mn._ Here is the main result from the paper he published:

> For a general matrix multiplication task C = ATB using N workers, where each worker can store 1/_m_ fraction of A and 1/_n_ fraction of B, we propose **_polynomial codes_** that achieve the optimum recovery threshold.

{{< figure src="http://dbhurley.com/media/uploads/2018/06/polynomial_optimum_threshold.png" >}}

He then determines polynomial codes only require a decoding complexity almost _linear_ to the input size.

I will save you the work associated with proving this theory and will leave the fundamental mathematics associated with the polynomial matrices for your review of the original paper. **The implications from this discovery are vast and far reaching.** It would be a terrible understatement to suggest this be only a step-wise improvement in our computational processing abilities. This is an exponential, order-of-magnitude improvement.

## The Practical Implications of polynomial coding

I'll leave you to contemplate this original work on your own and will instead only highlight a few obvious implications from this revelation in our thinking around computational coding. In current technology our processing happens linearly. We scale things linearly. Through the introduction of polynomial code we can achieve optimal design in record time, because the result is not a simple linear scaled tied to N, number of workers.

The practical implications of this development can be seen in those computationally intense fields first (_think machine learning, or artificial intelligence_). Or consider also the fields where "big data" players have traditionally found strength by "increasing bandwidth" or in more proper terminology, increasing N (_number of workers_). As Qian has proven **the introduction of polynomial code to the distributed matrix multiplication problem revolutionizes these industries and many more**. I have no doubt these findings will have ripple effects though every aspect of the internet as we know it today.

I recognize the depth this post extends beyond what many will find time to review, but should you be interested, here's [the research paper addressing the topic](https://arxiv.org/pdf/1705.10464.pdf). I encourage you to expand your mind and push your thinking to explore new concepts and move your horizons!

