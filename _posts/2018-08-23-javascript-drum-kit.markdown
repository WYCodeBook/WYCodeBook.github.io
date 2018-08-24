---
layout: post
title: "JavaScript Drum Kit"
date: "2018-08-23 20:25:02 -0700"
categories: JavaScript30DaysChallenge
description: JavaScript coding challenge DAY 1
---

### DAY 1

It is very exciting to start this challenge! During the Setup-Video and Day-1 Video, Wes mentioned there are many ways people learn and practice codes with the challenge materials and there is no one-fitted-all way to learn.

Since it's the first day of the challenge... I will just follow step by step presented in the video and begin my learning challenge Day 1 🤩

### Collective of notes from many people

##### window.addEventListener('keydown', playSound)

  - `playSound()` is a listener for `keydown` events registered using `window.addEventListener`.

  - `window` is the global object in a browser, or the root object of the DOM. And `document` stands for DOM.

👓 [JavaScript HTML DOM EventListener](https://www.w3schools.com/js/js_htmldom_eventlistener.asp)

  - `keydown` is the type of event

  - `playSound` is going to be the function we want to call when the event occur

In another word, this is what we want from `window.addEventListener('keydown', playSound)`... when we hit a key on the keyboard, meaning `keydown`, we would like to run the `playSound` function.

##### const audio = document.querySelector('audio[data-key="${e.keyCode}"]');

##### const key = document.querySelector('div[data-key="${e.keyCode}"]');

  - `keyCode` property is the KEY to connect our buttons(`<div>`s) and sounds(`<audio>`s).

  - `keyCode` 's value is same as ASCII code (in lowercase letter ), check keycodes [here](http://keycode.info/).

  - `data-key` is set for mapping buttons and audios to get the `keyCodes` via `keydown` event.

  - the whole `querySelector` expression has to be in back ticks `


  - `${}` is syntactic sugar for template literals, read more about Expression interpolation [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

💥 To figure out what key was pressed we simply look for the `keyCode` inside the event that was send to the function. You see every key has it’s own unique code. While this is different on some keyboards / inputs, they are mostly the same and you can use this little website Wes created called keycode.info to figure out the codes you need.

👓 [Keycode for JavaScript](http://keycode.info/)

##### if(!audio) return;

This is used to stop the function from running when the selected key from the keyboard is not matching any of the listed keys and audios.

##### audio.currentTime = 0;

##### audio.play();

These are used to prevent delay playing sounds as we keep selecting keys from the keyboard.

##### key.classList.add('playing');

  - use `item.classList.add('className')` to add class when key pressed. (same as `element.addClass('className')` in jQuery)

##### if(e.propertyName != 'transform') return;
##### event.target.classList.remove('playing');

  - to remove the add class we can just do `.remove` but not until we have checked for `transitionend` with another `eventListener`.

##### keys.forEach(key => key.addEventListener('transitionend', removeTransition));

  - `items.forEach()` instead of just `forEach`, which means it's a property of an array.

##### event

using `e` representing event

### Final Codes

{% highlight js %}

  function.playSound(e){
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
    const key = document.querySelector(`div[data-key="${e.keyCode}"]`);

    if(!audio) return; //stop the function from running all together

    audio.currentTime = 0; //rewind to the stop
    audio.play();

    key.classList.add('playing'); //adding a class to a pressed key
  }

  function removeTransition(e) {
    if(e.propertyName != 'transform') return; //skip it if it's not a transform
    event.target.classList.remove('playing'); //used to remove the add class
  }

  const keys = document.querySelectorAll(`.key`);
  keys.forEach(key => key.addEventListener('transitionend', removeTransition)); //items.forEach() instead of just forEach, which means it's a property of an array.
  window.addEventListener('keydown', playSound) //when we hit a key on the keyboard, meaning `keydown`, we would like to run the `playSound` function.
{% endhighlight %}
