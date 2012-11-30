---
layout: post
title: "Convert all S3 objects to RRD"
date: 2012-11-29 22:26
comments: true
categories: [aws, s3]
---

```python
#!/usr/bin/env python

import boto

s3 = boto.connect_s3()
b  = boto.lookup('bucket')

[x.change_storage_class('REDUCED_REDUNDANCY') for x in b.list() if x.storage_class == 'STANDARD']
```
