---
layout: post
title: "Functions"
date: "2018-08-23 20:36:04 -0700"
categories: JavaScript
description: How to use functions?
---

🔍 [Declaring Functions](#declaring-function) 🔍 [Function with Loop Example](#function-with-loop-example) 🔍 [Return Values](#return-values) 🔍 [Using Return Values](#using-return-values) 🔍 [Scopes](#scopes) 🔍 [Global Variables](#global-variables) 🔍 [Hoisting](#hoisting) 🔍 [Function Expressions](#function-expression) 🔍 [Patterns with Function Expressions](#patterns-with-function-expressions) 

---

## Declaring Functions

#### How to declare a function

`Functions` allow you to package up lines of code that you can use (and often reuse) in your programs.

Sometimes they take `parameters` like the pizza button from the beginning of this lesson. `reheatPizza()` had one `parameter:` the number of slices.

{% highlight js %}
function reheatPizza(numSlices) {
  // code that figures out reheat settings!
}
{% endhighlight %}

The `reverseString()` function that you saw also had one parameter: the string to be reversed.

{% highlight js %}
function reverseString(reverseMe) {
  // code to reverse a string!
}
{% endhighlight %}

In both cases, the parameter is listed as a variable after the function name, inside the parentheses. And, if there were multiple parameters, you would just separate them with commas.

{% highlight js %}
function doubleGreeting(name, otherName) {
  // code to greet two people!
}
{% endhighlight %}

But, you can also have functions that don't have any parameters. Instead, they just package up some code and perform some task. In this case, you would just leave the parentheses empty. Take this one for example. Here's a simple function that just prints out `"Hello!"`.

{% highlight js %}
// accepts no parameters! parentheses are empty
function sayHello() {
  var message = "Hello!"
  console.log(message);
}
{% endhighlight %}

If you tried pasting any of the functions above into the JavaScript console, you probably didn't notice much happen. In fact, you probably saw `undefined` returned back to you. `undefined` is the default return value on the console when nothing is explicitly returned using the special `return` keyword.

#### Return statements

In the `sayHello()` function above, a value is printed to the console with `console.log`, but not explicitly returned with a return statement. You can write a return statement by using the return keyword followed by the expression or value that you want to return.

{% highlight js %}
// declares the sayHello function
function sayHello() {
  var message = "Hello!"
  return message; // returns value instead of printing it
}
{% endhighlight %}

#### How to run a function

Now, to get your function to do something, you have to invoke or call the function using the function name, followed by parentheses with any arguments that are passed into it. Functions are like machines. You can build the machine, but it won't do anything unless you also turn it on. Here's how you would call the `sayHello()` function from before, and then use the return value to print to the console:

{% highlight js %}
// declares the sayHello function
function sayHello() {
  var message = "Hello!"
  return message; // returns value instead of printing it
}
// function returns "Hello!" and console.log prints the return value
console.log(sayHello());
{% endhighlight %}

Console will print: `"Hello!"`

#### Parameters vs. Arguments

At first, it can be a bit tricky to know when something is either a parameter or an argument. The key difference is in where they show up in the code. A `parameter` is always going to be a variable name and appears in the function declaration. On the other hand, an `argument` is always going to be a value (i.e. any of the JavaScript data types - a number, a string, a boolean, etc.) and will always appear in the code when the function is called or invoked.

## In a summary

`Functions` package up code so you can easily use (and reuse) a block of code.

`Parameters` are variables that are used to store the data that's passed into a function for the function to use.

`Arguments` are the actual data that's passed into a function when it is invoked:

{% highlight js %}
// x and y are parameters in this function declaration
function add(x, y) {
  // function body
  var sum = x + y;
  return sum; // return statement
}

// 1 and 2 are passed into the function as arguments
var sum = add(1, 2);
{% endhighlight %}

The `function body` is enclosed inside curly brackets:

{% highlight js %}
function add(x, y) {
  // function body!
}
{% endhighlight %}

`Return statements` explicitly make your function return a value:

{% highlight js %}
return sum;
{% endhighlight %}

You `invoke` or `call` a function to have it do something:

{% highlight js %}
add(1, 2);
{% endhighlight %}

Console will print: `3`

## Function with Loop Example

#### Directions:

Write a function called `laugh()` that takes one parameter, `num` that represents the number of `"ha"s` to return.

{% highlight js %}
function laugh(num) {
  var laugh = "";
  for (var x = 0; x < num; x++) {
    laugh += "ha";
  }
  return laugh + "!";
}

console.log(laugh(3));
{% endhighlight %}

Console will print: `hahaha!`

## Return Values

#### Console.log

Use to `print` a value to the JavaScript console.

#### Return

Use to stop execution of a function and return a value back to the caller.

💥 It’s important to understand that return and print are not the same thing. Printing a value to the JavaScript console only displays a value (that you can view for debugging purposes), but the value it displays can't really be used for anything more than that. For this reason, you should remember to only use `console.log` to test your code in the JavaScript console.

Paste the following function declaration and function invocation into the JavaScript console to see the difference between logging (printing) and returning:

{% highlight js %}
function isThisWorking(input) {
  console.log("Printing: isThisWorking was called and " + input + " was passed in as an argument.");
  return "Returning: I am returning this string!";
}

isThisWorking(3);
{% endhighlight %}

Prints: `"Printing: isThisWorking was called and 3 was passed in as an argument"`

Returns: `"Returning: I am returning this string!"`

💥 If you don't explicitly define a return value, the function will return undefined by default.

{% highlight js %}
function isThisWorking(input) {
  console.log("Printing: isThisWorking was called and " + input + " was passed in as an argument.");
}

isThisWorking(3);
{% endhighlight %}

Prints: `"Printing: isThisWorking was called and 3 was passed in as an argument"`

Returns: `undefined`

#### Undefined

A function is always going to return some value back to the caller. If a return value is not specified, then the function will just return back `undefined`.

## Using Return Values

Returning a value from a function is great, but what's the use of a return value if you're not going to use the value to do something?

A function's return value can be stored in a variable or reused throughout your program as a function argument. Here, we have a function that adds two numbers together, and another function that divides a number by 2. We can find the average of 5 and 7 by using the `add()` function to add a pair of numbers together, and then by passing the sum of the two numbers `add(5, 7)` into the function `divideByTwo()` as an argument.

And finally, we can even store the final answer in a variable called `average` and use the variable to perform even more calculations in more places!

{% highlight js %}
// returns the sum of two numbers
function add(x, y) {
  return x + y;
}


// returns the value of a number divided by 2
function divideByTwo(num) {
  return num / 2;
}


var sum = add(5, 7); // call the "add" function and store the returned value in the "sum" variable
var average = divideByTwo(sum); // call the "divideByTwo" function and store the returned value in the "average" variable
{% endhighlight %}

## Scopes

#### Global Scopes

identifiers can be accessed everywhere within your program

#### Function Scopes

identifiers can be accessed everywhere inside the function it was defined in

💥 The JavaScript language is constantly improving. One of these updates introduces a new type of scope, called Block scope. Check out our [ES6 course](https://www.udacity.com/course/es6-javascript-improved--ud356) to learn more!

#### Scope Recap

  - If an identifier is declared in global scope, it's available everywhere.

  - If an identifier is declared in function scope, it's available in the function it was declared in (even in functions declared inside the function).

  - When trying to access an identifier, the JavaScript Engine will first look in the current function. If it doesn't find anything, it will continue to the next outer function to see if it can find the identifier there. It will keep doing this until it reaches the global scope.

  - Global identifiers are a bad idea. They can lead to bad variable names, conflicting variable names, and messy code.

## Global Variables

So you might be wondering:

"Why wouldn't I always use global variables? Then, I would never need to use function arguments since ALL my functions would have access to EVERYTHING!"

Well... Global variables might seem like a convenient idea at first, especially when you're writing small scripts and programs, but there are many reasons why you shouldn't use them unless you have to. For instance, global variables can conflict with other global variables of the same name. Once your programs get larger and larger, it'll get harder and harder to keep track and prevent this from happening.

There are also other reasons you'll learn more about in more advanced courses. But for now, just work on minimizing the use of global variables as much as possible.

## Hoisting

Sometimes your JavaScript code will produce errors that may seem counterintuitive at first. Hoisting is another one of those topics that might be the cause of some of these tricky errors you're debugging.

Before any function being executed, all function declarations are "hoisted" to the top of their current scope.

  - JavaScript hoists function declarations and variable declarations to the top of the current scope.

  - Variable assignments are not hoisted.

  - Declare functions and variables at the top of your scripts, so the syntax and behavior are consistent with each other.

## Function Expressions

Storing function within a variables

#### Function Declaration

{% highlight js %}
function catSays (max) {
  //your code here
};

catSays();
{% endhighlight %}

#### Function Expression

{% highlight js %}
var catSays =
  function (max) {
    //your code here
  };

catSays();
{% endhighlight %}


Once you know how to declare a function, a whole new set of possibilities will open up to you.

For instance, remember how you can store anything you want in a variable? Well, in JavaScript, you can also store functions in variables. When a function is stored inside a variable it's called a function expression.

{% highlight js %}
var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};
{% endhighlight %}

Notice how the `function` keyword no longer has a name.

{% highlight js %}
var catSays = function(max) {
  // code here
};
{% endhighlight %}

It's an `anonymous function`, a function with no name, and you've stored it in a variable called `catSays`.

And, if you try accessing the value of the variable `catSays`, you'll even see the function returned back to you.

`catSays;`

Return:

{% highlight js %}
function(max) {
  var catMessage = ""
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
}
{% endhighlight %}

#### Function expressions and hoisting

Deciding when to use a function expression and when to use a function declaration can depend on a few things, and you will see some ways to use them in the next section. But, one thing you'll want to be careful of, is hoisting.

All function declarations are hoisted and loaded before the script is actually run. Function expressions are not hoisted, since they involve variable assignment, and only variable declarations are hoisted. The function expression will not be loaded until the interpreter reaches it in the script.

## Patterns with Function Expressions

#### Functions as parameters

Being able to store a function in a variable makes it really simple to pass the function into another function. A function that is passed into another function is called a callback. Let's say you had a `helloCat()` function, and you wanted it to return `"Hello"` followed by a string of "meows" like you had with `catSays`. Well, rather than redoing all of your hard work, you can make `helloCat()` accept a callback function, and pass in `catSays`.

{% highlight js %}
// function expression catSays
var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};

