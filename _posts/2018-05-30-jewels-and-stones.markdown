---
layout: post
title: "Jewels and Stones"
date: "2018-05-30 22:12:56 -0700"
categories: Problems
---

## Problem:

You're given strings J representing the types of stones that are jewels, and S representing the stones you have.  Each character in S is a type of stone you have.  You want to know how many of the stones you have are also jewels.

The letters in J are guaranteed distinct, and all characters in J and S are letters. Letters are case sensitive, so "a" is considered a different type of stone from "A".

[Leetcode - Jewels and Stones](https://leetcode.com/problems/jewels-and-stones/)

#### Example 1:

Input: J = "aA", S = "aAAbbbb"

Output: 3

#### Example 2:

Input: J = "z", S = "ZZ"

Output: 0

## Solution:

{% highlight js %}
/**
 * @param {string} J
 * @param {string} S
 * @return {number}
 **/
var numJewelsInStones = function(J, S) {
    var count = 0;
    for (var i=0; i<J.length; i++){
        for (var k=0; k<S.length; k++){
            if (J[i].includes(S[k])){
                count++
            }
        }
    }
    return count;
};
{% endhighlight %}
