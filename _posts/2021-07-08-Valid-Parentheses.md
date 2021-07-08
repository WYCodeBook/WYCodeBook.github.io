---
layout: post
title: "Valid Parentheses"
date: "2021-07-08 03:38:09 -0700"
tags: [String, Stack]
---

# Problem 


Given a string s containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['` and `']'`, determine if the input string is valid.

An input string is valid if:

- Open brackets must be closed by the same type of brackets.
- Open brackets must be closed in the correct order.

Example 1:

`Input: s = "()"`

Output: true

Example 2:

`Input: s = "()[]{}"`

Output: true

Example 3:

`Input: s = "(]"`

Output: false

Example 4:

`Input: s = "([)]"`

Output: false

Example 5:

`Input: s = "{[]}"`

Output: true
 

Constraints:

- 1 <= s.length <= 104
- s consists of parentheses only '()[]{}'.

# Note

Stack: first in last out

[Implementing Javascript Stack Using an Array](https://www.javascripttutorial.net/javascript-stack/)

# Solution

{% highlight JavaScript %}
/**
 * @param {string} s
 * @return {boolean}
 */
var isValid = function(s) {
    
    const brackets = {
        "(" : ")",
        "{" : "}",
        "[" : "]"
    };
    
    var stack = [];
    
    for (i=0; i<s.length; i++){
        if (s[i] in brackets){
            stack.push(brackets[s[i]]);
        } else {
            if (s[i] !== stack.pop()){
                return false;
            }
        }    
    }
    
    return stack.length === 0;
};
{% endhighlight %}