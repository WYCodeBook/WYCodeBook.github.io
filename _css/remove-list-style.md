---

layout: collection
title: "Removing List Styles"
picture:
description: How to remove all the styling for lists?

---

In a rare situation, bullet points and numbers for a list may not look good in certain style; so here is a solution on how to remove those default styles for a list.

With the following code, you can remove the numbers, bullet points, and indentation for lists.



{% highlight css %}
ul {
  list-style-type: none;
  margin-left: 0px;
  padding-left: 0px;
}
{% endhighlight %}