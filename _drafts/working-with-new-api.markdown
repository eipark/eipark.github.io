---
layout: post
title: "Components of a good API doc"
categories:
  - development
  - engineering
  - api
---

Good APIs are hard to design and good documentation hard to write. Using an API effectively is just as big of a challenge. At the most obvious level, you need to be able to find information about each endpoint, parameters, response codes, etc. This is the base level of expectation for any decent API doc. But to truly master and wield an API to the fullest, it's **context** that is most important. By context I mean understanding the underlying data model, concepts, and objectives that the creators of an API had in mind. Without this context, using an API becomes a chore of hunt and peck for the specific field of data I need, rather than understanding how the design of an API is meant to solve problems.

As an engineer on HubSpot's Social and Ads teams that integrate with many 3rd-party APIs, too many times I've foolishly jumped into a task just looking for that "one thing I need". I'd sink a bunch of time into a solution before realizing there was a much better approach or that I completely misunderstood how the API was supposed to function. Similarly, I've implemented solutions only to later find out the API had many hidden assumptions or undocumented connections that made my life very difficult.

Context, when provided by APIs, and gathered by implementers, is the key to avoiding these mistakes.


To that end, I think every API doc could benefit from these "THREE SIMPLE TRICKS":
  * a graph/visual of the data model and the connections therein (I'm sure there are static analysis or other graphing tools that can assist with this)
  * a conceptual overview of how the API was designed and intended to be used

When learning a new API, make sure to:
  * understand the higher level concepts of the API first
  * don't assume the first endpoint or object that gives you what you want is the best solution. Measure 10 times, API call once.
  * use StackOverflow and forums as an index into common problems
  * never assume documentation is infallible. test your assumptions early and often.







* working with APIs are hard. documentation is often imperfect or incomplete and you only get a small window into how it all works
*A hardest part is CONTEXT. 
* do a lot of up-front work and understand the API conceptaully first. seems obvious, but easy to fall into trap of solving the singular call or problem youre tryign to solve. mapipng out conceptually the API type (SOAP/REST, ID constraints? hierarchY) and data model and what the company is trying to achieve is key
  * facebook Graph.
  * google api docs pretty good: https://developers.google.com/adwords/api/docs/guides/objects-methods. diagram, explain concepts.
* understand authentication model
* read ahead, read multiple docs. file support tickets. get context from StackOverflow/forum if common problem. often hard to get context.


