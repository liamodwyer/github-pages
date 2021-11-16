---
title: Exploring History     # The title of the page
date: 0000-01-04    # Page order is set by date
---

As we saw in the previous episode, we can refer to commits by their identifiers. You can refer to the most recent commit of the working directory by using the identifier `HEAD`.

We’ve been adding one line at a time to `article.md`. We can track our progress in different ways but let’s do it using `HEAD`. Before we start, let’s make a further change to `article.md`, adding yet another line.

```
$ echo “an ill-considered change” > article.md
$ cat article.md
```
Oops! Using `>` rather that `>>` is a mistake and overwrites the other file content!!

Let's say I didn't realise this and I `add` the corrupted version:
```
$ git add article.md
```
If I now realise what I've done, I can retrieve the most recent commit from my repository using `HEAD` and `checkout`.
```
$ git checkout HEAD article.md
```
As you might guess from its name, `git checkout` checks out (i.e. restores) an old version of a file. In this case, we’re telling Git that we want to recover the version of the file recorded in HEAD, the last saved commit.

If we had actually committed that wrong copy to the repo we would want to recover the last-but-one commit. We can use relative syntax of `HEAD~1` to do that. Let’s go back and make the same error and `add` and `commit` it. Then do:

```
$ git checkout HEAD~1 article.md
```

📌 `Checkout` brings this version back to the staged area and working directory, so we now have to re-commit this restored version back if we want that to be the most recent commit.

```
$ git commit article.md
```

📌 The ~ notation used above can be used for all earlier commits, so HEAD~1 means “the previous commit”, while HEAD~123 goes back 123 commits from where we are now.

📌 Another way to call earlier versions is to use the commit identifier which can be retrieved from various commands like `git log`, `git diff` or `git show`.

📌 There are other commands or methods to undo or revert to earlier versions. [This tutorial](https://www.atlassian.com/git/tutorials/undoing-changes) gives a good overview of undo methods. For the situation above, `git revert` would be quicker to fix the issue, but the concepts of `checkout` and `HEAD` are quite important in Git so it is good to cover them here.

📌 The fact that files can be reverted one by one tends to change the way people organize their work. If everything is in one large document, it’s hard (but not impossible) to undo changes to the introduction without also undoing changes made later to the conclusion. If the introduction and conclusion are stored in separate files, on the other hand, moving backward and forward in time becomes much easier.

```
$ git show HEAD~3 article.md
```

Typically we might use one of these commands to get the identifier or make sure it is the version we want.  Git lets us use just the first few characters (typically seven for normal size projects) when we are using them in commands.

***
#### 💡 Key Points:

✅ `git diff` displays differences between commits.

✅ `git checkout` recovers old versions of files.
