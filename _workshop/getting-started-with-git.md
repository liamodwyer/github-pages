---
title: Getting Started     # The title of the page
date: 0000-01-02    # Page order is set by date
---

Open Git Bash.
First we’ll configure your name and email address.
```
$ git config --global user.name "<username>"
$ git config --global user.email "<email address>"
```

Configure the default text editor git uses (for example, when prompting for a commit message).
```
$ git config --global core.editor "atom"
```

As well as git commands we'll be using some shell commands in this lesson:
* `pwd` (print working directory) is useful to orient yourself
* `cd` (change directory) on its own will get you to your home directory
* `mkdir` (make directory)

Go to your desktop and make a folder called gitlesson. (It doesn’t matter where you go, as long as you know!). Then move into that folder you have created.
```
$ cd ~/desktop
$ mkdir gitlesson
$ cd gitlesson
```

We can check if there is anything in our folder using `ls` which lists the contents of the directory you’re in
```
$ ls
```

We have an empty folder.  We will create an empty git repository using our first git command `git init` (short for _initialise_)
```
$ git init
$ Initialized empty Git repository in <your file path>/gitlesson/.git/
```

When we use git via the command line, we preface each command with git, so that the computer knows we are trying to get git to do something, rather than some other program.

We’ll do a couple more shell commands now to see what has happened

```
$ ls 			
```
Our folder still shows as empty. If we add the `-a` flag to the `ls` command it will include hidden files, which the .git folder is.
```bash
$ ls –a
```
Now the response includes the .git folder is. That is where all of the revision history for this repository will live)

Now that it’s a git project we can check its current status (we’ll be doing this a lot)
* `$ git status`
  * `On branch master`
  * `Initial commit`
  * `Nothing to commit` 
