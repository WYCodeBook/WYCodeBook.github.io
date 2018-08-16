---
layout: post
title: "Introduction to GitHub"
date: "2018-08-15 22:25:14 -0700"
categories: GitHub
description: GitHub Learning Lab Course 1
---

## What's GitHub?

GitHub is a collaboration platform.

GitHub is also a powerful version control tool.

▶️ [What's GitHub Video](https://www.youtube.com/watch?v=w3jLJU7DT5E)

## Repository

GitHub repository is the container that hold everything related to the project. The code view is where you will find the files included in the repository.

▶️ [GitHub Repository Video](https://www.youtube.com/watch?v=R8OAwrcMlRw)

`README.md` is used to explain the project and point readers to helpful information within the project.

The `CONTRIBUTING.md` is used to describe the process for contributing to the repository. A link to the CONTRIBUTING.md file is shown anytime someone creates a new issue or pull request.

The `ISSUE_TEMPLATE.md` is another file you can use to pre-populate the body of an issue. For example, if you always need the same types of information for bug reports, include it in the issue template, and every new issue will be opened with your recommended starter text.

## Issues

This is an issue 📖: a place where you can have conversations about bugs in your code, code review, and just about anything else.

Issue titles are like email subject lines. They tell your collaborators what the issue is about at a glance. For example, the title of this issue is Getting Started with GitHub.

#### Using Issues

Issues are used to discuss ideas, enhancements, tasks, and bugs. They make collaboration easier by:

  - Providing everyone (even future team members) with the complete story in one place

  - Allowing you to cross-link to other issues and pull requests 📖

  - Creating a single, comprehensive record of how and why you made certain decisions

  - Allowing you to easily pull the right people and teams into a conversation with @-mentions

▶️ [Issue Video](https://www.youtube.com/watch?v=Zhj46r5D0nQ)

## Notifications

Once you've commented on an issue or pull request, you'll start receiving email notifications when there's activity in the thread.

How to silence or unmute specific conversations:

  - Go to the issue or pull request

  - Under "Notifications", click the Unsubscribe button on the right to silence notifications or Subscribe to unmute them

You'll see a short description that explains your current notification status.

How to customize notifications in Settings:

  1. Click your profile icon

  2. Click Settings

  3. Click Notifications from the menu on the left and adjust your notification preferences

Repository notification options:

  - Watch: You'll receive a notification when a new issue, pull request or comment is posted, and when an issue is closed or a pull request is merged

  - Not watching: You'll no longer receive notifications unless you're @-mentioned

  - Ignore: You'll no longer receive any notifications from the repository

How to review notifications for the repositories you're watching:

  1. Click your profile icon

  2. Click Settings

  3. Click Notification from the menu on the left

  4. Click on the repositories you’re watching link

  5. Select the Watching tab

  6. Click the Unwatch button to disable notifications, or Watch to enable them


▶️ [Notification Video](https://www.youtube.com/watch?v=ocQldxF7fMY)

## GitHub Flow

People use different workflows to contribute to software projects, but the simplest and most effective way to contribute on GitHub is the GitHub flow.

#### Creating branch

You just learned how to create a branch—the first step in the GitHub flow.

Branches are an important part of the GitHub flow because they allow us to separate our work from the master branch. In other words, everyone's work is safe while you contribute.

Tips for using branches:

  - A single project can have hundreds of branches, each suggesting a new change to the master branch.

  - The best way to keep branches organized with a team is to keep them concise and short-lived. In other words, a single branch should represent a single new feature or bug fix. This reduces confusion among contributors when branches are only active for a few days before they’re merged into the master branch.

Creating a branch allows you to make modifications to your project without changing the deployed master branch.

▶️ [GitHub Flow Video](https://www.youtube.com/watch?v=PBI2Rz-ZOxU)

## Committing a file

When you’re finished creating or making changes to a file on GitHub, scroll to the bottom of the page. Then find the "Commit new file" section.

In the first field, type a commit message. The commit message should briefly tell contributors about the changes you are introducing to the file.

Rules to live by for commit messages:

  - Don’t end your commit message with a period.

  - Keep your commit messages to 50 characters or less. Add extra detail in the extended description window if necessary. This is located just below the subject line.

  - Use active voice. For example, "add" instead of "added" and "merge" instead of "merged".

  - Think of your commit as expressing intent to introduce a change.

## Open a pull request

While issues encourage discussion with other contributors and collaborators on a project, pull requests help you share your changes, receive feedback on them, and iterate on them until they’re perfect!

▶️ [Pull Request Video](https://www.youtube.com/watch?v=kJr-PIfLDl4&feature=youtu.be)



## Lesson Activities

1️⃣ Assign yourself

On the right side of the issue screen, under the "Assignees" section, click the gear icon and select yourself

2️⃣ GitHub Pages

  - Click on the Settings tab in this repository

  - Scroll down to the "GitHub Pages" section

  - From the "Source" drop down, select the master branch

  - Click Save

💥 The sample [GitHub Page](https://wycodebook.github.io/github-slideshow/#/)

3️⃣ Close an issue

Click the Close issue button at the bottom of the issue

4️⃣ Create a branch

  - Navigate to the Code tab

  - Click Branch: master in the drop-down

  - In the field, enter a name for your branch

  - Click Create branch: <name> or press the “Enter” key to create your branch

5️⃣ Commit a file

  - While on the branch you just created, click Create new file on the "Code" tab.

  - In the file name field, type `_posts/0000-01-02-YOUR-USERNAME.md`

  - When you’re done naming the file, add the following content to your file:

      {% highlight html %}
      ---
      layout: slide
      title: “Welcome to our second slide!”
      ---
      Your test
      Use the left arrow to go back!
      {% endhighlight %}

  - After adding the text, you can commit the change by entering a commit message in the text-entry field below the file edit view.

  - When you’ve entered a commit message, click Commit new file

6️⃣ Open a pull request

  - On the Code tab, click New pull request

  - In the base: drop-down menu, make sure the master branch is selected

  - In the compare: drop-down menu, select the branch you recently made your commit on

  - When you’ve selected your branch, enter a title for your pull request, for example

  - Add username's file

  - The next field helps you provide a description of the changes you made. Feel free to add a description of what you’ve accomplished so far. As a reminder, you have: created a branch, created a file and made a commit, and opened a pull request

  - Click Create pull request

7️⃣ Respond to a review

  - Click the Files Changed tab in this pull request

  - Click on the pencil (✏) icon found on the right side of the screen

  - Replace line 5 with something new

  - Scroll to the bottom and click Commit Changes.

8️⃣ Merge your pull request

  - Click Merge pull request

  - Click Confirm merge

  - Once your branch has been merged, you don't need it anymore. Click Delete branch.

## Completed Course!

![GitHub Course 1 Completed](/pic/GHcourse1.PNG)
