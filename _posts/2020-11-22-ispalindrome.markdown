---
layout: post
title: "isPalindrome"
date: "2020-11-22 20:09:08 -0800"
tags: [Algorithms, JavaScript]
---

Given a string, write a function that returns true if the given string is palindrome, else false. For example, `race car` is palindrome, but `racecar` is not palindrome.

{% highlight javascript %}
function isPalindrome(string) {
  string = string.toLowerCase();
  var charactersArr = string.split('');
  var validCharacters = 'abcdefghijklmnopqrstuvwxyz'.split('');

  var lettersArr = [];
  charactersArr.forEach(char => {
    if (validCharacters.indexOf(char) > -1) lettersArr.push(char);
  });

  return lettersArr.join('') === lettersArr.reverse().join('');
}

isPalindrome("Madam, I'm Adam");
{% endhighlight %}
