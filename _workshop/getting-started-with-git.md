---
title: Getting Started     # The title of the page
date: 0000-01-02    # Page order is set by date
---

When we use Git on a new computer for the first time, we need to configure a few things.
* our name and email address
* what our preferred text editor is
* and that we want to use these settings globally (i.e. for every project)

On a command line, Git commands are written as `git verb options`, where `verb` is what we actually want to do and `options` is additional  information which may be needed for the verb.

Open __Git Bash__ from wherever you installed it. There is a GUI for Git and you may have installed it but for this lesson we will be working mostly in the command line.

First we’ll configure your name and email address.
```
git config --global user.name "<username>"
git config --global user.email "<email address>"
```

This user name and email will be associated with your subsequent Git activity. Any changes pushed to GitHub or another Git host server after this lesson will include this information. In this lesson, we will be interacting with GitHub and so __*the email address used should be the same as the one used when setting up your GitHub account*__.

---
📌 __Keeping your email private__: If you are concerned about privacy, you can read [here](https://github.blog/2017-04-11-private-emails-now-more-private/) how to keep your email address private.

📌 __Line endings__: As with other keys, when you hit Return on your keyboard, your computer encodes this input as a character. Different operating systems use different character(s) to represent the end of a line. (You may also hear these referred to as newlines or line breaks.) Because Git uses these characters to compare files, it may cause unexpected issues when editing a file on different machines. Though it is beyond the scope of this lesson, you can read more about this issue in the [Pro Git book](https://www.git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_core_autocrlf).


📌 __Text editors__: We'll be working within our Git Bash window for most of this lesson but for some operations Git needs to open an associated text editor. _Vim_ is the default on most installs. If you haven’t used Vim before and wish to exit a session without saving your changes, press `Esc` then type `:q!` and hit `Return`. If you want to save your changes and quit, press `Esc` then type `:wq` and hit `Return`.

Or we can also set our favorite text editor if you didn't select one on your Git install:

| __Editor__                         | __Configuration command__                                                                                                |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Atom                               | $ git config --global core.editor "atom --wait"                                                                          |
| Nano                               | $ git config --global core.editor "nano -w"                                                                              |
| Notepad (Win)	                     | $ git config --global core.editor "c:/Windows/System32/notepad.exe"                                                      |
| Notepad++ (Win, 64-bit install)    | $ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin" |
| Sublime Text (Win, 64-bit install) | $ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"                                |
| Vim                                | $ git config --global core.editor "vim"                                                                                  |
| Visual Studio Code                 | $ git config --global core.editor "code --wait"                                                                          |

I use atom so I will switch to that:
```
$ git config --global core.editor "atom --wait"
```

📌__Shell Commands__: As well as Git commands we’ll be using some shell commands in this lesson:
* `pwd` (print working directory) is useful to orient yourself
* `cd` (change directory) on its own will get you to your home directory
* `mkdir` (make directory)

We have a cheat sheet pdf with more shell and git commands [here](./assets/pdfs/gitcheatsheet.pdf)

---

So let's get started with Git! Go to your desktop and make a folder called _gitlesson_. (It doesn’t matter where you go, as long as you know!). Then move into that folder you have created.
```
$ cd ~/desktop
$ mkdir gitlesson
$ cd gitlesson
```

We can check if there is anything in our folder using `ls` which lists the contents of the directory you’re in
```
$ ls
```

We have an empty folder.  We will create an empty Git repository using our first Git command `git init` (short for _initialise_)
```
$ git init
  Initialized empty Git repository in <your file path>/gitlesson/.git/
```

When we use Git via the command line, we preface each command with git, so that the computer knows we are trying to get Git to do something, rather than some other program.

We’ll do a couple more shell commands now to see what has happened

```
$ ls 			
```
Our folder still shows as empty. If we add the `-a` flag to the `ls` command it will include hidden files, which the .git folder is.
```
$ ls –a
  .	..	.git
```
Now the response includes the .git folder is. That is where all of the revision history for this repository will live)

Now that our folder is a Git project we can check its current status (we’ll be doing this a lot).
```
$ git status
  On branch master
  Initial commit
  Nothing to commit
``` 
