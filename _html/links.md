---

layout: collection
title: "Links"
picture:
description: Linking sites, emails, image, and sections of the page
---


Links are necessary for users to jump from one page to another. HTML links are defined with the `<a>` tag.

{% highlight html %}
  <a href="url">link text</a>
{% endhighlight %}

The `href` attribute specifies the destination address (the url) of the link. The `link text` is the visible part.

👓 Read more about Links at:

- [3wschools - Links](https://www.w3schools.com/html/html_links.asp)
- [Simple Guide to HTML](http://www.simplehtmlguide.com/linking.php)



### Basic Link

There are two main parts to a link tag: the text a user can click, and the web address they go to if they click it. The bit between the `<a>` and `</a>` tags is the link text, and is generally displayed in blue and underlined by web browsers. The `href="url"` part is the web address, where `url` can be set in several ways:

- href="example.html" - another page in the current directory
- href="example/page.html" - a relative location
- href="http://wycodebook.github.io" - a full address

{% highlight html %}
  <a href="url">link text</a>
{% endhighlight %}



### Image as a Link

By placing an image tag between the `<a>` and `</a>` tags, you can turn an image into a link, and clicking on that image will then load the referenced page. `<a href="url"><img ...></a>`

{% highlight html %}
  <a href="default.asp">
    <img src="smiley.gif" alt="HTML tutorial">
  </a>
{% endhighlight %}

💥 By default, you may notice that the image gets a blue border just as link text became underlined. This can be resolved by setting the `border="0"` attribute of the image, or using css.

{% highlight html %}
  <a href="default.asp">
    <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;border:0;">
  </a>
{% endhighlight %}



### Email Link

A special kind of link, the `mailto` notation link instructs the browser to compose and email to the specified address using the default email program. But it does not actually send any emails automatically.

{% highlight html %}
  <a href="mailto:email"></a>
{% endhighlight %}

You can also set a subject for the email by using

{% highlight html %}
  <a href="mailto:xyz@sample.com?Subject=Links">email me</a>.
{% endhighlight %}



### Link Titles

The title attribute specifies extra information about an element. The information is most often shown as a tooltip text when the mouse moves over the element.

{% highlight html %}
  <a href="https://wycodebook.github.io" title="Go To WY's Code Book">WY's Code Book</a>
{% endhighlight %}



### Create a Bookmark (Internal Linking)

HTML bookmarks are used to allow readers to jump to specific parts of a Web page.

Step 1: Create a bookmark with the id attribute:

{% highlight html %}
  <h2 id="link">HTML Links</h2>
{% endhighlight %}

Step 2: Add a link to the bookmark ("Jump to HTML Links"), from within the same page:

{% highlight html %}
  <a href="#link">Jump to HTML Links</a>
{% endhighlight %}

💥 By default, a link will appear like this (in all browsers):

- An unvisited link is underlined and blue
- A visited link is underlined and purple
- An active link is underlined and red
- You can change the default colors, by using CSS.