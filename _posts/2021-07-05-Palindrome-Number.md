---
layout: post
title: "Palindrome Number"
date: "2021-07-05 03:38:09 -0700"
tags: [Math]
---

# Problem

Given an integer x, return true if x is palindrome integer.

An integer is a palindrome when it reads the same backward as forward. For example, `121` is palindrome while `123` is not.

Example 1:

Input: x = 121

`Output: true`

Example 2:

Input: x = -121

`Output: false`

Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.

Example 3:

Input: x = 10

`Output: false`

Explanation: Reads 01 from right to left. Therefore it is not a palindrome.

Example 4:

Input: x = -101

`Output: false`
 

Constraints:

- -231 <= x <= 231 - 1

# Note

In JavaScript, a truthy value is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN).

# Solution

{% highlight JavaScript %}
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function(x) {
    
    var firstNum = x.toString();
    var secondNum = x.toString().split("").reverse().join("");
    
    if (firstNum !== secondNum){
        return false;
    } else {
        return true;
    }

};

{% endhighlight %}