---
layout: post
title: "Migrating your repository to GitHub"
date: "2018-08-24 20:08:55 -0700"
tags: [GitHub Learning Lab Course]
---

GitHub Learning Lab Course 4

🔍 [Step 1](#step-1) 🔍 [Step 2](#step-2) 🔍 [Step 3](#step-3) 🔍 [Step 4](#step-4)

---

This course helps you seamlessly migrate a project using GitHub's importer tool. Along the way, we will also discuss important steps for preparing and sharing your project.

In this course, you’ll learn how to:

  - Prepare your project for a successful migration

  - Handle any binary files currently stored in your project

  - Create important Git files like a `.gitignore`

  - Import your project to GitHub

## Step 1: Plan the migration

Migrating your repository to GitHub gives you the feature-rich tools and collaboration needed to elevate your project to the next level. This course will guide you through the necessary steps to migrate your repository from another version control system to GitHub.

#### Important considerations for migrations

If you are moving from another version control system such as Mercurial, Subversion, or another Git platform, you will need to make a few decisions:

  1. Do you need all of the history?

  2. Is there project data that lives outside of the history you need to preserve? (ex: Issues, Discussions, Pull Requests)

#### Should you keep all of the history?

If you are moving your project to GitHub as a public project, you may want to consider what is in your history. For example:

  - Is there sensitive information in historical commit 📖 messages?

  - Do you want to use [private email addresses](https://help.github.com/articles/setting-your-commit-email-address-on-github/) on GitHub?

![Course 4](/pic/GH4.PNG)

#### Should you keep non-Git data?

Mapping users, keeping commit comments, and other data migrations are more complex, but not impossible. For most version control systems there are helpful Open Source 📖 tools available. Here are a few resources:

  - [GitHub's documentation on importing from other VCS](https://help.github.com/enterprise/2.12/admin/guides/migrations/importing-data-from-third-party-version-control-systems/)

  - [Blog post about GitHub Migrator tool](https://blog.github.com/2016-02-11-migrate-your-code-with-the-github-importer/)

#### Activity: Next steps

Different situations...

- Using the GitHub Importer

  GitHub has a terrific import tool that will allow you to import your repository in just a few minutes.

  First, let's make sure your repository 📖 is Git friendly. Close this issue and I will open a new issue with next steps.

- Doing a clean cutover

  To do a clean cutover, you will need to remove the existing history. Some people like to save a back up of the project with the history. To start the process:

  1. Download a copy of the project to your local machine.

  2. Remove version control (with Git this is as simple as running `rm` `-rf` `.git` inside the repository).

  3. Now that your project is local on your machine and you have removed any history being tracked by Git, the remaining steps in this course largely cover migrating that Git history.

- Migrating non-Git data

  These migrations are more nuanced and outside the scope of this course. I recommend you go through these steps with a simple repository so you can learn best practices and then apply them to your more complex migration.

  If you don't have a repository to use for this activity, you are welcome to use this one: https://github.com/githubtraining/github-move

## Step 2: Prepare the project

#### Working with Binary files

In general, there are two types of files: text files and binary files.

Text files, like most code files, are easily tracked with Git 📖 and are very lightweight.

However, binary files like spreadsheets, presentations with slides, and videos don't work well with Git. If your repository already has some of these files, it's best to have a plan in place before you enable Git version control.

You could choose to remove the binary files, or use another tool like [git-lfs](https://git-lfs.github.com/) (Git Large File Storage). We won't get into detail on how to set up [git-lfs](https://git-lfs.github.com/) in this course, but we will talk about .gitignore files next, which are key to protecting your code from becoming bloated with binaries.

#### Add a .gitignore

As we convert your project to a Git repository, it should only include the source code necessary to build or compile your project. In addition to avoiding binaries as we discussed above, you will also want to keep build artifacts out of your version controlled code.

To do this, you will create a file in your current project named `.gitignore`. Git will use the `.gitignore` to determine which files and directories should not be tracked under version control. The [.gitignore file](https://help.github.com/articles/ignoring-files/) is stored in your repository in order to share the ignore rules with any other users that interact with the repository.

Since the files to be ignored are dependent on the language you are using, the open source community has contributed some great templates for `.gitignore` files in the [github/gitignore](https://github.com/github/gitignore) repository.

#### Activity: Prepare your repository

  - Remove any binary files from your repository.

  - In your local environment, [create a `.gitignore`](https://help.github.com/articles/ignoring-files/) file. You can use a [template](https://github.com/github/gitignore) or create your own.

## Step 3: Private or Public?

You have one more decision to make before you migrate your code! Right now, your repository is set to public.

You can change the visibility of a repository to Private or Public at any time in your repository's Settings tab, but there are some things you should know.

#### Private Repositories

If your repository is private, the only people who can see your code are you and the collaborators 📖 you've invited.

There is a small charge associated with Private repositories, but if your project has sensitive information, it's worth it.

#### Public Repositories

In public repositories, anybody can see your code. Millions of open source repositories on GitHub are public, too!

Licenses, code of conduct, and other files are important when you create a public repository. There are many benefits to this, but it's also a large responsibility. Keep in mind that once a repository is public and open source, there are certain implications about keeping it public, depending on the license chosen.

It's important to note that public does not equal open source! The license associated with code determines whether or not it is open source.

## Step 4: Complete the Import

It's time for the big move! Since your source code is in Subversion, Mercurial, Team Foundation Server, or another Git repository, you can move it to GitHub using GitHub Importer. GitHub Importer doesn't bring over every piece of data, but it does bring the history. You can read more about GitHub Importer's capabilities [here](https://help.github.com/articles/about-github-importer/).

#### Activity: Import your project using GitHub Importer

  1. Copy the URL for your existing repository on Subversion, Mercurial, TFS, or another Git server

  2. Mavigate to the Code tab of this repository and scroll down to the section labeled …or import code from another repository

  3. Click Import code

  4. Paste the URL for your repository in its current location

  5. Click Begin import


![GitHub Course 4 Completed](/pic/GHcourse4.PNG)
