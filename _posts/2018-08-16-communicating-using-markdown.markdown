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

## Activity: Add a comment

1. Add a comment to this issue, using Markdown to create a list of items to complete. Your task can include any tasks you wish, or you can use this example:

  {% highlight html %}
  - [ ] Turn on GitHub Pages
  - [ ] Outline my portfolio
  - [ ] Introduce myself to the world
  {% endhighlight %}

2. Use the Preview tab to check your markdown formatting

3. Click Comment
