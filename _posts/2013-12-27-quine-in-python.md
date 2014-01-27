---
layout: post
title: Quines in python
description: "Quines in python, how to create one?"
modified: 2013-12-27
tags: [python, quine]
comments: false
share: true
image:
  feature: unsplash_522af9ac823b4_1.jpg
---

According to [wikipedia](http://en.wikipedia.org/wiki/Quine_(computing)):

> In computing, a quine is a computer program which produces a copy of its own source code as its only output.
...
Quines are named after philosopher Willard Van Orman Quine (1908–2000), who made an extensive study of indirect self-reference. He coined, among others, the following paradox-producing expression, known as Quine's paradox.
"Yields falsehood when preceded by its quotation" yields falsehood when preceded by its quotation.


Coming up with simple quine in python is not hard...

{% highlight bash %}
s="s=%s;print s%%`s`";print s%`s`
{% endhighlight %}

There is also alternative approach. The output is program's source code, this is not really allowed but loading its source code works like a charm...

{% highlight bash %}
import sys; print "".join(open(sys.argv[0]).readlines())
{% endhighlight %}

For some more self-reproducing programs have a look at: [self_pyth.txt](http://www.nyx.net/~gthompso/self_pyth.txt).