// function declaration helloCat accepting a callback
function helloCat(callbackFunc) {
  return "Hello " + callbackFunc(3);
}

// pass in catSays as a callback function
helloCat(catSays);
{% endhighlight %}

#### Inline function expressions

A function expression is when a function is assigned to a variable. And, in JavaScript, this can also happen when you pass a function inline as an argument to another function. Take the `favoriteMovie` example for instance:

{% highlight js %}
// Function expression that assigns the function displayFavorite
// to the variable favoriteMovie
var favoriteMovie = function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
};

// Function declaration that has two parameters: a function for displaying
// a message, along with a name of a movie
function movies(messageFunction, name) {
  messageFunction(name);
}

// Call the movies function, pass in the favoriteMovie function and name of movie
movies(favoriteMovie, "Finding Nemo");
{% endhighlight %}

Consile will print: `My favorite movie is Finding Nemo`

But you could have bypassed the first assignment of the function, by passing the function to the movies() function inline.

{% highlight js %}
// Function declaration that takes in two arguments: a function for displaying
// a message, along with a name of a movie
function movies(messageFunction, name) {
  messageFunction(name);
}

// Call the movies function, pass in the function and name of movie
movies(function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
}, "Finding Nemo");
{% endhighlight %}

Console will print: `My favorite movie is Finding Nemo`

