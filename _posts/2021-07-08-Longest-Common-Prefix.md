---
layout: post
title: "Longest Common Prefix"
date: "2021-07-08 03:38:09 -0700"
tags: [String]
---

# Problem

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string "".

Example 1:

Input: strs = ["flower","flow","flight"]

Output: "fl"

Example 2:

Input: strs = ["dog","racecar","car"]

Output: ""

Explanation: There is no common prefix among the input strings.
 

Constraints:

- 1 <= strs.length <= 200
- 0 <= strs[i].length <= 200
- strs[i] consists of only lower-case English letters.

# Solution 1

{% highlight JavaScript %}
/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function(strs) {
    
    var common = "";
    var short = "";
    
    for (i=0; i<strs.length; i++){
        if (short.length <= strs[i].length){
            short += strs[i];
        }
    };
    
    console.log(short);
    
    var shortLength = short.length;
    
    console.log(shortLength);
    
    if (strs.length <= 1){
        return strs.toString();
    }
    
    for (i=0; i<shortLength; i++){
        
        for (j=0; j<strs.length; j++){
        
            if (strs[j][i] !== short[i]){
                console.log("common= " + common);
                return common;
                }
        }
        
        common += short[i];
    }
    
    
    console.log(common);
    return common;
};
{% endhighlight %}

# Solution 2

{% highlight JavaScript %}

/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function(strs) {
    
    var common = "";
    var shortest = strs[0];
    
    for (i=0; i<strs.length; i++){
        if (strs[i].length < shortest.length){
            shortest = strs[i];
        }
    };
    
    console.log(shortest);
    
    var shortestLength = shortest.length;
    
    console.log(shortestLength);
    
    if (strs.length <= 1){
        return strs.toString();
    }
    
    for (i=0; i<shortestLength; i++){
        
        for (j=0; j<strs.length; j++){
        
            if (strs[j][i] !== shortest[i]){
                console.log("common= " + common);
                return common;
                }
        }
        
        common += shortest[i];
    }
    
    
    console.log(common);
    return common;
};
{% endhighlight %}