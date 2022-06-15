+++
author = "DB Hurley"
categories = ["Mautic", "Open Source", "Community"]
date = 2017-12-13T16:36:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1524062850143-d314efa60f57?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=853947f9085237ddd61359803f6e457a"
slug = "standardizing-github-for-project-management"
tags = ["Mautic", "Open Source", "Community"]
title = "Standardizing Github for Project Management"

+++


GitHub is a fantastic tool for organizing code, handling issues, and tracking feature requests. Mautic has always used GitHub for its code repositories and more. But there are struggle that come from tools like this and without proper organization or structure it can quickly make a project become a chaotic jumble of questions, feature requests, and code. A lack of standardization destroys an otherwise useful system.

{{< figure src="/images/2018/11/github_mautic_labels.png" >}}

I am proud of the organization that Mautic has around issues and the use of labels. This has historically been something we’ve done somewhat well. We’ve also made extremely good use of the basic code repository and release functionality. You can see this well-organized approach by diving into the **Releases** tab and noting how every release going all the way back is documented and tracked. It’s refreshing to see things like that and speaks to the consistent attention to detail we’ve worked so hard to maintain.

{{< figure src="/images/2018/11/github_mautic_release_list.png" >}}

But I firmly believe there are always things that can be improved and our GitHub usage is no different. So I sat down and looked at our repositories and began exploring ways we could improve our organization and structure around our already amazing product.

## Improving and Explaining Labels

I shared at the beginning that Mautic is very good in its use of labels as it relates to issues and pull requests. But I think sharing what those labels mean and how they are applied is helpful as we discuss a standardization of our GitHub account and organizational structure. Plus, I’m not sure it’s been clearly outlined recently how those labels are used.

**Label Meanings**Here’s a current list of our existing GitHub labels, when they are applied to issues, and how they should be interpreted.

