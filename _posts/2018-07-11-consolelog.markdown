---
layout: post
title: "Console.log"
date: "2018-07-11 23:52:17 -0700"
categories: JavaScript
description: What do console.log do?
---


`console.log` is used to display content to the JavaScript console.

## Examples to try...

{% highlight js %}
  console.log("Hello World!");
{% endhighlight %}

Console will print: hiya friend!

The message you’ve logged is "Hello World!". `Hello World!` is a string (a sequence of characters).

{% highlight js %}
  for (var i = 0; i < 10; i++) {
    console.log(i);
  }
{% endhighlight %}

### Console Prints...
0
1
2
3
4
5
6
7
8
9

This is a loop function.

Based on this loop's settings, any code written inside the curly brackets `{...}` will be repeated 10 times. In this case, `console.log` is printing out the value of `i` each time the loop runs.
