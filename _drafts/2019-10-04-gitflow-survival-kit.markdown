---
layout: post
title:  "Gitflow Survival Kit"
date:   2019-10-04 21:53:00 +0000
categories: [development]
tags: [github, git, notetomyself]
comments: true
---

At work, my team uses git with gitflow branching model for version control. As most of my days are spent bossing people around rather than doing any real work I tend to feel rusty when I do need to commit some code. Google always obliges, but I end up frustrated trying to find that one brief and to the point resource I liked the last time. Over the last few months, I ended up keeping a brief git / gitflow cribsheet as an unsaved tab in my text editor. Yup, just sitting there and waiting for the trouble, to be closed without saving. What a better way to generate some new content for the blog and keep my notes safe than putting them into a blog post? :stuck_out_tongue_winking_eye:

Disclaimer: this is not meant to be exhausive git / gitflow coverage, just the comands I tend to use most frequently, 

## Git Basics

Create an empty repository on GitHub / BitBucket / insert your provider here. Clone the repository, start creating. 

{% highlight sh %}
git clone [user@]host.xz:path/to/repo.git/
{% endhighlight %}

If you have an existing local repository you can specify your empty repo as a remote for it.

{% highlight sh %}
git remote add origin [user@]host.xz:path/to/repo.git/
{% endhighlight %}


{% highlight sh %}
git init
git status
git add .
git commit 
git pull origin
git push origin -u --all # Push everythng
git push -u origin master
{% endhighlight %}


## Gitflow Basics

This assumes git-flow git extension has been installed. On a Debian based system this can be 


{% highlight sh %}
git flow init -d  //With default branch names
{% endhighlight %}


{% highlight sh %}
git flow feature start MYFEATURE
git flow feature publish MYFEAT
git flow feature pull origin MYFEATURE
git flow feature finish MYFEATURE
{% endhighlight %}


{% highlight sh %}
git flow release start RELEASE [BASE]
git flow release publish RELEASE
git flow release finish RELEASE
git push origin --tags
{% endhighlight %}

{% highlight sh %}
git flow hotfix start VERSION [BASENAME]
git flow hotfix finish VERSION
{% endhighlight %}



To squeeze in a bit more practice I'm using glitflow branching model for my blog. Yeah, a bit of an overkill, but good for developing that muscle memory. 


