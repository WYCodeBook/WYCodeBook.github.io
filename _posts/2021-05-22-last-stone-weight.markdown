---
layout: post
title: "Last Stone Weight"
date: "2021-05-22 03:38:09 -0700"
tags: [Array, Heap (Priority Queue)]
---

# Problem

We have a collection of stones, each stone has a positive integer weight.

Each turn, we choose the two heaviest stones and smash them together.  Suppose the stones have weights `x` and `y` with `x <= y`.  The result of this smash is:

If `x == y`, both stones are totally destroyed;

If `x != y`, the stone of weight `x` is totally destroyed, and the stone of weight `y` has new weight `y-x`.

At the end, there is at most 1 stone left.  Return the weight of this stone (or 0 if there are no stones left.)

Example:

Input: `[2,7,4,1,8,1]`

Output: 1

Explanation:

We combine 7 and 8 to get 1 so the array converts to [2,4,1,1,1] then,
we combine 2 and 4 to get 2 so the array converts to [2,1,1,1] then,
we combine 2 and 1 to get 1 so the array converts to [1,1,1] then,
we combine 1 and 1 to get 0 so the array converts to [1] then that's the value of last stone.

Note:

1 <= stones.length <= 30

1 <= stones[i] <= 1000

# Solution

{% highlight JavaScript %}
/**
 * @param {number[]} stones
 * @return {number}
 */
var lastStoneWeight = function(stones) {

    while(stones.length > 1){
        stones.sort(function(a, b){return b-a});
        console.log(stones);
        let i=0;


        if (stones[i] == stones[i+1]){
            stones.splice(0,2);
        }

        if (stones[i] > stones[i+1]){
            let num1 = stones.shift();
            let num2 = stones.shift();
            stones.push(num1 - num2);

        }

    }

    if(stones.length == 1){
        return stones;
    }

    if(stones.length == 0) {
        return 0;
    }

    console.log(stones);
};
{% endhighlight %}


# Note

[JavaScript Array sort() Method](https://www.w3schools.com/jsref/jsref_sort.asp)

[JavaScript Array push() Method](https://www.w3schools.com/jsref/jsref_push.asp)

[JavaScript Array shift() Method](https://www.w3schools.com/jsref/jsref_shift.asp)

[JavaScript Array splice() Method](https://www.w3schools.com/jsref/jsref_splice.asp)
