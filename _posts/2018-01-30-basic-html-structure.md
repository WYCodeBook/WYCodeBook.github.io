---
layout: post
title: "Basic HTML Structure"
date: 2018-03-30
categories: HTML
---

## Document Type <!DOCTYPE>

The `<!DOCTYPE>` is an instruction to the web browser about what version of HTML the page is written in. `<!DOCTYPE html>` is used to declear HTML 5. The `<!DOCTYPE>` declaration must be the very first thing in your HTML document, before the `<html>` tag. The `<!DOCTYPE>` declaration is NOT case sensitive.

## The HTML <html>...</html>

The `<html>` tag tells the browser that this is an HTML document. The `<html>` tag represents the root of an HTML document. All other tags must fall between the `<html>` tags.

## Header <head>...</head>

The `<head>` contains information about the document that will not appear on the actual page. The `<head>` element can include a title for the document, scripts, styles, meta information, and more.


## Title <title>...</title>

The `<title>` tag is required in all HTML documents and it defines the title of the document in the title bar of your web browser.

## Metadata <meta ...>

Metadata is data (information) about data. `<Meta>` tags contain information about the page that does not need to be displayed, but it still used by search engines and other web crawlers. `<meta>` can be used by browsers (how to display content or reload page), search engines (keywords), or other web services.

💡 HTML5 has a new attribute, charset, which makes it easier to define charset: `<meta charset="UTF-8">`

## <link ...>

The `<link>` tag defines a link between a document and an external resource. The `<link>` tag is used to link to stylesheet(s). The `<link>` element is an empty element, it contains attributes only.

💡 Since there are many version if Internet Explorer, remember to link older versions of IE to ensure codes are working properly: `<link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" type="text/css">`

## The Body <body>...</body>

The `<body>` tags contain all the information and other visible content on the page. The `<body>` element contains all the contents of an HTML document, such as text, hyperlinks, images, tables, lists, etc.

## Example: Basic HTML structure

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
