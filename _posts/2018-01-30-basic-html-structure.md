---
layout: post
title: "Basic HTML Structure"
date: 2018-01-30
categories: HTML
---

## <!DOCTYPE>

The `<!DOCTYPE>` is an instruction to the web browser about what version of HTML the page is written in. The `<!DOCTYPE>` declaration must be the very first thing in your HTML document, before the `<html>` tag. The `<!DOCTYPE>` declaration is NOT case sensitive.


## <html>...</html>

The `<html>` tag tells the browser that this is an HTML document. The `<html>` tag represents the root of an HTML document. All other tags must fall between the `<html>` tags.


## <head>...</head>

The `<head>` contains information about the document that will not appear on the actual page The `<head>` element can include a title for the document, scripts, styles, meta information, and more.

## <title>...</title>

The `<title>` tag is required in all HTML documents and it defines the title of the document in the title bar of your web browser.


## <meta ...>

Metadata is data (information) about data. `<Meta>` tags contain information about the page that does not need to be displayed, but it still used by search engines and other web crawlers. `<meta>` can be used by browsers (how to display content or reload page), search engines (keywords), or other web services.

Note! HTML5 has a new attribute, charset, which makes it easier to define charset: `<meta charset="UTF-8">`

## <link ...>

The `<link>` tag defines a link between a document and an external resource. The `<link>` tag is used to link to external stylesheet (css, JavaScript, etc).

Note! Since there are many version if Internet Explorer, there is a need to include a link here so the older versions of IE can run codes: `<link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" type="text/css">`


{% highlight html %}

    <!DOCTYPE html>
    <html>
      <head>
        <title>First Web Page</title>
        <meta charset="UTF-8">
        <link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" type="text/css">
      </head>
      <body>
        Basic content for the first web page.
      </body>
    </html>

{% endhighlight %}
