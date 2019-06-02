---
layout: post
title: "GitHub Pages"
date: "2018-08-23 17:17:30 -0700"
categories: Notes
tags: [GitHub, Jekyll]
description: GitHub Learning Lab Course 3
---

🔍 [Step 1](#step-1) 🔍 [Step 2](#step-2) 🔍 [Step 3](#step-3) 🔍 [Step 4](#step-4) 🔍 [Step 5](#step-5) 🔍 [Step 6](#step-6) 🔍 [Step 7](#step-7) 🔍 [Step 8](#step-8)

---

In this course, you’ll learn how to:

- Enable GitHub Pages
- Choose a theme with Jekyll
- Use YAML front matter
- Customize your site
- Create and edit blog posts

## Step 1: Enable GitHub Pages

In this course, you'll create a blog hosted on GitHub Pages and learn how to:

  - Enable GitHub Pages
  - Use Jekyll, a static site generator
  - Customize Jekyll sites with a theme and content

#### Activity: Turn on GitHub Pages

The first step to publishing your blog to the web is to enable GitHub Pages on this repository 📖. When you enable GitHub Pages on a repository, GitHub takes the content that's on the master branch and publishes a website based on its contents.

  - Under your repository name, click Settings

  - In the "GitHub Pages" section, use the Select source drop-down menu to select the master branch as your GitHub Pages publishing source.

  - Click Save

  - After GitHub Pages is enabled, we'll be ready to create some content.

💥 Turning on GitHub Pages creates a deployment of your repository. It may take up to a minute to respond as I await the deployment.

## Step 2: Customize your homepage

You can customize your homepage by adding content to either an `index` file or the `README.md` file. GitHub Pages first looks for an `index` file. If an `index` file is found, GitHub Pages uses the content in the file to create the homepage. If an `index` file isn’t found, it uses the `README.md` to create the homepage.

Your repository has an `index.md` file so we can update it to include your personalized content.

#### Activity: Create your homepage

  - Navigate to the Code tab of this repository, and browse to the index.md file.

  - In the upper right corner, click the ✏️ pencil icon to open the file editor.

  - Type the content you want on your homepage and remember, you can use Markdown to format your content.

  - Scroll to the bottom, type a commit message, and click Create a new branch for this commit and start a pull request.

  - Open a pull request.

## Step 3: Merge your pull request

Merge the pull request.

#### Activity: Merge your pull request

  - Click Merge pull request below

  - Click Confirm merge

  - Click Delete branch

## Step 4: Adding a Theme

Let's add a theme to the blog site.

#### Activity: Select a basic theme

  - Under your repository name, click Settings.

  - In the "GitHub Pages" section, click Choose a theme.

  - Click the theme you want to use and then click Select theme.

## Step 5: Customize Site Details

Getting your page blog ready: GitHub added the theme you selected to your `_config.yml` file. Jekyll uses the` _config.yml` file to store settings for your site, like your theme, as well as reusable content like your site title and GitHub handle.

You can check out the `_config.yml` file on the Code tab of your repository.

#### Activity: Modify the config file

Let's change the `_config.yml` so it's a perfect fit for your new blog. First, we need to use a blog-ready theme. For this activity, we will use a theme named `minima`.

  - Navigate to the Code tab of this repository, and browse to the `_config.yml` file.

  - In the upper right corner, click ✏️ to open the file editor.

  - Change `theme:` to `minima` and modify the other configuration variables such as `title:`, `author:`, and `description:` to customize your site.

  - Click Create a new branch for this commit and start a pull request.

  - Open a pull request.

## Step 6: Create a blog post

#### Activity: Add some content to your blog

  - On the `"Code"` tab, select your `WYCodeBook-patch-1` branch

  - Click Create new file

  - Name the file `_posts/YYYY-MM-DD-title.md`, but replace the `YYYY-MM-DD` with today's date, and `title` with the title you'd like to use for your first blog post

  - If your blog post date doesn't follow the correct date convention, you'll receive an error and your site won't build. For more information, see "Page build failed: Invalid post date".

  - Type a quick draft of your blog post. Remember, you can always edit it later

  - Commit your changes to your branch

👓 [Page build failed: Invalid post date](https://help.github.com/articles/page-build-failed-invalid-post-date/)

## Step 7: Add blog post metadata

Now that you've created your Jekyll blog post file, we can add syntax to it. The syntax Jekyll files use is called YAML front matter. It goes at the top of your file and looks something like this:

{% highlight md %}
---
title: "Welcome to my blog"
date: 2019-01-20
---
{% endhighlight %}

This example adds a title and date to your blog post. There are other useful things you could add here in the future like layouts, categories, or any other logic that is useful to you. For more information about configuring front matter, see the [Jekyll front matter documentation](https://jekyllrb.com/docs/frontmatter/).

#### Activity: Add Front Matter

  - Click the "Files Changed" tab in this pull request

  - Click on the pencil icon on the right side of the screen

  - Type the following content at the top of your blog post:

  {% highlight md %}
  ---
  title: "YOUR-TITLE"
  date: YYYY-MM-DD
  ---
  {% endhighlight %}

  - Replace YOUR-TITLE with the title for your blog post

  - Replace YYYY-MM-DD with today's date

  - Commit your changes to your branch

## Step 8: Merge your first post

#### Activity: Merge your pull request

  - If satisfied with your post, click Merge pull request

  - Click Confirm merge

  - Click Delete branch

![GitHub Course 3 Completed](/pic/GHcourse3.PNG)
