---
layout: post
title: Benford's law
description: "A phenomenological law also called the first digit law..."
modified: 2013-12-27
tags: [python, benford]
comments: false
share: true
---
Have you heard about the [Benford's law](http://mathworld.wolfram.com/BenfordsLaw.html)? Apparently you can predict the first digit when number of statistical data is provided (any kind). 

> A phenomenological law also called the first digit law, first digit phenomenon, or leading digit phenomenon. Benford's law states that in listings, tables of statistics, etc., the digit 1 tends to occur with probability ~30%, much greater than the expected 11.1% (i.e., one digit out of 9).

This inspired me to check whether that is also applicable when using files' sizes as statistical data. I must admit that I'm pretty surprised by the results. Just have a look at the output:

{% highlight bash %}
Total samples: 23352
Start directory: /usr
Total time: 2.66 seconds
Digit	Result	Benford	Difference
1	0.3219	0.3010	-0.0209
2	0.1688	0.1761	+0.0073
3	0.1197	0.1249	+0.0052
4	0.0948	0.0969	+0.0021
5	0.0708	0.0792	+0.0084
6	0.0625	0.0669	+0.0045
7	0.0561	0.0580	+0.0019
8	0.0632	0.0512	-0.0121
9	0.0421	0.0458	+0.0036
{% endhighlight %}

You can try [benford.py script](https://gist.github.com/hmml/8151335) yourself, for example:

{% highlight bash %}
$ python benford.py /usr    
{% endhighlight %}
