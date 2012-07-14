---
layout: post
title: "Show git branch via your bash prompt"
date: 2012-07-14 13:10
comments: true
categories: [bash, git]
---

* Create the Bash function below to determine what branch you are using:

``` bash
function parse_git_branch {
  ref=$(git symbolic-ref HEAD 2> /dev/null) || return
  echo "("${ref#refs/heads/}")"
}
```

* Update your PS1:

``` bash
export PS1="\[\033[01;36m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\\[\033[01;31m\] \$(parse_git_branch)\[\033[00m\]\n\[\033[01;34m\]\$\[\033[00m\] "
```
