---
title: Tracking Changes     # The title of the page
date: 0000-01-03    # Page order is set by date
---

We will create a new file so that we can add it. We'll make a `.md` file which is _markdown_ format, a lightweight markup language (like a very stripped- back version of html).

📌 _Markdown can be used with git and github to build web pages and websites. We'll use another shell command `touch` to create the empty file._
```
$ touch article.md
```
Let's check that that has worked and we have in fact created an empty file:
```
$ ls
  article.md
```
We'll check our status again to see what it tells us:
```
$ git status
  On branch master
  Initial Commit
  Untracked files
```
Git has noticed the new file. But it calls it an _untracked_ file. We’ll _add_ it as it prompts us to and tell Git to track this file:
```
$ git add article.md
```
Let’s add some content to our empty `article.md` file.
📌 _We can do this from the command line combining `echo` and `>` which directs the content to whatever we put after the `>`. We'll use the `cat` to check that the output has been written to the file:_
```
$ echo “# How To Use Git to Manage Your Writing Project” > article.md
$ cat article.md
$ git status  	
  On branch main
  Initial commit
  changes to be committed
  new file: article.md
  Changes not staged for commit
  modified: article.md
```
So Git has spotted the new changes to our file, but we haven’t staged (or _added_) them yet. Let's do that and then _commit_ it to our repository, which will be our first commit or snapshot.

📌 _When we use the 'commit' command we have to add a message, signified by the `-m` flag. These commit messages should be meaningful so that they can be recognised as a point in time of a file or project, should we wish to roll back to it._
```
$ git add article.md
$ git commit -m 'Add initial version of article'
```
📌 _When we run `git commit`, Git takes everything we have staged using `git add` and stores a copy permanently inside the special `.git directory`. This permanent copy is called a commit (or revision) and has a unique hash or identifier which has a short and long version._

If we do a _git status_ we should see everything is up to date:
```
$ git status
  On branch main
  Nothing to commit, working tree clean  
```
We can check our repository history using `git log`. This lists all commits made to a repository in reverse chronological order. The listing for each commit includes the commit’s full identifier (which starts with the same characters as the short identifier printed by the git commit command earlier), the commit’s author, when it was created, and the log message Git was given when the commit was created.

Let's make a new entry to our `article.md` file. We can use `>>` to append content (rather than overwrite)
```
$ echo "### Introduction" >> article.md
```
Now do a `git status` to check if git recognises that a change has been made.
If we want to see what the changes or differences are we can do that by using another git command, `git diff`
```
$ git diff
  diff --git a/article.md b/article.md
  index aed0629..989787e 100644
  --- a/article.md
  +++ b/article.md
  @@ -1 +1,2 @@
   # How To Use Git to Manage Your Writing Project
  +### Introduction
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
Oops. This gives an error because we have forgotten to `add` the file update first. You have to add or stage a change before you can commit it.

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

> Git insists that we add files to the set we want to commit before actually committing anything. This allows us to commit our changes in stages and capture changes in logical portions rather than only large batches.
For example, suppose we’re adding a few citations to relevant research to our thesis. We might want to commit those additions, and the corresponding bibliography entries, but not commit some of our work drafting the conclusion (which we haven’t finished yet).

>To allow for this, Git has a special staging area where it keeps track of things that have been added to the current changeset but not yet committed.

📌 __Staging area__
If you think of Git as taking snapshots of changes over the life of a project, `git add` specifies what will go in a snapshot (putting things in the staging area), and `git commit` then actually takes the snapshot, and makes a permanent record of it (as a commit). If you don’t have anything staged when you type `git commit`, Git will prompt you to use `git commit -a` or `git commit --all`, which is kind of like gathering everyone to take a group photo! However, it’s almost always better to explicitly add things to the staging area, because you might commit changes you forgot you made. (Going back to the group photo simile, you might get an extra with incomplete makeup walking on the stage for the picture because you used -a!) Try to stage things manually, or you might find yourself searching for “git undo commit” more than you would like!

<p align="center">
  <img src="./assets/images/git-staging-area.svg">
</p>

Let’s watch as our changes to a file move from our editor to the staging area and into long-term storage. First, we’ll add another line to the file:
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
Let's look at the _log_ now it should be a bit more detailed (it will show three changes)
```
$ git log
```
Git presents the log with most recent first. Some other options or arguments for the `git log` command are `git log –-oneline` and `git long -2` (just shows the last 2 commits).

To recap, when we want to add changes to our repository, we first need to add the changed files to the staging area (git add) and then commit the staged changes to the repository (git commit):

<p align="center">
  <img src="./assets/images/git-committing.svg">
</p>

***
#### 💡 Key Points:

✅ `git status` shows the status of a repository.

✅ Files can be stored in a project’s working directory (which users see), the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).

✅ `git add` puts files in the staging area.

✅ `git commit` saves the staged content as a new commit in the local repository.

✅ write a commit message that accurately describes your changes.


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
