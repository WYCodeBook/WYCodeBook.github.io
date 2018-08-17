---
layout: post
title: "Conditionals"
date: "2018-08-16 20:26:13 -0700"
categories: JavaScript
description: If...Else | Else If | Logical Operators |
---

## If...else statements

`If...else` statements allow you to execute certain pieces of code based on a condition, or set of conditions, being met.

{% highlight js %}
  if (// this expression is true //) {
    // run this code
  } else {
    //run this code
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

In some situations, two conditionals aren’t enough. Consider the following situation.

You're trying to decide what to wear tomorrow. If it is going to snow, then you’ll want to wear a coat. If it's not going to snow and it's going to rain, then you’ll want to wear a jacket. And if it's not going to snow or rain, then you’ll just wear what you have on.

In JavaScript, you can represent this secondary check by using an extra if statement called an `else if` statement.

{% highlight js %}

  var weather = "sunny";

  if (weather === "snow") {
    console.log("Bring a coat.");
  } else if (weather === "rain") {
    console.log("Bring a rain jacket.");
  } else {
    console.log("Wear what you have on.");
  }

{% endhighlight %}

Console will prints: Wear what you have on.

By adding the extra `else if` statement, you're adding an extra conditional statement.

If it’s not going to snow, then the code will jump to the `else if` statement to see if it’s going to rain. If it’s not going to rain, then the code will jump to the `else` statement.

The `else` statement essentially acts as the "default" condition in case all the other if statements are false.

## Logical Operators

Let's say Julia is planning to meet with Colt over the weekend to do something... Here’s the logical expression used to represent Julia’s weekend plans:

{% highlight js %}

  var colt = "not busy";
  var weather = "nice";

  if (colt === "not busy" && weather === "nice") {
    console.log("go to the park");
  }

{% endhighlight %}

Console will print: "go to the park"

Notice the && in the code above.

The `&&` symbol is the logical `AND` operator, and it is used to combine two logical expressions into one larger logical expression. If `both` smaller expressions are true, then the entire expression evaluates to true. If `either one` of the smaller expressions is false, then the whole logical expression is false.

Another way to think about it is when the `&&` operator is placed between the two statements, the code literally reads, "if Colt is not busy AND the weather is nice, then go to the park".

#### Logical expressions

Logical expressions are similar to mathematical expressions, except logical expressions evaluate to either `true` or `false`.

Entering `11 != 12`

Console will print: true

You’ve already seen logical expressions when you write comparisons. A comparison is just a simple logical expression.

Similar to mathematical expressions that use `+`, `-`, `*`, `/` and `%`, there are logical operators `&&`, `||` and `!` that you can use to create more complex logical expressions.

#### Logical operators

Logical operators can be used in conjunction with boolean values (`true` and `false`) to create complex logical expressions.

By combining two boolean values together with a logical operator, you create a logical expression that returns another boolean value. Here’s a table describing the different logical operators:

![Operators](/pic/operators.PNG)

By using logical operators, you can create more complex conditionals like Julia’s weekend example.

💥 Logical expressions are evaluated from left to right. Similar to mathematical expressions, logical expressions can also use parentheses to signify parts of the expression that should be evaluated first.
