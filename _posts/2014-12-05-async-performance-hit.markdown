---
layout: post
title:  "Async != Fast"
categories: software
---

In a recent campaign to improve our HubSpot's performance, we learned a simple but important lesson: __Async != Fast__.

Javascript heavy apps and libraries have become much more prevalent on the web, and HubSpot is no different. We use Backbone on the client which consumes a handful of any of our hundreds of API endpoints via AJAX. We also load third party libraries with script tags at the end of the body. Even though all these scripts and requests are happening asynchronously, it's very dangerous and downright wrong to think that your app won't suffer a performance hit because of them.

Though asynchronous loading means your Javascript can do other things while it's fetching a resource, there are a couple other considerations to keep in mind:

## 1. [# of Concurrent Requests](http://www.browserscope.org/?category=network)

Browsers have a limited number of requests they can make at a single time. In Chrome for instance, that number is 10. If you have 11 requests happening at once, that 11th one has to wait for one fo the first 10 to return. There is also a limit per hostname, so if you're making many requests to your own API, you could be causing waterfall'ing of your requests.

## 2. Parse/Eval time

In the case of a Javascript library, your browser still has to parse and evaluate the script after it has been downloaded. Javascript is single-threaded, so this is time spent not doing anything else. Any client-side libs that have a large footprint should set off some alarms.

-----

With our performance monitoring, we recently discovered that one aysnchronously loaded Javascript library was slowing down our app significantly.

<a href="http://cdn2.hubspot.net/hub/319577/file-2180960427-jpg/load_time_3rd_party_lib.jpg"><img src='http://cdn2.hubspot.net/hub/319577/file-2180960427-jpg/load_time_3rd_party_lib.jpg' style='margin-top:10px;display:block;margin:auto;width:600px;'/></a> From the graph, you can see in cases where the third-party script finished downloading before our internal scripts, it delayed time to interactivity and the execution of our own scripts by nearly a full second. It was essentially a race condition based on how fast the third party script loaded.

So before you add that latest and greatest Javascript library or add another request to your app, remember that asynchronous __does not__ mean fast.