This type of syntax, writing function expressions that pass a function into another function inline, is really common in JavaScript. It can be a little tricky at first, but be patient, keep practicing, and you'll start to get the hang of it!

#### Why use anonymous inline function expressions?

Using an anonymous inline function expression might seem like a very not-useful thing at first. Why define a function that can only be used once and you can't even call it by name?

Anonymous inline function expressions are often used with function callbacks that are probably not going to be reused elsewhere. Yes, you could store the function in a variable, give it a name, and pass it in like you saw in the examples above. However, when you know the function is not going to be reused, it could save you many lines of code to just define it inline.

## Function Expression Recap

Function Expression: When a function is assigned to a variable. The function can be named, or anonymous. Use the variable name to call a function defined in a function expression.

{% highlight js %}
// anonymous function expression
var doSomething = function(y) {
  return y + 1;
};
{% endhighlight %}

{% highlight js %}
// named function expression
var doSomething = function addOne(y) {
  return y + 1;
};
{% endhighlight %}

{% highlight js %}
// for either of the definitions above, call the function like this:
doSomething(5);
{% endhighlight %}

Console will print: `6`

You can even pass a function into another function inline. This pattern is commonly used in JavaScript, and can be helpful streamlining your code.

{% highlight js %}
// function declaration that takes in two arguments: a function for displaying
// a message, along with a name of a movie
function movies(messageFunction, name) {
  messageFunction(name);
}

// call the movies function, pass in the function and name of movie
movies(function displayFavorite(movieName) {
  console.log("My favorite movie is " + movieName);
}, "Finding Nemo");
{% endhighlight %}

## Function Examples

{% highlight js %}
var laugh = function(num) {
    var message = "";
    for (var x = 0; x < num; x++) {
        message += "ha";
    }
    return message + "!";
};
// finish the function expression //

console.log(laugh(10));
{% endhighlight %}

Console will print: `hahahahahahahahahaha!`


{% highlight js %}
function emotions(myString, myFunc) {
    console.log("I am " + myString + ", " + myFunc(2));
} emotions ("happy", function (x) {
    var laugh = "";
    for (var y=0; y<x; y++){
        laugh += "ha";
    }
    return laugh + "!";
})
{% endhighlight %}

Console will print: `I am happy, haha!`
