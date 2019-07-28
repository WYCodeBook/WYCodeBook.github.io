---
layout: post
title: "Length of Last Word"
date: "2019-06-27 22:49:48 -0700"
categories: Problems
---

## Problem:

Given a string s consists of upper/lower-case alphabets and empty space characters ' ', return the length of last word in the string.

If the last word does not exist, return 0.

Note: A word is defined as a character sequence consists of non-space characters only.

#### Example:

Input: "Hello World"

Output: 5

## Solution:

{% highlight js %}
/**
 * @param {string} s
 * @return {number}
 */


var lengthOfLastWord = function(s) {
    var stringsplit = s.trim().split(" ");
    var lastword = stringsplit[stringsplit.length-1];

    return lastword.length;
};
{% endhighlight %}
