---
layout: post
title: "Valid Perfect Square"
date: "2021-07-14 03:38:09 -0700"
tags: [Math, Binary Search]
---

# Problem

Given a positive integer num, write a function which returns True if num is a perfect square else False.

Follow up: Do not use any built-in library function such as sqrt.

 

Example 1:

Input: num = 16

Output: true

Example 2:

Input: num = 14

Output: false
 

Constraints:

- 1 <= num <= 2^31 - 1

# Solution

{% highlight JavaScript %}
/**
 * @param {number} num
 * @return {boolean}
 */
var isPerfectSquare = function(num) {
    return num ** (1/2) === Math.floor(num ** (1/2));
};
{% endhighlight %}