---

layout: post
title: "HTML Images"
date: 2018-03-30
categories: HTML
img: /img/coding_logo.png

---

Images are defined with the `<img>` tag.

💥 The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The basic form of the `<img>` tag:

{% highlight html %}
  <img src="url">
{% endhighlight %}

`<img>` tag with more details:

{% highlight html %}
  <img src="xyz.jpg" alt="xyz.com" width="104" height="142">
{% endhighlight %}

The `src` attribute specifies the URL (web address) of the image.

The `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the `src` attribute, or if the user uses a screen reader).

💥 You can use the style attribute to the `<img>` tag to make it interesting. However, it's not recommended, because your codes will be cleaner if you systemically apply styles in the CSS stylesheet(s).

- An image will normally be shown actual size, but by using the width and height attributes you can change the displayed size. `<img ... width="?" height="?">` You can specify the size in pixels or as a percentage.

- Add a border by specifying the thickness in pixels. `<img ... border="?">` You can also set border="0" to remove the border added when images are used as links.

- By default `<img ... align="?">` an image appears at the place specified in the html code(as with any other tag). However, you can align an image with the surrounding text or paragraph by setting any of `align="left | right | top | bottom | middle"`.

- Adjust the whitespace (or runaround space) around an image, in pixels. `<img ... vspace="?" hspace="?">` Use `vspace` to adjust the vertical spacing above and below, or `hspace` for the left and right sides.

- Use the CSS `float` property to let the image float to the right or to the left of a text by using `float:"right | left"`.

👓 Read more about Links at:

- [3wschools - Images](https://www.w3schools.com/html/html_images.asp)
- [Simple Guide to HTML](http://www.simplehtmlguide.com/images.php)
