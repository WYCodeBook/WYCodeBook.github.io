---
layout: post
title: "countTinyPairs"
date: "2019-08-18 00:56:03 -0700"
categories: Problems
---

##Problem:

Let say there are two arrays, `a` and `b`. We go through the `array a` from left to right and go through the `array b` from right to left... and concatenate each index of the array into `ab`. And we compare the 'ab' to a `constant k`, then total up the number of `ab` that's less than the `constant k`.

##Example:

a = [4,5,6,7,8]

b = [1,2,3,4,5]

k = 60

ab = [45, 54, 63, 72, 81]

There should be a total count of two `ab` from the concatenated arrays, because 45 and 54 is smaller than `k=60`.

##Solution:

{% highlight js %}

(function main() {
const a = [1, 2, 3];
const b = [5, 6, 7];
const k = 20;
let c = '';
let i = 0;
let j = b.length-1;
let count = 0;

while (i<a.length){
    c = String(a[i]) + String(b[j]);
    // console.log(c)
    if (Number(c) < k){
        count++;
    }
    i++;
    j--;
}
console.log(count);

}());

{% endhighlight %}
