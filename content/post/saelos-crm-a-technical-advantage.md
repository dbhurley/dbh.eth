+++
author = "DB Hurley"
categories = ["Technology", "Open Source", "Saelos"]
date = 2018-04-21T20:52:00Z
description = ""
draft = false
image = "https://images.unsplash.com/photo-1518687513698-5ef14465356a?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=f8d5d00a079bbdc01896a9ad69854004"
slug = "saelos-crm-a-technical-advantage"
tags = ["Technology", "Open Source", "Saelos"]
title = "Saelos CRM: A Technical Advantage"

+++


One of my greatest undertakings of this past year has been the development and subsequent release of the** [Saelos CRM](http://dbhurley.com/announcing-saelos-beta-crm/)** (_still in beta of course!_). I was able to use my knowledge and experience gained from Mautic (a world-class marketing automation platform) to create a complementary platform for relationship management. I expect if you're reading this you've probably already read the original announcement post (if not, go check that out before continuing). Otherwise, let's take a few moments to explore what an **open CRM** looks like and what it means for the future.

> By the way, if you haven’t looked at [Mautic](https://www.mautic.org) you should definitely check it out. The open source marketing automation platform is second to none and does incredible things for your marketing department.

### Goal

The purpose of this post is to showcase just a bit of the Saelos CRM **technical advantage**. I’ll touch briefly on the methodology and practices implemented as well as the reasons for various technical choices made along the journey.

As a brief overview, Saelos has been written in two distinct sections. A frontend and a backend. This was done to make Saelos completely headless. (_I’ve jokingly made the comment that not only did we create the first headless CRM, but also the first bodiless CRM as well - I’ll explain that in more detail later in this post_) Creating a CRM in two sections like this allows for the absolute maximum flexibility and customizability in the future by an incredibly wide variety of use cases.

> By default Saelos runs smoothly and seamlessly as a single app, so for most users this distinction of “frontend” and “backend” will hold little meaning. But for those more technically minded or for those use cases where it is required Saelos is capable of meeting those advanced requirements.

Without any more delay, let’s start by exploring the backend system for Saelos.

## Backend CRM

Saelos backend (not to be confused with admin or config) is the code platform which interacts directly with the database. This backend manages all the code and logic related to the data and then provides a full API by which the Saelos frontend (and other systems) can interact with this data.

Saelos was written in the “API first” mentality and as such every functional aspect of Saelos is controlled and manipulated via an API. That’s a pretty big statement and gives us the ability therefore to offer **Saelos as a completely headless app**. _Any interface_ can interact with the CRM simply by referencing this robust API.

### Technology

Finally, here is a quick note on the technology involved with the Saelos backend. This platform is written in [Laravel](https://laravel.com/) (Laravel 5.5) as the base, and follows the [12 Factors](https://12factor.net/) of recommended methodology for apps.

## Frontend CRM

The Saelos frontend is the UI platform which the user interacts with directly. This visual interface makes functional calls to the API to return the information in a user-friendly format. This interface is cutting-edge and incredibly intuitive. And that’s not just marketing speak. The Saelos UI responds instantly and is declarative as well as component-based.

The Saelos interface is able to cache responses, storing data in the client’s browser for improved query speed, only making server calls when the data is changed. Doing this takes full advantage of modern browser local caches and makes page load speeds lightning fast (and in many cases non-existent).

Just as the backend is able to function independently of the frontend; so the UI can function independent of the backend. This means, as I joked in the beginning - Saelos CRM is completely bodiless. You can take the Saelos UI and connect it to your data source provided your admin backend implements the same API endpoints.

### Technology

Again, as a final note on the technology involved. The Saelos UI is written completely in [React](https://reactjs.org/). This compiled with axios, redux, and lodash provides one of the best frontend platforms available today.

## Outcome

The outcome or result of this approach to **a modern CRM and sales enablement platform** is abundantly clear. Lightning fast, incredibly flexible, and infinitely customizable. No other CRM or sales enablement tool gives this much freedom. Saelos, a single powerful application, with the ability to exist as two complete platforms, capable of being independently as needed.

To be clear, Saelos does **not** replace Mautic _in any world_. Instead Saelos is a beautiful and perfect compliment to an outstanding marketing automation platform. The lessons learned from Mautic have been applied to make Saelos incredible, but it doesn’t stop there. Already, Saelos is giving back, allowing the Mautic community to begin expanding and improving our code for version 3 (already in the works!). This is a beautiful symbiotic relationship where two open source projects and communities are able to work together to improve each other and I am so excited to be a part of each.

> Interested in learning more about Saelos? Read [the original announcement pos](http://dbhurley.com/announcing-saelos-beta-crm/)t, then check out the [new community website](https://www.saelos.org)!

