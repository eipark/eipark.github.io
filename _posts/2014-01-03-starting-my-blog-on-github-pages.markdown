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

1. Created a new GitHub [repo](https://github.com/eipark/eipark.github.io) for my blog
2. Installed Jekyll (`gem install jekyll` and `jekyll new my_blog`)
3. Created a file called `CNAME` in my repo with `erniepark.com`
4. Updated DNS records on my domain registrar to point to GitHub

That's it! Writing posts is as simple as creating a new markdown file in your `_posts` directory.
