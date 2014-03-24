---
layout: post
title: "Thinking in Layers"
categories:
  - softwaredevelopment
---

In the Spring semester of my freshman year in college, I took my first programming course, [Introduction to Computers and Engineering Problem Solving](http://ocw.mit.edu/courses/civil-and-environmental-engineering/1-00-introduction-to-computers-and-engineering-problem-solving-spring-2012/). It was a basic course taught in Java that started with general syntax and programming constructs then progressed to more complex topics like inheritance, modular design, and basic algorithms. From the beginning I was totally hooked; every task was like a little puzzle that I could focus on. The first few problem sets weren't too difficult and didn't require much design, it was mostly getting a handle of how to represent concepts such as mathematical formulas in code as functions and other similar analogs. I simply read the problem set, put my head down, and coded away on the task at hand.

Fast forward to this past month at my job working on [Social Inbox](http://www.hubspot.com/products/social-inbox) at [HubSpot](http://hubspot.com). Our team had decided to develop a new feature and I was responsible for all front-end (Coffeescript and Backbone) development. Of course, there was no problem set to go by like in school, so I had to take a bit of time to plan, code, test, and repeat. I started working on one part of the feature, but then I stopped to think: _"Hmm... how exactly should I model this data. The way I'm doing it now doesn't seem to be really idiomatic or modular"_, _"Dang... I'm spending a lot of time trying to get this object to have the data I want in it, should the API format it for me instead?"_, _"Uh oh, this little bit is really complicated and involved to develop, are users even going to want this? Or maybe we don't need it just to do some basic user testing."_ This was nowhere near as straightforward as my freshman year problem set.

  
![Mmm, layers](/images/layercake.jpg)

While developing software, I tend to organize my thoughts in different layers - each layer being a train of thought or consideration at a different level of detail. My freshman year problem sets generally only dealt with one layer (represent this thing in code, or get this output), but when developing real software, you're often dealing with five or more layers at once. Lucky for me, later problem sets, and my coursework in the later years of school forced me to focus on multiple layers. 

So what exactly are these layers? Let's take the example of the feature I was developing at work - here are some of the layers I was juggling in my head at some point (generally from lowest level to highest):

  * how should I write this specific line of code?
  * what should this visual element look like?
  * what function should this be in?
  * is this code in the right class?
  * is this feature/component properly architected? modularity/separation of concerns
  * how am I going to deploy this?
  * could we achieve this feature in a completely different way (as part of another feature, maybe not even with code)

Some meta layers might be:

  * are we even making the right thing? do users want this?
  * am I using the right tech stack for this job?
  * how much technical debt is this worth? can I just hack this quickly, or should I design it very well from the get-go
  * should I be working on something else right now?
  * what's on TV?



The more layers you have to juggle, the harder your job becomes. Switching between these layers and prioritizing concerns between them is what can often lead to feeling incredibly frazzled or overwhelmed. Each layer is a different context in your brain and switching between them takes some level of mental capacity, even if they are all related to the same task. Getting good at switching between them reduces cognitive overhead and helps keep your thoughts organized. The times I've failed at switching contexts between these layers, my thoughts get incredibly jumbled and I feel worn out. Generally, the higher level the layer, the larger magnitude of impact it can have on your product. That's why becoming a fantastic slinger of code is simply not good enough to be a good developer of __software__. Becoming the greatest top-coder of all time is like achieving a local maximum in one area of your professional capabilities, but if you're not building the right thing, or properly considering other layers, you'll never reach that global maximum. 

This is partially what made developing for [my startup](http://microeval.com) during YC very difficult. I had all these technical issues and stack questions I was dealing with, but we also weren't sure what we even wanted to build! It's hard to churn out lines of code when you're constantly uncertain about whether you're building the right thing. 

…


When we think of programming as a layered context thought process, I think it sheds light on some other interesting tendencies of programmers. I am huge on tools that increase my productivity, even if it's just one or two seconds I'm saving - why is that? I certaintly waste way more time grabbing snacks or making coffee. For example, using Alfred to go to a specific website I'm working on is probably only two seconds faster than me switching to Chrome and entering the URL directly, but every time I use it, it feels __awesome__. This is because these types of productivity tools are not necessarily about saving _time_, but saving _space in your brain_! When I'm focused on one layer of thought, then realize I should check something on a website that's in another layer, switching between those layers quickly is crucial in maintaining a train of thought. If I have to switch apps to Chrome, figure out what URL I want, type it, get it autocompleted, etc. I've made this context switch much clunkier and I may have lost my focus. It sounds somewhat petty and whiny, but when these kinds of context or layer switches happen hundreds or thousands of times a day, making them happen faster and smoother leads to easier development and overall developer happiness.

The application from this idea of layers is that anything that can reduce the number of layers you have to consider, or the complexity of each layer, will make you more productive, happy, and effective. Here are some things that reduce complexity and make work easier for me:

* A [good product manager](http://www.startupproductmanager.com/) that tries hard to keep you working only on one task at a time
* Communication between team members that makes your part of the work well defined - e.g. a clear API or design spec
* Good internal tooling that makes deploying/developing easy
* Good communication tools like HipChat, Github, Trello
* Co-workers whose strengths are your weaknesses (I am capable, but very slow at making good markup/CSS, so [this guy](http://darowski.com/) has been a lifesaver)
* A [good manager](http://graysky.org/) that helps you be at peace with work, so you don't have to manage the layer of interviewing somewhere else!
* A good understanding of your codebase and architecture


Though I am still a relatively young programmer, I've found that being able to think across layers is one of the skills that I've improved on the most in the past few years. It's also exceedingly clear though that I have much to grow into as well. Being able to focus on a single layer and context, while still maintaining good perspective on all the others is crucial. Every programmer's ability to handle these ideas is different, but the key is being introspective and refining your personal process.

_Note: Someone pointed out that they think of layers as abstractions instead. I agree to the point that abstractions are the coding subset of what I'm calling layers. Since software development is greater than just the code you're writing, things tend to get trickier than just dealing the with proper level of abstraction in your code (which is a difficult task in and of itself)._


[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
