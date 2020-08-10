---
layout: post
title: "Single Number"
date: "2020-08-10 00:52:02 -0700"
---
# Problem:

[30-Day LeetCoding Challenge for April 2020](https://leetcode.com/explore/challenge/card/30-day-leetcoding-challenge/)

Given a non-empty array of integers, every element appears twice except for one. Find that single one.

Note:

Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

Example 1:

`Input: [2,2,1]`
Output: 1

Example 2:

`Input: [4,1,2,1,2]`
Output: 4


# Solution:

1. rearranged the order of the array
2. then using 'for-loop' to go through each pair of the numbers in the array
3. if 'not-match' is found, then return the number in that array position

{% highlight js %}
/**
 * @param {number[]} nums
 * @return {number}
**/


var singleNumber = function(nums) {
    let number = nums.sort((a,b)=>a-b);

    for (x=0; x<=number.length; x+=2){
        if (number[x] != number[x+1]){
            return number[x];
        }
    }
};

{% endhighlight %}
