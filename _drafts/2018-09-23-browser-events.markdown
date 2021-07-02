---
layout: post
title: "Browser Events"
date: "2018-09-23 21:17:06 -0700"
tags: [DOM, JavaScript, HTML, CSS]
---

## Seeing An Event

There is a hidden world of events going on right now on this very page! It's really hard to actually see into this hidden world, though. So how can we know that events really are being announced? If they are being announced, how come they're not easy for us to see?

Fortunately, the Chrome browser has a special `monitorEvents()` function that will let us see different events as they are occurring.

Check out the documentation on the Chrome DevTools site: `monitorEvents` documentation

Chrome browser does offer an `unmonitorEvents()` function that will turn off the announcing of events for the targeted element:

// start displaying all events on the document object
`monitorEvents(document);`

// turn off the displaying of all events on the document object.
`unmonitorEvents(document);`

One last little bit of info on `monitorEvents` is that this is for development/testing purposes only. It's not supposed to be used for production code.

## EvenTarget

is an interface implemented by objects that can receive events and may have listeners for them.

and

Element, document, and window are the most common event targets, but other objects can be event targets too…

👓 EvenTarget page: https://developer.mozilla.org/en-US/docs/Web/API/EventTarget

If you take a look at the `EventTarget` Interface, you'll notice that it doesn't have any properties and only three methods! These methods are:

`.addEventListener()`

`.removeEventListener()`

`.dispatchEvent()`

## Adding An Event Listener

Using the `.addEventListener()` method will let us listen for events and respond to them! I just said "listen for events". There are several ways to "phrase" this, so I want to give some examples:

  - listen for an event
  - listen to an event
  - hook into an event
  - respond to an event

...all of these mean the same thing and are interchangeable with one another.

Let's use some pseudo-code to explain how to set an event listener:

`<event-target>.addEventListener(<event-to-listen-for>, <function-to-run-when-an-event-happens>);`

So an event listener needs three things:

  1. an event target - this is called the target
  2. the type of event to listen for - this is called the type
  3. a function to run when the event occurs - this is called the listener

The `<event-target>` (i.e. the target) goes right back to what we just looked at: everything on the web is an event target (e.g. the `document` object, a `<p>` element, etc.).

The `<event-to-listen-for>` (i.e. the type) is the event we want to respond to. It could be a click, a double click, the pressing of a key on the keyboard, the scrolling of the mouse wheel, the submitting of a form...the list goes on!

The `<function-to-run-when-an-event-happens>` (i.e. the listener) is a function to run when the event actually occurs.

Let's transform the pseudo-code to a real example of an event listener:

`const mainHeading = document.querySelector('h1');

mainHeading.addEventListener('click', function () {
  console.log('The heading was clicked!');
});`

Let's break down the snippet above:

  - the target is the first `<h1>` element on the page
  - the event type to listen for is a `"click"` event
  - the listener is a function that logs `"The heading was clicked!"` to the console

👓 List of events: https://developer.mozilla.org/en-US/docs/Web/Events

## Removing An Event Listener

To remove an event listener, we use the `.removeEventListener()` method.

The `.removeEventListener()` method requires you to pass the same exact listener function to it as the one you passed to `.addEventListener()`.

Let's see some pseudo-code for the `.removeEventListener()`:

`<event-target>.removeEventListener(<event-to-listen-for>, <function-to-remove>);`

So an event listener needs three things:

  1. an event target - this is called the `target`
  2. the type of event to listen for - this is called the `type`
  3. he function to remove - this is called the `listener`

Remember, the listener function must be the exact same function as the one used in the `.addEventListener()` call...not just an identical looking function. Let's look at a couple of examples.

This code will successfully add and then remove an event listener:

`function myEventListeningFunction() {
    console.log('howdy');
}`

// adds a listener for clicks, to run the `myEventListeningFunction` function
`document.addEventListener('click', myEventListeningFunction);`

// immediately removes the click listener that should run the `myEventListeningFunction` function
`document.removeEventListener('click', myEventListeningFunction);`

It works because both `.addEventListener()` and `.removeEventListener`:

  - have the same target
  - have the same type
  - and pass the exact same listener

💥 Instead of `event`, the parameter's name could just as easily be:

  - evt
  - e
  - theEvent
  - horse
