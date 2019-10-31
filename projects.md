---
layout: page
title: Projects
permalink: /projects/
---

As well as being an active <a href="https://github.com/shioyama"
target="_blank">contributor</a> to well-known open-source projects, I am also
the author and maintainer of a number of libraries of my own.

### Mobility

[Mobility](https://github.com/shioyama/mobility) is a library for storing translations of a model in a Ruby
application, for example translations of posts in a blog. It provides a
seamless interface for storing such translations in the same way you would
store untranslated model data.

While there are other libraries in Ruby that do this, Mobility’s design is
unique in that it allows you to store your translations in whatever format you
want. This makes it very flexible and adaptable to many different usage
scenarios (hence the name).

Mobility is used in a growing number of companies with international customers.
For a deep dive into Mobility's design, see [my recent talk at RubyConf
2018](/speaking#building-generic-software).

### Wharel

[Wharel](https://github.com/shioyama/wharel) helps you write concise Arel
queries with ActiveRecord using Virtual Rows inspired by
[Sequel](http://sequel.jeremyevans.net/).

Although similar in spirit to other gems which provide block-based interfaces
for querying with Arel, Wharel is much much smaller. In fact, the core of the
gem is only 30 lines long! It uses a single BasicObject as a clean room to
evaluate the query block. That's really all there is to it.

For a more detailed explanation of the implementation, see this [blog
post](https://dejimata.com/2018/5/30/arel-with-wharel).

### Invisible

Say you want to override some methods from a gem so you can add some
instrumentation (measure performance or something). If you're not careful, you
may change the "visibility" of those methods: a method was originally private,
but your override makes it public. This is not ideal and can lead to subtle bugs.

[Invisible](https://github.com/shioyama/invisible) solves this problem. Simply
extend a module with `Invisible`, define your methods, and Invisible will take
care of ensuring that when you include (or prepend) the module somewhere, any
methods it overrides will keep their original visibility. Invisible does this
in just a dozen lines of code, [check it
out for yourself](https://github.com/shioyama/invisible/blob/master/lib/invisible.rb).
