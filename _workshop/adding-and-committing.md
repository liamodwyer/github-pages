---
title: Adding and Committing     # The title of the page
date: 0000-01-03    # Page order is set by date
---

We will create a new file so that we can add it. We'll make a `.md` file which is _markdown_ format, a lightweight markup language (like a very stripped- back version of html). Markdown can be used with git and github to build web pages and websites. We'll use another shell command (`touch`) to create the empty file.
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
Git has spotted the new changes to our file, but we haven’t staged (or _added_) them yet. Let's do that and then _commit_ it to our repository, which will be our first commit or snapshot. When we use the 'commit' command we have to add a message, signified by the `-m` flag. These commit messages should be meaningful so that they can be recognised as a point in time of a file or project, should we wish to roll back to it.
```
$ git add article.md
$ git commit -m 'Add initial version of article'
```
Now if we do a _git status_ we should see everything is up to date:
```
$ git status
  On branch master
  Nothing to commit, working tree clean  
```
We can check our repository history using `git log`. Let's make a new entry to our `article.md` file. We can use `>>` to append content (rather than overwrite)
```
$ echo "### Introduction" >> article.md
```
No do a `git status` and see if git recognises that a change has been made.
If we want to see what the changes or differences are we can do that by using another git command, `git diff`
```
$ git diff
  diff --git a/article.md b/article.md
  index aed0629..989787e 100644
  --- a/article.md
  +++ b/article.md
  @@ -1 +1,2 @@
   Some text here
   +Some new text here
```
It’s a little cryptic as it’s meant for text editors but we’ll go through it to see what it is saying.
1.	The first line tells us that Git is producing output similar to the Unix diff command comparing the old and new versions of the file.
2.	The second line tells exactly which versions of the file Git is comparing; df0654a and 315bf3a are unique computer-generated labels for those versions.
3.	The third and fourth lines once again show the name of the file being changed.
4.	The remaining lines show us the actual differences and the lines on which they occur. In particular, the + marker in the first column shows where we added a line.

We’ll go ahead and try and commit this.

```
$ git commit –m ‘Add section header’
```
This gives an error because we have forgotten to `add` the file update first. You have to add or stage a change before you can commit it. This can seem slow or clunky but it can be more efficient as it enables us to select and group changes. We don’t have to commit everything if we don’t want to include all our current draft files. So `git add` specifies what will go in a snapshot but `git commit` takes the snapshot.
```
$ git add article.md
```
Once we have ‘staged’ it we can now commit it to our repository
```
$ git commit –m ‘Add section header’
```
If we want to check we are up to date can go `git diff`
So let’s go through that again of
* making a change
* staging that change  
* and then committing that change

Instead of using echo again we are going to open atom - this time just as a text editor - we’ll come back to our git command line in a minute. So
```
$ echo "First line of my intro" >> article.md
$ git diff
$ git add article.md
```
If we stop at this point and try `diff` again...
```
$ git diff
```
We see no difference. This is because `diff` compares working directory to staging area (not to repository). To compare staged content to the last committed change use the -`--staged` flag
```
$ git diff --staged
```
We will now commit our latest change
```
$ git commit –m ‘Add intro text’
```
Let'ss look at the _log_ now it should be a bit more detailed (it will show three changes)
```
$ git log
```
Git presents the log with most recent first. Some other options or arguments for the `git log` command are `git log –-oneline` and `git long -2` (just shows the last 2 commits).

We’ve done a lot of adding and committing. Let’s look at how we can retrieve old versions. You can see in the `git log` each commit has its own hash identifier. You can refer to the _most recent commit_ of the working directory by using the identifier `HEAD`. And earlier versions with `HEAD~1` or `HEAD~2` etc. Before we start, let’s make one more change to `article.md`, adding yet another line.
```
$ echo “an ill-considered change” > article.md
$ cat article.md
$ git restore article.md
```
if I make the same mistake but go further and `add` the file this is what I would do to retrieve the repository version
```
$ git checkout HEAD article.md
```
If we had actually commited that wrong copy to the repo we could use `HEAD~1` to retrieve the earlier version. Let’s go back and make the same error and `add` and `commit` it. Then do: 
```
$ git checkout HEAD~1 article.md
```
(We have to commit this back if we want that to be the new HEAD)
