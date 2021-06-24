---
layout: post
title: "Reverse Words"
date: "2020-11-22 22:28:00 -0800"
tags: [JavaScript]
---

Every word should be reversed but the string as a whole should not be reverse.

Example:

`this is a string of words` should return as `siht si a gnirts fo sdrow`

{% highlight javascript %}
function reverseWords(string) {
  var wordsArr = string.split(' ');
  var reversedWordsArr = [];

  wordsArr.forEach(word => {
    var reversedWord = '';
    for (var i = word.length - 1; i >= 0; i--) {
      reversedWord += word[i];
    };
    reversedWordsArr.push(reversedWord);
  });

  return reversedWordsArr.join(' ');
}

reverseWords('Coding JavaScript'); // this should return gnidoC tpircSavaJ
{% endhighlight %}
