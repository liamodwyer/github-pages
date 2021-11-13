---
title: Getting Started     # The title of the page
date: 0000-01-02    # Page order is set by date
---

Open Git Bash. First we’ll configure your name and email address.
`$ git config` --global user.name “<username>"		configure your user name
`$ git config` --global user.email “<email address>"	# configure your user email
Configure the default text editor git uses (for example, when prompting for a commit message).
`$ git config --global core.editor "atom"` what about this
`$ pwd` 	is useful to orient yourself
`$ cd` 	will get you to your home directory.
`$ cd ~/desktop` to go to your desktop. It doesn’t matter where you start from for this lesson
`$ cd gitlesson`	create a subfolder gitlesson. We can check if there is anything in our folder.
`$ ls` 	lists the contents of the directory you’re in We have an empty folder.  We are going  to create an empty git repository using our first git command `git init` (short for initialise)
`$ git init`	When we use git via the command line, we preface each command with git, so that the computer knows we are trying to get git to do something, rather than some other program. We’ll do a couple more shell commands now to see what has happened
`$ ls` 			(lists files in the directory you are in)
`$ ls –a`		(includes hidden files – which the .git folder is. That is where all of the revision history for this repository will live)
Now that it’s a git project we can check its current status (we’ll be doing this a lot)
`$ git status`
On branch master
Initial commit
Nothing to commit 
