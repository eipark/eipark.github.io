---
layout: post
title:  "Starting my blog on GitHub Pages"
date:   2014-01-03 00:46:02
tags:
  - meta
#permalink: starting-my-blog-on-github-pages.html
---

Like many other software engineers, I've wanted to write a blog for a long time. I keep meticulous track of my thoughts and ideas in Evernote, but was never able to jump the hurdle of actually finding a good platform to host my blog. It's a lame excuse, but a common one. Fortunately, the phenomenal new [GitHub Pages](http://pages.github.com/) site along with [Jekyll](http://jekyllrb.com) makes it extremely easy to get a blog started.

Both GitHub and Jekyll have done an incredible job of identifying the pain points that stop most people in their tracks. To get set up, I:

1. Create a new GitHub repo for my blog https://github.com/eipark/eipark.github.io
2. Install Jekyll (`gem install jekyll` and `jekyll new my_blog`)
3. Create a file called `CNAME` in my repo with `erniepark.com`
4. Update DNS records on my domain registrar to point to GitHub

That's it! Writing posts is as simple as creating a new markdown file in your `_posts` directory.

I hope to use this blog to post primarily about software development, Christian living, personal finance, and sports (hockey in particular). However, I find writing thoughts down to be therapeutic so I may rant about random other things as well. I grappled with the idea of focusing on one area for the site, but due to the nature of how content is discovered these days, I figured it wouldn't make much of a difference to throw everything in the pile.
