---
layout:     post
title:      Migrating your Jekyll site to Vercel / Netlify
subtitle:   
date:       2017-05-11
author:     Brian Douglas
header-img: img/post-bg-debug.png
catalog: true
tags:    
        - 笔记
---

#### This guide was most recently updated on July 24th, 2018. Below are the package versions used:
* Ruby 2.4.3
* github-pages 73

Screenshots may be outdated.

***

This post will cover how to move your Jekyll site from GitHub Pages to Netlify in just a few steps.

If you have generated your Jekyll site using GitHub pages or forked a template there is a good chance you do not have a Gemfile. This is because GitHub pages will infer dependencies for you. If you would like to build your project outside of GitHub a Gemfile is needed and simple to create.

In your GitHub repo create a new file with the name Gemfile and add the following content to it:

```
source "https://rubygems.org"
gem 'github-pages'
```

The github-pages gem includes Jekyll, along with other dependencies and plugins you had available to your site on GitHub Pages.

Since Netlify also needs to know what version of Ruby to run, put your version string in a file called `/.ruby-version` and we’ll use that version! If you don’t know, use version `2.4.3`.

Once you have a Gemfile and a .ruby-version file, you can now connect your site to Netlify without issue.

Adding a new site with Git is not a requirement for adding a site, but it’s strongly recommend to take advantage of all of Netlify’s continuous deployment features.

![](/img/2017-05-11-migratingjekyllsite/01.png)

Once your site is connected, you can find your Repository from the list GitHub repos. There is also a convenient search box in case you have more repositories than the page can fit.

![](/img/2017-05-11-migratingjekyllsite/02.png)

Finally, you will just need to add the Jekyll build command and build location. For Jekyll that is `jekyll build` for the command and `_site` for the location.

![](/img/2017-05-11-migratingjekyllsite/03.png)

You now have your Jekyll site on Netlify and can take advantage of some great features, like deploy previews and free custom domains with SSL.

This article has a good list of things to configure after you deploy your site.

If you made it this far and do not have a Jekyll site to try this out with, you can try out my Jekyll template.
