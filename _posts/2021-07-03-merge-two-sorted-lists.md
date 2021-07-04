---
layout: post
title: "Merge Two Sorted Lists"
date: "2021-07-03 03:38:09 -0700"
tags: [Linked List, Recursion]
---

# Problem

Merge two sorted linked lists and return it as a sorted list. The list should be made by splicing together the nodes of the first two lists.

Example 1:

Input: l1 = [1,2,4], l2 = [1,3,4]
Output: [1,1,2,3,4,4]

Example 2:

Input: l1 = [], l2 = []

Output: []

Example 3:

Input: l1 = [], l2 = [0]
Output: [0]
 

Constraints:

- The number of nodes in both lists is in the range [0, 50].
- -100 <= Node.val <= 100
- Both l1 and l2 are sorted in non-decreasing order.

# Note

1. A `linked list` is a linear data structure similar to an array. `Not Array!!!` However, unlike arrays, elements are not stored in a particular memory location or index. Rather each element is a separate object that contains a pointer or a link to the next object in that list.

2. Each element (commonly called nodes) contains two items: the data stored and a link to the next node. The data can be any valid data type. You can see this illustrated in the diagram below.

3. The entry point to a linked list is called the `head`. The `head` is a reference to the `first node` in the linked list. The last node on the list points to `null`. If a list is empty, the `head` is a `null` reference.

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
 * @param {ListNode} l1
 * @param {ListNode} l2
 * @return {ListNode}
 */
var mergeTwoLists = function(l1, l2) {
    
    let l3 = new ListNode();
    let head = l3;
    
    
    while (l1 || l2){
        if (l1 && l2){
            if (l1.val <= l2.val){
                l3.next = new ListNode(l1.val);
                l1 = l1.next;
            } 
            else {
                l3.next = new ListNode(l2.val);
                l2 = l2.next;
            }
        } 
        else if (l1) {
            l3.next = new ListNode(l1.val);
            l1 = l1.next;
        }
        else {
            l3.next = new ListNode(l2.val);
            l2 = l2.next;
        }
        l3 = l3.next;
    }
    


    return head.next;
};
{% endhighlight %}