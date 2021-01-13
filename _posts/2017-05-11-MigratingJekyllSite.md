---
layout:     post
title:      Migrating your Jekyll site to Vercel / Netlify
subtitle:   
date:       2017-05-11
author:     Brian Douglas
header-img: img/post-bg-miui6.jpg
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
