---
layout: post
title: "Remove Linked List Elements"
date: "2021-07-04 03:38:09 -0700"
tags: [Linked List, Recursion]
---

# Problem

Given the `head` of a linked list and an integer `val`, remove all the nodes of the linked list that has `Node.val == val`, and return the new head.

Example 1:


Input: head = [1,2,6,3,4,5,6], val = 6

`Output: [1,2,3,4,5]`

Example 2:

Input: head = [], val = 1

`Output: []`

Example 3:

Input: head = [7,7,7,7], val = 7

`Output: []`
 

Constraints:

- The number of nodes in the list is in the range [0, 104].
- 1 <= Node.val <= 50
- 0 <= val <= 50

# Solution

{% highlight JavaScript %}
/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} head
 * @param {number} val
 * @return {ListNode}
 */
var removeElements = function(head, val) {
    
    let l2 = new ListNode();
    let newList = l2;
    
    while (head){
        if (head.val !== val){
            newList.next = new ListNode(head.val);
            newList = newList.next;
        }
        head = head.next;
    }
    
    return l2.next;
};
{% endhighlight %}