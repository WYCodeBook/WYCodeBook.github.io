---
layout: post
title: "Maximum Subarray"
date: "2020-08-17 17:25:34 -0700"
tags: [Array, Divide and Conquer, Dynamic Programming]
---

# Problem:

[30-Day LeetCoding Challenge for April 2020](https://leetcode.com/explore/challenge/card/30-day-leetcoding-challenge/)

Given an integer array `nums`, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

Example:

`Input: [-2,1,-3,4,-1,2,1,-5,4]`

Output: 6

Explanation: [4,-1,2,1] has the largest sum = 6.

# Solution:

{% highlight js %}

/**
 * @param {number[]} nums
 * @return {number}
 */
var maxSubArray = function(nums) {

    let max = nums[0];
    let sum = nums[0];

    for (i=1; i <= nums.length; i++){
        if (nums.length === 1){
            return nums[0];
        }

        sum = sum + nums[i];

        if (sum < nums[i]){
            sum = nums[i];
        }

        if (sum > max){
            max = sum;
        }
    }
    return max;
};

{% endhighlight %}
