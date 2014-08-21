---
layout: post
title:  "10 Practical Tips for Software Engineers"
categories: software
---

These are a few tips and strategies I've picked up over my (short) career. See what works for you!

## 1. Be a rubber ducky, find a rubber ducky
Have you ever talked to someone about a problem then realized the solution as you were describing it? This happens all the time. Talking out loud often gives your mind clarity and organization around a problem. In scenarios like this, the person you are talking to is considered a [rubber ducky](http://en.wikipedia.org/wiki/Rubber_duck_debugging). Everyone on your team should be open to being a rubber ducky and talking to one. Sometimes, if you're lucky, the rubber duckies will even offer good suggestions.

## 2. Get feedback fast
Try to get feedback on code as soon as it makes sense. If you're working on a Pull Request flow like we do at HubSpot, make some trivial change and open the PR as soon as you can so you have a place to discuss design and code. Talk to your rubber duckies and make them quack! It's cheaper to iterate on prototypes than a 'finished' product.

Depending on how your team is structured, this might mean not writing code at all initially. Mockups, designs on a whiteboard, etc. are a lot cheaper to throw out than hundreds of lines of code.


## 3. Get End-to-End first

When working on a new problem or feature, it's very easy to dive right into the nitty gritty details. I've found a better approach is to get end to end as quickly as possible (or alternatively, to a "Hello world").

For example, say I needed a user click on a web page to trigger some complicated calculation, then save some results to a server. You might want to dive right into figuring out how to do the meaty calculation. For me, a better approach is to set up the event handler for the user action, mock the calculation with some fixed values, and then fire the API request to the server. This way, I can test my system end to end before I've figured out every detail. I now have a feedback loop which helps me iterate and code faster. The design might not be perfect initially, but by seeing how things fit together, you get a clearer picture of the full system you're trying to design.

At HubSpot, we take this concept even further by pushing features to production before they're even finished so that we can test them internally. We can do this because of our gating infrastructure (more on this in another blog post).

## 4. Know when to step away from the keyboard
Sometimes, putting in debuggers, console.logging everywhere, and just bashing at the keyboard is a good way to test code. Other times, when you're having a tough time managing a complex design or problem, you need to stop looking at your screen. It's silly but sometimes I solve problems or have great insights in the bathroom. My wife, who is also a software engineer, does her best thinking when she sleeps (literally as she's falling asleep, or sometimes even in dreams...). Take a nap, go for a walk, go to the bathroom, whatever, but find ways to think away from your computer.

## 5. Automate
  The most efficient developers automate many of their tedious processes. A common misconception about automation is that it's about saving time. Certainly when you automate a process you might end up saving time. But even more valuable than saving time, automation allows you to chase a train of thought uninterrupted and lowers the barrier for actually completing tasks.

For instance, if there was a complex SQL query I needed to run very often to get some metrics, I am much less inclined to run the query if it is long and I have to type it every time. If instead, I've saved it on my clipboard using a program like [Alfred](http://www.alfredapp.com/), or saved it somewhere for easy access, I'm much more likely to run the query often.

## 6. You can always DRY off later
It's tempting to write perfect code and figure out every abstraction when you're designing new code. I've found that abstractions are dangerous time sinks when starting on something new, even when they seem obvious and easy to design. Rather than abstract right away, I'll simply copy paste methods as I'm prototyping. It helps me move quicker on new projects at the beginning and often times reveals better abstractions and concerns than I could have discovered on a piece of paper or whiteboard. Of course the caveat is that you have to actually clean up the code before it rots.

## 7. Stay mobile
Mobile as in your body, not your iPhone. Coding is not the most strenuous of activities so it's important to force yourself to stay active. Make sure to get a good stretch in a few times a day and walk around from time to time. At HubSpot, we have a club that does pushups before lunch three days a week. I like to do a few pushups every hour or so to keep my blood flowing and muscles stretched.

Sitting for long periods of time has caused me intense shoulder and back pain in the past, but having a standing desk has eliminated those pains completely. I'd strongly suggest trying it out for short periods of time if you experience pain related to sitting.

## 8. Read ahead
Reading documentation, technical articles, and code can often be confusing and maddening. Before flailing your arms and scratching your head, read ahead a bit and get more context. Programming concepts are difficult to express in a linear form. Reading ahead will often make it more clear what a previous sentence or code snippet is talking about.

## 9. Write meticulous notes
This tip might not jive with the less organized devs out there. I take meticulous notes in Evernote every single day about what I've worked on, problems I've encountered, and how I've solved them. These notes have become invaluable to me whenever I encounter a problem that I know I've solved in the past but can't recall the solution to. It also has the added benefit of helping you recall your accomplishments when its time to have a 1 on 1 or performance review.

## 10. Plan for tomorrow, today
Either before I go home for the day, or at night at home, I make myself a todo list in Evernote of what I'd like to accomplish the next day. Then when I get into work the next morning, I am focused and have a clear agenda so I can hit the ground running. Personally, getting a good, productive start to the day often carries through the rest of the morning and afternoon.
