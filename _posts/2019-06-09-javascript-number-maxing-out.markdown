---
layout: resource
title: "JavaScript Number Maxing Out"
date: "2019-06-09 19:34:02 -0700"
tags: JavaScript
categories: Notes
---

The MAX_SAFE_INTEGER constant has a value of 9007199254740991 (9,007,199,254,740,991 or ~9 quadrillion). The reasoning behind that number is that JavaScript uses [double-precision floating-point format](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) numbers as specified in [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) and can only safely represent numbers between -(253 - 1) and 253 - 1.

Note: Safe in this context refers to the ability to represent integers exactly and to correctly compare them.


[MDN - Number​.MAX_SAFE_INTEGER](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER)
