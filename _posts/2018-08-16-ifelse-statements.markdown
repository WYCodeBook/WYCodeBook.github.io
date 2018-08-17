---
layout: post
title: "If...Else Statements"
date: "2018-08-16 20:26:13 -0700"
categories: JavaScript
description: If...Else and Else If
---

## If...else statements

`If...else` statements allow you to execute certain pieces of code based on a condition, or set of conditions, being met.

{% highlight js %}
  if (/* this expression is true */) {
    // run this code
  } else {
    // run this code
  }
{% endhighlight %}

This is extremely helpful because it allows you to choose which piece of code you want to run based on the result of an expression. For example,

{% highlight js %}
  var a = 1;
  var b = 2;

  if (a > b) {
    console.log("a is greater than b");
  } else {
    console.log("a is less than or equal to b");
  }
{% endhighlight %}


Console will print: "a is less than or equal to b"

A couple of important things to notice about `if...else statements`.

The value inside the `if` statement is always converted to true or false. Depending on the value, the code inside the `if` statement is run or the code inside the `else` statement is run, but not both. The code inside the `if` and `else` statements are surrounded by curly braces `{...}` to separate the conditions and indicate which code should be run.

💥 When coding, sometimes you may only want to use an `if` statement. However, if you try to use only an `else` statement, then you will receive the error `SyntaxError: Unexpected token else`. You’ll see this error because `else` statements need an `if` statement in order to work. You can’t have an `else` statement without first having an `if` statement.

## Else If Statements