* **Backlog**: Applied to any issue left in an open state longer than 6 months, not automatically applied yet but will be in the future.* **Bug**: Applied to issues directly related to a bug in the production code.* **Code Review**: Applied to issues that require additional review of code by core and community developers before merging will occur.* **Duplicate**: Applied to issues that have already been submitted. New issues will be closed in deference to older ones.* **Feature Request**: Applied to new features or modifications to functionality that is different than originally intended.* **Has Conflicts**: Applied to PR’s mainly that conflict with other parts of the Mautic codebase. Must be resolved before merging.* **L1**: Applied to issues where the fix is deemed lowest level of knowledge to create. Alternatively applied to PR’s where the testing is considered minor in time and intensity. Considered a **Level 1** item.* **L2**: Applied to issues where the fix is deemed to require a moderate level of knowledge to create. Alternatively applied to PR’s where the testing is considered moderate in time and intensity. Considered a **Level 2** item.* **L3**: Applied to issues where the fix is deemed to require a significant level of knowledge to create. Alternatively applied to PR’s where the testing is considered significant in time and intensity. Considered a **Level 3** item.* **Needs Automated Tests**: Applied to pull requests submitted without the appropriate unit tests. _Every pull request requires unit testing of code._* **Needs Documentation**: Applied to pull requests submitted without the appropriate documentation. _Every documentation requires accompanying documentation._* **P0**: Applied to issues considered critically important to resolve. These issues are ‘showstoppers’ and ‘break’ the entire Mautic system.* **P1**: Applied to issues considered detrimental to Mautic functionality. These issues are important but do not stop day-to-day operations.* **P2**: Applied to issues considered annoyances to Mautic functionality. These issues are high priority to fix but do not restrict usage.* **Pending Feedback**: Applied to issues or pull requests that require further information or discussion before being added into work queues or testing.* **Pending Test Confirmation**: Applied to PRs that still require a second successful test confirmation. /Every Pull Request requires 2 successful *+1* tests before merging./* **Ready To Commit**: Applied to PRs that have been tested and are ready to be merged.* **Ready To Test**: Applied to PRs that have been submitted with completed code and are ready for community testing.* **Translations**: Applied to issues that are related to translations. /All language translation strings are handled by Transifex/* **User Experience**: Applied to issues and PRs that are related to how the end user uses Mautic and experiences the platform.* **User Interface**: Applied to issues and PRs that are related to the user interface directly, typically these are cosmetic problems.* **WIP**: Applied to PRs that are not ready for testing. These are **Work In Progress** and represent work actively being done by another individual.

I recognize that list feels long and possibly a bit daunting but I trust the somewhat exhaustive explanation will help clarify how Mautic applies labels to issues and pull requests and makes your life a bit easier as you contribute to the Mautic platform. Other labels may be added in the future either for temporary usage or as additional labeling is needed.

## Improving Feature Requests

The way that Mautic handles feature requests is quite simple at the moment. We have a label marked **Feature Requests** which is applied to every issue created that represents a new feature request (_See I told you it was simple._) There are a few problems with this basic approach to feature request tracking. First, this drastically clutters and increases the total number of “issues” on the project (notice the screenshot above - **728 Issues**). This number actually includes **314 Feature Requests** and inaccurately skews the number of issues. Second, with the current system feature requests are lumped in with every other issue in the system and it makes it exceedingly hard to identify what features have been requested and which are the most popular. This leads me to the first standardization I am recommending we implement in GitHub.

Standardize Feature Request VotingMoving forward I recommend that the somewhat new “reaction” feature in GitHub be used for feature voting.

{{< figure src="/images/2018/11/github_feature_request_reactions.png" >}}

Specifically, **only** the following two reactions should be used for feature request voting: 👍 and 👎. A thumbs-up indicated a +1 vote on the feature and a thumbs-down indicates a -1 vote on the feature.

This will then allow anyone to quickly view the issues on GitHub and with the proper query be able to see a list of feature requests sorted by popularity. To make it easier for you here is the exact link you can use:

> [Most Requested Feature Requests · mautic/mautic · GitHub](https://github.com/mautic/mautic/issues?q=is%3Aissue+is%3Aopen+label%3A%22Feature+Request%22+sort%3Areactions-%2B1-desc)

_As a bonus side effect of this standardization we will be able to programmatically pull this list of issues via an API and allow us to inject a **Top Feature Request List** in other locations as well._

## Improving Pull Request Testing

The second area where I think a bit of standardization may be helpful involves the testing of pull requests. Currently there is a core team in the community managing the testing and committing of pull requests. This ends up appearing to be a bit unclear and not as visible as it should be to the community as well as not demonstrating a clear path for community volunteers to grow into various leadership positions. The core team is open to community members who demonstrate their ability to properly test and merge code contributions. However, the privilege of that responsibility has to be earned through a building of trust. That trust can’t be established without some method of consistent demonstration of personal reliability.

This brings about my second recommendation for GitHub standardization.

**Standardize Pull Request Testing**Our Mautic community needs greater empowerment as I shared above in playing an active role in which pull requests are merged. Our volunteers also need the opportunity to grow into greater leadership roles and become critical parts of the core team. This means community testing of pull requests. Specifically, a **+1** listed as a comment on a pull request implies that the developer has tested the PR in accordance with the test procedures listed in the pull request description.

{{< figure src="/images/2018/11/github_pr_testing_overview.png" >}}

Alternatively, adding a **-1** comment signifies the developer has followed all the same steps and procedures outlined in the pull request but did not find the fix to successfully solve the issue.

{{< figure src="/images/2018/11/github_pr_testing.png" >}}

> Notice in the above comment additional text was added (this is acceptable as long as the comment begins with the appropriate **+1** or **-1** designation.

_And you guessed it, as a bonus we can programmatically use the comment text to extend the use of GitHub to other systems and improve communications as well as automations._

It may not sound like a terribly fancy system, or even a huge difference in how we manage our GitHub account currently but these little improvements and standards in how things are managed make our entire development process better and more streamlined. And the more organized we are, the more efficient we can be. The more efficient we are the better and faster we can grow.

You now have all sorts of new knowledge and insight into Mautic development, go find your favorite feature requests and 👍!

