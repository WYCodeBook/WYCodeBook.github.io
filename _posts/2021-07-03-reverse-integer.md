---
layout: post
title: "Reverse Integer"
date: "2021-07-03 03:38:09 -0700"
tags: [Math]
---

# Problem

Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).


Example 1:

Input: x = 123

`Output: 321`

Example 2:

Input: x = -123

`Output: -321`

Example 3:

Input: x = 120

`Output: 21`

Example 4:

Input: x = 0

`Output: 0`

# Note 

1. check whether the x is positive or negative
2. if positive then turn into a string and reverse x, and return x at last
3. if negative then, take the absolute value, turn into a string and reverse x, and add the negative sign back to it at the last step when returning the x
4. check the 32-bit integer range, if within the range then return x, if out of range then return 0
5. if 0, return 0

# Solution

{% highlight JavaScript %}
/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {
    
    if (x > 0){
        x = x.toString().split("").reverse().join("");
        if (((-2)**31 < x) && (x < 2**31)) {
            return x;
        } else {
            return 0;
        }
    }
    
    if (x < 0){
        x = Math.abs(x);
        x = x.toString().split("").reverse().join("");
        if (((-2)**31 < x) && (x < 2**31)) {
            return -x;
        } else {
            return 0;
        }
    }
    
    return x;
    
};
{% endhighlight %}