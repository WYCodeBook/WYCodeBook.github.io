---
layout: post
title: "Communicating using Markdown"
date: "2018-08-16 17:25:40 -0700"
categories: GitHub
description: GitHub Learning Lab Course 2
---

This course will walk you through creating and using headings more effectively, organizing thoughts in bulleted lists, and showing how much work you’ve completed with checklists. You can even use Markdown to add some depth to your work with the help of emoji, images, and links. See a word you don't understand? We've included an emoji 📖 next to some key terms. Click on it to see its definition.

In this course, you’ll learn how to:

- Use Markdown to add lists, images, and links in a comment or text file
- Determine where and how to use Markdown in a GitHub repository

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

  - Add a comment to this issue, using Markdown to create a list of items to complete.Your task can include any tasks you wish, or you can use this example:

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

  - In this pull request, click the Files changed tab.

  - In the upper right corner of the file view, click the small pencil ✏️ icon for the file `titled _includes/01-name.md`.

  - On the Edit file tab, add a # before the content to make it an H1 Header. You can add more headers, using one to six # characters.

  - Above your new content, click Preview changes.

  - At the bottom of the page, type a short, meaningful commit message that describes the change you made to the file.

  - Click Commit changes.

## Step 4: Merge your headers

Let's merge this pull request and move on with the course.

#### Activity: Merge the Pull Request

Click Merge pull request.

#### Activity: Delete your branch

Go ahead and delete your branch 📖 in this pull request.

## Step 5: Add an image

You can add an image of yourself or anything else you'd like to feature. You'll also learn how to create descriptive text, or "alt text", for images, and how to create links.

#### Images

Let's add an image. Don't forget to include descriptive text in the square brackets. This text is read aloud for people using screen readers. It's also shown at times when your , or in case your image doesn't display, such as when there's a poor connection.

`![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)`


#### Activity: Adding an image
  - As you did before, edit the file in this pull request.

  - In the file, replace `_includes/02-image.md` with the correct Markdown for your image of choice. Don't forget to include alt-text!

  - Commit 📖 your changes.

## Step 6: Add a profile link

Next, you'll want to add links to your awesome portfolio projects. Links help create context when you’re communicating in issues and pull requests.

You might link to a website, a repository, or even a line of code. To create a link, put the text you want to display in square brackets, and the URL in the following parentheses.

`[GitHub](http://github.com)`

#### Activity: Add a link

  - Edit the file `_includes/03-links.md`.

  - Replace the filler text with a link to your GitHub profile (or anywhere else).

## Step 7: Merge your image and link

Pull request to share the updates

#### Activity: Merge the Pull Request

Click Merge pull request below.

## Step 8: Add a list

Help people get to know you by adding a list containing a few of your favorite things. Don't know what to add? Why not add a list of your favorite books or places to eat.

#### Activity: Create a list

  - Edit the `_includes/04-lists.md` in this pull request.

  - Create a markdown list in the file. It can be ordered or unordered.

  - Commit your changes.

## Step 9: Use emphasis

Let's try something new. You can use bold and italic text in Markdown. There are a couple of ways to create emphasis.

  {% highlight md %}

  *This text will be italic*
  _This will also be italic_

  **This text will be bold**
  __This will also be bold__

  _You **can** combine them_

  {% endhighlight %}

#### Activity: Add some emphasis

  - Edit the file `_includes/05-emphasis.md` in this pull request.

  - Use the Preview tab and your ✨ new Markdown knowledge, add emphasis (like bold or italics) to your skills.

  - Commit your changes.

## Step 10: Merge lists and emphasis

You can merge this pull request when you're ready.

#### Activity: Merge the Pull Request

Go ahead and click Merge pull request below.

## The Product of This Course

[Check It Out Here](https://wycodebook.github.io/markdown-portfolio/)

## Completed Course!

![GitHub Course 2 Completed](/pic/GHcourse2.PNG)
