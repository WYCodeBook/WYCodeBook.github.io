---
layout: post
title: "Null, Undefined, and NaN"
date: "2018-08-15 21:44:11 -0700"
categories: Notes
tags: JavaScript
description: Definitions
---

### Null

`null` refers to the "value of nothing"

A variable can be explicitly set to a value of `null`.

### Undefined

`undefined` refers to the "absence of value". `undefined` is not even a value of nothing.

{% highlight js %}

var x;

console.log(x);

{% endhighlight %}

The above example will printed as `undefined` because the variable x exists, but it does not have a value. `undefined` will return to you when you didn't assign a value to something (which refers to as variable in this example)

### NaN

NaN stands for "Not-A-Number" and it's often returned indicating an error with number operations.

For instance, if you wrote some code that performed a math calculation, and the calculation failed to produce a valid number, NaN might be returned.

{% highlight js %}

// calculating the square root of a negative number will return NaN
Math.sqrt(-10)

// trying to divide a string by 5 will return NaN
"hello"/5

{% endhighlight %}
