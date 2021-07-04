---
layout: post
title: "Group Anagrams"
date: "2020-08-30 19:44:16 -0700"
tags: [Hash Table, String, Sorting]
---

# Problem:

[30-Day LeetCoding Challenge for April 2020](https://leetcode.com/explore/challenge/card/30-day-leetcoding-challenge/)

Given an array of strings `strs`, group the anagrams together. You can return the answer in any order.

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

Example 1:

`Input: strs = ["eat","tea","tan","ate","nat","bat"]`

Output: [["bat"],["nat","tan"],["ate","eat","tea"]]

Example 2:

`Input: strs = [""]`

Output: [[""]]

Example 3:

`Input: strs = ["a"]`

Output: [["a"]]

Constraints:

1 <= strs.length <= 104

0 <= strs[i].length <= 100

strs[i] consists of lower-case English letters.

# Solution

{% highlight JavaScript %}
/**
 * @param {string[]} strs
 * @return {string[][]}
 */
var groupAnagrams = function(strs) {

    var compare = {};
    var finalAnagrams =[];

    for (let item of strs){
        let words = item.toLowerCase().split("").sort().join("");
        compare[words] = compare[words] || [];
        compare[words].push(item);
    }

    for (let eachItem in compare){
        finalAnagrams.push(compare[eachItem])
    }

    console.log(finalAnagrams);
    return finalAnagrams;  
};
{% endhighlight %}

# Notes

Step 1: There should be some array print out at the end. Set the final solution print out as `finalAnagrams`.

Step 2: The words in the listed array needed to re-organize in alphabetic order, so created variable `words` to sort and re-order each words.

Step 3: `compare[words] = compare[words] || []` is here to check/compare the current item in words to see if there is already the same one exist. If not, store the item into a new array.

Step 4: After the comparison, `compare[words].push(item)` is used to push the actual strings from the original array into the new `compare` object.

Step 5: It is time to go through each grouped array in the `compare` object using the For/In loop to and push all array objects into the `finalAnagrams`.
