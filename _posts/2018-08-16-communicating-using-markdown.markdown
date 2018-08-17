---
layout: post
title: "Communicating using Markdown"
date: "2018-08-16 17:25:40 -0700"
categories: GitHub
description: GitHub Learning Lab Course 2
---

## What is Markdown?

Markdown is a lightweight syntax for writing all types of communication on GitHub, as well as many other places on the web. You can format words as bold or italic, add images, and create lists. Mostly, Markdown is just regular text combined with a few non-alphabetic symbols, such as `#` or `*`. You can use Markdown with the formatting toolbar in issues 📖 and pull requests 📖, or you can learn the syntax and type it yourself.

You can use Markdown most places around GitHub:

  - Comments in issues and pull requests (like this one!)

  - Files with the .md or .markdown extension

  - Sharing snippets of text in Gists

## Step 1: Create a Task List

A task list creates checkboxes that can be checked off by people with access 📖 in a repository. They're very useful for tracking issues and pull requests.

If you include a task list in the first comment of an issue or pull request, you'll see a progress indicator in your issue list.

Watch out! The syntax for task lists is very specific. Be sure to include the spaces where required, or else they won't render properly.

#### Example markup:

{% highlight html %}

- [x] Additional markup is supported, including @mentions, #referencess, [links](url), **emphasis**, and <del>HTML tags</del>.
- [x] List syntax is required.
  - You can nest lists below, too!
- [x] This item is completed.
- [ ] This item is not complete.

{% endhighlight %}

#### Activity: Add a comment

  - Add a comment to this issue, using Markdown to create a list of items to complete.

  Your task can include any tasks you wish, or you can use this example:

    {% highlight html %}
    - [ ] Turn on GitHub Pages
    - [ ] Outline my portfolio
    - [ ] Introduce myself to the world
    {% endhighlight %}

  - Use the Preview tab to check your markdown formatting

  - Click Comment

## Step 2: Turn on GitHub Pages

Turning this course 2 into GitHub Pages

#### Activity: Enable GitHub Pages

  - Under your repository name, click Settings.

  - In the GitHub Pages section, use the Select source drop-down menu to select master as your GitHub Pages publishing source.

  - Click Save.

## Step 3: Add headers

We'll learn how to edit the file in this pull request to incorporate some Markdown headers.

You can see an example of a header at the top of this page! Just like in HTML, a header is a larger bit of text at the beginning of a section. There are six sizes.

#### Example

  {% highlight html %}

    # This is an <h1> header, which is the largest

    ## This is an <h2> header

    ###### This is an <h6> header, which is the smallest

  {% endhighlight %}

In issues, pull requests, and comments, you can use the text formatting toolbar.

The toolbar isn't available everywhere. When you edit a file, you must type the `#` symbols manually.

#### Activity: Edit your file with headers

  1. In this pull request, click the Files changed tab.
  2. In the upper right corner of the file view, click the small pencil ✏️ icon for the file `titled _includes/01-name.md`.
  3. On the Edit file tab, add a # before the content to make it an H1 Header. You can add more headers, using one to six # characters.
  4. Above your new content, click Preview changes.
  5. At the bottom of the page, type a short, meaningful commit message that describes the change you made to the file.
  6. Click Commit changes.

## Step 4: Merge your headers
