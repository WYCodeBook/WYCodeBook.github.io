---

layout: collection
title: "Fizz Buzz"
picture:
description: How to run Fizz Buzz game using JavaScript?
---

Fizz buzz is a group word game for children to teach them about division. Players take turns to count incrementally, replacing any number divisible by three with the word "fizz", and any number divisible by five with the word "buzz".

💥 In computing, the modulo operation (%) finds the remainder after division of one number by another (sometimes called modulus). Given two positive numbers, a (the dividend) and n (the divisor), a modulo n (abbreviated as a mod n) is the remainder of the Euclidean division of a by n.

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

<p data-height="265" data-theme-id="0" data-slug-hash="odZyWd" data-default-tab="js,result" data-user="WYCodeBook" data-pen-title="Fizz Buzz -Modulus %" class="codepen">See the Pen <a href="https://codepen.io/WYCodeBook/pen/odZyWd/">Fizz Buzz -Modulus %</a> by WYCodeBook (<a href="https://codepen.io/WYCodeBook">@WYCodeBook</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
