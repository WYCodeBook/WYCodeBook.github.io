---

layout: post
title: "HTML Lists"
date: 2018-03-30
categories: HTML
img: /img/coding_logo.png

---

Lists are defined with the `<ul>` (unordered/bullet list) or the `<ol>` (ordered/numbered list) tag, followed by `<li>` tags (list items).

### Unordered HTML List

An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag. The list items will be marked with bullets (small black circles) by default.

{% highlight html %}
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>
{% endhighlight %}

Choose List Item Markers: The CSS `list-style-type` property is used to define the style of the list item marker.

- `disc` Sets the list item marker to a bullet (default)
- `circle` Sets the list item marker to a circle
- `square` Sets the list item marker to a square
- `none` The list items will not be marked

{% highlight html %}
  <ul style="list-style-type:disc">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>
{% endhighlight %}

### Ordered HTML List

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag. The list items will be marked with numbers by default.

{% highlight html %}
  <ol>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ol>
{% endhighlight %}

The `type` attribute of the `<ol>` tag, defines the type of the list item marker:

- `type="1"` The list items will be numbered with numbers (default)
- `type="A"` The list items will be numbered with uppercase letters
- `type="a"` The list items will be numbered with lowercase letters
- `type="I"` The list items will be numbered with uppercase roman numbers
- `type="i"` The list items will be numbered with lowercase roman numbers

{% highlight html %}
  <ol type="A">
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ol>
{% endhighlight %}

👓 Read more about Links at:

- [3wschools - Lists](https://www.w3schools.com/html/html_lists.asp)
- [Simple Guide to HTML](http://www.simplehtmlguide.com/lists.php)
