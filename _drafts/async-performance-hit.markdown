---
layout: post
title:  "Async != No Performance Hit"
categories: jekyll update
---

At HubSpot, we have a 'dumbbell' architecture that consists of tons of micro-services on the API end, and heavy Backbone/Javascript on the client side. As a front-end developer on the Social Inbox team here, our architecture is a joy to work with. It's very easy to work on the product and iterate quickly when developing apps on the front-end.

As Javascript-heavy apps and libraries have become more prevalent, asynchronous loading through AJAX or putting scripts at the end of your `<body>` tag have become the de-facto ways of having non-blocking requests so the rest of your app can run. To load any page in HubSpot, we are generally hitting several APIs asynchronously and composing the data and templates on the fly. However, it's very dangerous and downright wrong to think that since you're loading resources asynchronously, that your app won't suffer a performance hit. 

## __ Async != No Performance Hit__

Though asynchronous loading means your Javascript can do other things while it's fetching a resource, there are a couple other considerations to keep in mind:

1. # concurrent requests [link]()
Browsers have a limited number of requests they can make at a single time. In Chrome for instance, that number is 10. If you have 11 requests happening at once, that 11th one has to wait for one fo the first 10 to return. There is also a limit per hostname, so if you're making many requests to your own API, you could be causing waterfall'ing of your requests.

2. Parse/Eval time
In the case of a JS lib, after it has been downloaded, your browser still has to parse and evaluate it. Javascript is single-threaded, so this is time spent not doing anything else. Any client-side libs that have a large code-size should set off some alarms.

We use a ton of small scripts, both our own and third party. Through our performance monitoring though, we recently discovered that one aysnchronously loaded javascript library was slowing down certain pages of our app significantly. In cases where the third-party script finished downloading before our internal scripts, it delayed time to interactivity and the execution of our own scripts by nearly a full second.

Before you add that latest and greatest Javascript library or add another request to your app, make sure to consider the performance cost.


Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].


[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
