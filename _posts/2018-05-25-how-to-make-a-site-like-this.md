---
layout: post
title: "How to Make a Site Like This"
description: "Guide to making a site similar to this."
category: Web Development
excerpt: A brief outline on making a set of static sites with Jekyll
---

A while ago I decided it was time to make a personal website. I didn't want to use a template system because that's lame. I also didn't want to write something from scratch because that is not my wheelhouse. I found a happy medium with [Jekyll](https://jekyllrb.com). It has numerous advantages too:

- I can create a blog with no SQL configuration.
- I can add a number of static pages with ease.
- The pages are hosted on [GitHub](https://www.github.com).
- Pages and posts can be created in [Markdown](https://daringfireball.net/projects/markdown/syntax) and 
- Pages can be built using [Bootstrap](http://getbootstrap.com).

Let's be upfront: I love the sleek, clean layout from [Sourabh](https://sourabhbajaj.com) so much I shamelessly 
copied it. That said, his directions didn't completely explain how to make the site look nice so let me 
expand on his directions.

**Step 1** : Create a new github repository `username.github.io` in your account.

**Step 2** : Install Jekyll using the command `gem install jekyll`.

**Step 3** : Create the clone of Jekyll bootstrap and set the remote to track the repository you just created.

        git clone https://github.com/plusjade/jekyll-bootstrap.git portfolio
        cd portfolio
        git remote set-url origin git@github.com:USERNAME/USERNAME.github.io.git
        git push origin master

**Step 4** : Change and modify your theme using [Twitter Bootstrap](http://getbootstrap.com/).

**Step 5** : Create the pages you want using `rake page name="pages/about.html"`, similarly create the other pages as well.

**Step 6** : Create your first post using `rake post title="Hello World"`.

**Step 7** : Remove the default example posts `rm -rf _posts/core-examples`

**Step 8** : Edit the `index.md` as per requirements.

**Step 9** : Change the default template as need be, it is located in `_include/themes/bootstrap/defaults.html`. I made some style change and removed the buttons and navbar at the side to set my current layout. And I added the links to the pages I had created in the `step 5`.

**Step 10** : Just push the source code to the github repository and Github will automatically render it, `git push`.

**Step 11** : If you find anything wrong in this guide. Please let me know about it.