---
layout: post
title: "Create a new and empty branch in git"
date: 2012-07-14 13:18
comments: true
categories: [git]
---

* Create new empty branch:

``` bash
$ git checkout --orphan <branch>
```

* Delete all files in the working directory:

``` bash
$ git rm -rf .
```
