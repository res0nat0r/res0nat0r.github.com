---
layout: post
title: "Add authentication to Gollum"
date: 2012-07-23 21:43
comments: true
categories: [git, gollum]
---

* Create a Rack `config.ru` like below:

```ruby
require 'rubygems'

require 'gollum/frontend/app'

use Rack::Auth::Basic, "Restricted Area" do |username, password|
   [username, password] == ['admin', 'admin']
end

Precious::App.set(:gollum_path, '<repo-path>')
Precious::App.set(:wiki_options, {})
run Precious::App
```
