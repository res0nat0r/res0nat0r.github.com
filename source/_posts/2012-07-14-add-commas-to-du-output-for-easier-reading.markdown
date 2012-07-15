---
layout: post
title: "Add commas to du output"
date: 2012-07-14 17:48
comments: true
categories: [awk]
---

#### Note this requires [GAWK](http://www.gnu.org/software/gawk/)

* Create _commas.awk_:

``` bash
{printf "%d %s\n", $1, $2}
```

* Pipe _du_ output through _commas.awk_:

``` bash
$ du -sk | gawk -f commas.awk
38,522,624 .
```
