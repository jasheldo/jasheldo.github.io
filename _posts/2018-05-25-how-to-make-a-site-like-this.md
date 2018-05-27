---
layout: post
title: "How to Make a Site Like This Part 1"
description: "Guide to making a site similar to this."
category: Web Development
excerpt: A brief outline on making a set of static sites with Jekyll
---

A few days ago I decided it was time to make a personal website. I didn't want to use a 
template system because that's lame. I also didn't want to write something from scratch 
because that is not my wheelhouse. I found a happy medium with 
[Jekyll](https://jekyllrb.com). It has numerous advantages too:

- I can create a blog with no SQL configuration.
- I can add a number of static pages with ease.
- The pages are hosted on [GitHub](https://www.github.com).
- Pages and posts can be created in 
[Markdown](https://daringfireball.net/projects/markdown/syntax) and 
- Pages can be built using [Bootstrap](http://getbootstrap.com).

Let's be upfront: I love the simple, clean layout from [Sourabh](https://sourabhbajaj.com) 
so much I shamelessly copied it. That said, his directions didn't completely explain how 
to replicate his site starting with a Jekyll install. I'd like to take his explanation 
and expand on it, starting from installing Jekyll and getting to the finished product.

This is the start of a multi-post outline on creating a specific Jekyll site. Of course, 
if you want a full description on using Jekyll for building a bunch of static sites 
please refer to the official documentation.

With that, let's get started:

### Setting up Your Environment

#### Installing base packages

You'll need to install a few pieces of software. Fortunately, on a Mac it's simple. Open 
a Terminal and run the following commands:

        gem install jekyll #install Jekyll
        gem install jekyll-compose
        gem install jekyll-redirect-from

If you're not using Git and Github you'll need to install Git and setup a GitHub account. 
I highly recommend using [`Homebrew`](https://brew.sh) if you're on a Mac. Install 
`Homebrew` and use it to install `Git`.

        /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
        brew install git

#### Setting up GitHub

If you don't already have a GitHub account, you'll need to visit [GitHub](https://www.github.com) and set up an 
account. Once done, create a new repository and name it `username.github.io` where 
`username` is your GitHub username. During the setup process, be sure not to include any 
of the optional files they suggest such as a README or gitignore file. You want a 
completely empty repository (repo).

#### Local directory

At this point we're going to diverge from Sourabh's instructions and hand craft this new site. 

Create an empty directory where you'd like this site to live. I created my directory in 
`~/Sites/portfolio`. In terminal, change to this directory and run the following commands:


        cd portfolio
        git remote set-url origin git@github.com:USERNAME/USERNAME.github.io.git
        git push origin master

You've now initiated a local Git repo and have it tied to the GitHub repo you just made. 
You can now develop the site locally and push changes to the GitHub which will then 
render the pages.

However, the right way to go about developing the site is to use the built-in server to 
run the site locally to see what it looks like. Then, debug it on your computer and once 
you're comfortable with the changes, push them out to GitHub.

You can run the local server by moving to the `portfolio` directory and running

        jekyll serve --livereload
        
In the next post, we'll explore creating the site using Jekyll.