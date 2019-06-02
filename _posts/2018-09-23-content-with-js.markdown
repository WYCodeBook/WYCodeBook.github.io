---
layout: post
title: "Content with JS"
date: "2018-09-23 14:34:27 -0700"
categories: Notes
tags: [DOM, JavaScript, HTML, CSS]
description: The Basic - Writing Content with JavaScript
---

### An Element's Inner HTML

Every element inherits properties and methods from the Element Interface (remember this from the previous lesson!). This means that every element has an `.innerHTML` property. This property, as it's rightly named, represents the markup of the element's content. We can use this property to:

  - get an element's (and all of its descendants!) HTML content

  - set an element's HTML content

### An Element's Text Content

The `.textContent` property will:

set the text content of an element and all its descendants
return the text content of an element and all its descendants

💥 Like the `.textContent` property, the `.innerText` property can be used to get/set an element's text content, but there are some important differences between the two properties.

`.textContent` sets/gets the text content of an element...pretty clear and simple.

`.innerText` on the other hand, is a little tricker, it will just show all the content in plain-text

💥 Between `.textContent` and `.innerText`, you probably want to use `.textContent` since that will return all of the text no matter what. Rarely will you actually want only the visible text.

### Add New Page Content Recap

How to create new DOM elements and add them to the page:

`.createElement()` to create new elements

`.appendChild()` to add a child element to a parent element as its last child

`.createTextNode()` to create a text node

`.insertAdjacentHTML()` to put HTML text anywhere around an element

Some important things to note are:

  - if an element already exists in the DOM and this element is passed to `.appendChild()`, the `.appendChild()` method will move it rather than duplicating it

  - an element's `.textContent` property is used more often than creating a text node with the `.createTextNode()` method

  - the `.insertAdjacentHTML()` method's second argument has to be text, you can't pass an element

### Remove Page Content Recap

Two ways to remove an element from the page. You learned about:

`.removeChild()`

`.remove()`

The difference is that with `.removeChild()` must be called on the parent of the element being removed and must be passed the child to be removed, while `.remove()` can be called directly on the element to delete.

More helpful properties:

`.firstChild`

`.firstElementChild`

`.parentElement`

The difference between `.firstChild` and `.firstElementChild`, is that `.firstElementChild` will always return the first element, while `.firstChild` might return whitespace (if there is any) to preserve the formatting of the underlying HTML source code.

### Style Page Content Recap

  - modifying individual styles with `.style.<prop>`

  - updating multiple styles at once with `.style.cssText`

  - getting/setting a list of classes with `.className`

  - getting/setting/toggling CSS classes with `.classList`

`.classList` is by far the most helpful property of the bunch, and it helps to keep your CSS styling out of your JavaScript code.
