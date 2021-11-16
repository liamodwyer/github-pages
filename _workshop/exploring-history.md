---
title: Exploring History     # The title of the page
date: 0000-01-04    # Page order is set by date
---

As we saw in the previous episode, we can refer to commits by their identifiers. You can refer to the most recent commit of the working directory by using the identifier `HEAD`.

We’ve been adding one line at a time to `gitlesson.md`. It’s easy to track our progress by looking, so let’s do that using our HEADs. Before we start, let’s make a change to gitlesson.md, adding yet another line.

Before we start, let’s make one more change to `article.md`, adding yet another line.

```
$ echo “an ill-considered change” > article.md
$ cat article.md
```
Oops! Using `>` rather that `>>` is a mistake and overwrites the other file content!!

Let's say I didn't realise this and I `add` the corrupted version:
```
$ git add aricle.md
```
If I now realise what I've done, I can retrieve the most recent commit from my repository using `HEAD` and `checkout`.
```
$ git checkout HEAD article.md
```
As you might guess from its name, `git checkout` checks out (i.e., restores) an old version of a file. In this case, we’re telling Git that we want to recover the version of the file recorded in HEAD, the last saved commit.

If we had actually committed that wrong copy to the repo we would want to recover the previous commit to the latest one. We use `HEAD~1` to do that. Let’s go back and make the same error and `add` and `commit` it. Then do:
```
$ git checkout HEAD~1 article.md
```
📌 `Checkout` brings this version back to the staged area, so we now have to re-commit this restored version back if we want that to be the new HEAD
```
$ git commit article.md
```

📌 We can refer to any previous commits using the ~ notation, so HEAD~1 means “the previous commit”, while HEAD~123 goes back 123 commits from where we are now.

📌 Another way to go back to earlier versions is to use the identifier that we see from the `log` or `diff` commands.


📌 __*The Staging Area*__

If you think of Git as taking snapshots of changes over the life of a project, `git add` specifies what will go in a snapshot (putting things in the staging area), and `git commit` then actually takes the snapshot, and makes a permanent record of it (as a commit). If you don’t have anything staged when you type `git commit`, Git will prompt you to use `git commit -a` or `git commit --all`, which is kind of like gathering everyone to take a group photo! However, it’s almost always better to explicitly add things to the staging area, because you might commit changes you forgot you made. (Going back to the group photo simile, you might get an extra with incomplete makeup walking on the stage for the picture because you used -a!) Try to stage things manually, or you might find yourself searching for “git undo commit” more than you would like!

<p align="center">
  <img src="./assets/images/git-staging-area.svg">
</p>



***
#### 💡 Key Points:

✅ `git status` shows the status of a repository.

✅ Files can be stored in a project’s working directory (which users see), the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).

✅ `git add` puts files in the staging area.

✅ `git commit` saves the staged content as a new commit in the local repository.

✅ write a commit message that accurately describes your changes.
