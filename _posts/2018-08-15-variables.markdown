---
layout: post
title: "Variables"
date: "2018-08-15 20:28:33 -0700"
categories: Notes
tags: JavaScript
description: Different Variables in JavaScript
---

With variables, you no longer need to work with one-time-use data.

At the beginning of this course, you declared the value of a string, but you didn't have a way to access or reuse the string later.

#### Creating a variable...

{% highlight js %}

var variableName = value;

{% endhighlight %}

#### Using variable...

{% highlight js %}

"Hello"; // Here's a String "Hello"

"Hello" + " World"; // Here's a new String (also with the value "Hello") concatenated with " World"

{% endhighlight %}

Storing the value of a string in a variable is like packing it away for later use.

{% highlight js %}

var greeting = "Hello";

{% endhighlight %}

Now, if you want to use "Hello" in a variety of sentences, you don't need to duplicate "Hello" strings. You can just reuse the `greeting` variable.

Entering `greeting + " World!";`

Console will print: Hello World!

Entering `greeting + " Mike!";`

Console will print: Hello Mike!

You can also change the start of the greeting by reassigning a new string value to the variable `greeting`.

{% highlight js %}

greeting = "Hola";

{% endhighlight %}

Entering `greeting + " World!";`

Console will print: Hola World!

Entering `greeting + " Mike!";`

Console will print: Hola Mike!

## Naming conventions

When you create a variable, you write the name of the variable using `camelCase` (the first word is lowercase, and all following words are uppercase). Also try to use a variable name that accurately, but succinctly describes what the data is about.

{% highlight js %}

var totalAfterTax = 53.03; // uses camelCase if the variable name is multiple words

var tip = 8; // uses lowercase if the variable name is one word

{% endhighlight %}

Not using `camelCase` for your variables names is not going to necessarily break anything in JavaScript. But there are recommended style guides used in all programming languages that help keep code consistent, clean, and easy-to-read. This is especially important when working on larger projects that will be accessed by multiple developers.

#### 👓 Read more at:

  - [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
