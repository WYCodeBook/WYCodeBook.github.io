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

## Logical AND and OR

Before you advance any further in the lesson, here’s the truth tables for logical `AND` (` && `) and logical `OR` (` || `).

![Truth Table](/pic/andor.PNG)

Truth tables are used to represent the result of all the possible combinations of inputs in a logical expression. `A` represents the boolean value on the left-side of the expression and `B` represents the boolean value on the right-side of the expression.

Truth tables can be helpful for visualizing the different outcomes from a logical expression. However, do you notice anything peculiar about the truth tables for logical AND and OR?

#### Short-circuiting

![Short Circuiting](/pic/shortcircuiting.PNG)

In both tables, there are specific scenarios where regardless of the value of `B`, the value of `A` is enough to satisfy the condition.

For example, if you look at `A AND B`, if `A` is false, then regardless of the value `B`, the total expression will always evaluate to `false` because both `A` and `B` must be `true` in order for the entire expression to be `true`.

This behavior is called `short-circuiting` because it describes the event when later arguments in a logical expression are not considered because the first argument already satisfies the condition.

## Truthy and Falsy

Every value in JavaScript has an inherent boolean value. When that value is evaluated in the context of a boolean expression, the value will be transformed into that inherent boolean value.

#### Falsy values

A value is `falsy `if it converts to `false` when evaluated in a boolean context. For example, an empty String `""` is falsy because, `""` evaluates to `false`. You already know if...else statements, so let's use them to test the truthy-ness of `""`.

{% highlight js %}
if ("") {
    console.log("the value is truthy");
} else {
    console.log("the value is falsy");
}
{% endhighlight %}

Console will print: "the value is falsy"

Here’s the list of all of the falsy values:

  - the Boolean value false

  - the null type

  - the undefined type

  - the number 0

  - the empty string ""

  - the odd value NaN (stands for "not a number", check out the NaN MDN article)

That's right, there are only six falsy values in all of JavaScript!

#### Truthy values

A value is `truthy` if it converts to `true` when evaluated in a boolean context. For example, the number `1` is truthy because, `1` evaluates to `true`. Let's use an if...else statement again to test this out:

{% highlight js %}

if (1) {
    console.log("the value is truthy");
} else {
    console.log("the value is falsy");
}

{% endhighlight %}

Console will print: "the value is truthy"

Here are some other examples of truthy values:

{% highlight js %}
true
42
"pizza"
"0"
"null"
"undefined"
{}
[]
{% endhighlight %}
