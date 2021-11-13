---
title: Adding and Committing     # The title of the page
date: 0000-01-03    # Page order is set by date
---

We will create a new file so that we can add it. `touch` is a quick way to create an empty file. We will create a `.md` file which is a _markdown_, a lightweight markup language (like a very stripped- back version of html). Markdown can be used with git and github to build web pages and websites.
```
$ touch article.md
```
Let's check that that has worked and we have in fact created an empty file.
```
$ ls
  article.md
```
We'll check our status again to see what it tells us.
```
$ git status
  On branch master
  Initial Commit
  Untracked files
```
Git has noticed the new file. But it calls it an untracked file. We’ll add it as it tells us we should.
```
$ git add article.md
```
Let’s add some content to our empty `article.md` file. We can add content from the command line combining `echo` and `>` which directs the content to whatever we put after the `>`. We'll use the `cat` to check that the output has been written to the file.
```
$ echo “# How To Use Git to Manage Your Writing Project” > article.md
$ cat article.md
$ git status  	
  On branch master
  Initial commit
  changes to be committed
  new file: article.md
  Changes not staged for commit
  modified: article.md
```
