---
layout: post
title: Benford's law
description: "A phenomenological law also called the first digit law..."
modified: 2013-12-26
tags: [python benford]
comments: false
share: true
---
Have you heard about the [Benford's law](http://mathworld.wolfram.com/BenfordsLaw.html)? Apparently you can predict the first digit when number of statistical data is provided (any kind). 

> A phenomenological law also called the first digit law, first digit phenomenon, or leading digit phenomenon. Benford's law states that in listings, tables of statistics, etc., the digit 1 tends to occur with probability ~30%, much greater than the expected 11.1% (i.e., one digit out of 9).

This inspired me to check whether that is also applicable when using file sizes as statistical data. I must admit that I'm pretty surprised by the results. Just have a look at the data:

{% highlight bash %}
Total samples: 253338
Start directory: c:/
Total time: 179.18 seconds
Digit   Result  Benford Difference
1       0.2942  0.3010  +0.0068
2       0.1746  0.1761  +0.0015
3       0.1266  0.1249  -0.0017
4       0.0918  0.0969  +0.0051
5       0.0790  0.0792  +0.0002
6       0.0798  0.0669  -0.0129
7       0.0595  0.0580  -0.0015
8       0.0503  0.0512  +0.0008
9       0.0440  0.0458  +0.0017
{% endhighlight %}

You can try [benford.py script](https://gist.github.com/hmml/8151335) yourself, for example:

{% highlight bash %}
$ python benford.py /    
{% endhighlight %}
