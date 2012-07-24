Bundler.require(:default)
---
layout: post
title: "Track upstream branch in git"
date: 2012-07-14 12:43
comments: true
categories: [git]
---


* Show upstream remotes:

``` bash 

$ git remote show octopress
* remote octopress
  Fetch URL: git://github.com/imathis/octopress.git
  Push  URL: git://github.com/imathis/octopress.git
  HEAD branch: master
  Remote branches:
    2.1                 tracked
    gh-pages            tracked
    linklog             tracked
    master              tracked
    refactor_with_tests tracked
    rubygemcli          tracked
    site                tracked
```

* Create local branch tracking upstream:

``` bash 
$ git checkout -t -b rubygemcli octopress/rubygemcli
Branch rubygemcli set up to track remote branch rubygemcli from octopress.
Switched to a new branch 'rubygemcli'
```
