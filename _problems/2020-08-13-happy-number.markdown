---
layout: post
title: "Happy Number"
date: "2020-08-13 03:52:43 -0700"
---

# Problem

[30-Day LeetCoding Challenge for April 2020](https://leetcode.com/explore/challenge/card/30-day-leetcoding-challenge/)

Write an algorithm to determine if a number `n` is "happy".

A happy number is a number defined by the following process: Starting with any positive integer, replace the number by the sum of the squares of its digits, and repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle which does not include 1. Those numbers for which this process ends in 1 are happy numbers.

Return True if `n` is a happy number, and False if not.

Example:

`Input: 19`

Output: true

Explanation:

1^2 + 9^2 = 82

8^2 + 2^2 = 68

6^2 + 8^2 = 100

1^2 + 0^2 + 0^2 = 1


# Solution

{% highlight js %}

/**
 * @param {number} n
 * @return {boolean}
 */
var isHappy = function(n) {

    let count = 0;

    while (n !== 1){
        if (count >= 1000){
            return false;
        } else {
            n = n.toString().split("");
            n = n.reduce((accumulator, number) => Number(accumulator) + Number(number * number), 0);
            count++;
            console.log(count);
        }
    }
    console.log(n);
    return true;

};

{% endhighlight %}
