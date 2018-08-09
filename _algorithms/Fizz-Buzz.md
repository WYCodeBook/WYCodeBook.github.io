---

layout: collection
title: "Fizz Buzz"
picture:
description: How to run Fizz Buzz game using JavaScript?
---

Fizz buzz is a group word game for children to teach them about division. Players take turns to count incrementally, replacing any number divisible by three with the word "fizz", and any number divisible by five with the word "buzz".

💥 In computing, the modulo operation (%) finds the remainder after division of one number by another (sometimes called modulus). Given two positive numbers, a (the dividend) and n (the divisor), a modulo n (abbreviated as a mod n) is the remainder of the Euclidean division of a by n.

### Examples to try...

Within this example, the console will go through each numbers from 1 to 30, and replacing any number divisible by three with the word "fizz", and any number divisible by five with the word "buzz".

{% highlight javascript %}
function fizzBuzz(num){
  for (var i=1; i <= num; i++){
    if (i % 15 === 0) console.log('FizzBuzz');
    else if (i % 3 === 0) console.log('Fizz');
    else if (i % 5 === 0) console.log('Buzz');
    else console.log(i);
  }
}

fizzBuzz(30);
{% endhighlight %}

### Console Prints...

1
2
"Fizz"
4
"Buzz"
"Fizz"
7
8
"Fizz"
"Buzz"
11
"Fizz"
13
14
"FizzBuzz"
16
17
"Fizz"
19
"Buzz"
"Fizz"
22
23
"Fizz"
"Buzz"
26
"Fizz"
28
29
"FizzBuzz"
