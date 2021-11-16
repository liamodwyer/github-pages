---
title: Sharing with Github     # The title of the page
date: 0000-01-05    # Page order is set by date
---

So we’ve done a lot on Git. We’re now going to look at how along with Git to preserve and record your own work, we can use Github to share that - including all its recorded changes. This can enable group collaboration or give you a stable way to work from two different machines.

Open Github and login to the account you have created. Create a new repository on Github, give it the name _gitlesson_. For now don’t add a `readme.md` or `.gitignore` file just click `Create repository`

Connect your local repo to the Github repo (at the moment they don’t know anything about each other). Copy the Github repo url and then go back to our Git Bash window.

```
$ git remote add origin https://github.com/liamodwyer/gitlesson.git
```
[_origin_ in the `git remote add` line is a short alias we’re giving to that long repository URL. It could be anything, but by convention in Git, it is usually called `origin`]
```
$ git remote –v
```
Now we have established a connection but we haven’t synchronised the content. To send our content from the local to the remote we use the Git push command

### Pushing Changes

We ‘push’ our local changes to the Github repo. You will be prompted for your Github login during this process.

```
$ git push –u origin master		
  Counting objects: 3, done.
  Writing objects: 100% (3/3), 226 bytes | 0 bytes/s, done.
  Total 3 (delta 0), reused 0 (delta 0)
  To https://github.com/<your_github_username>/gitlesson
  * [new branch]      master -> master
  Branch master set up to track remote branch master from origin.
```
Go to Github and refresh. We have the file and we also have the commit history

We’ll just check that we are up to date with our remote (now that we have a remote, `git status` output includes that info). If we had made changes from elsewhere (or someone else had) which caused the remote/Github content to be ahead of our local version, we might want to bring the Github content into our local repository. To do that we use `git pull`
```
$ git pull origin master
```
(but this will say they are up to date)

### Pulling Changes

So now we have gone as far as we go in one direction...
* we created content in a working directory
* we staged that content
* we committed it to the local repository
* now we have pushed that repository to a remote Github repository

So just to show that we can work in the other direction too, where the Github repository becomes the _source_, we will create a separate _laptop_ folder and imagine that this could be a second device you want to be able to manage this project from.
```
$ cd ~/desktop
$ mkdir laptop
$ cd laptop
$ git clone https://github.com/liamodwyer/gitlesson.git
$ ls 					(to show that the gitlesson directory is now there)
$ cd gitlesson 			(to move into that repository)
```
So we have essentially an up-to-date repository in three places - two separate Git repositories and one on Github.

The image below shows the commands and workflow we have implemented in this lesson using Git and Github:

<p align="center">
  <img src="./assets/images/gitlocalremote.jpg">
</p>

* creating files in the working directory
* adding them to the staging area
* committing them to the local repository
* checking out files from the repository back to the working directory
* pushing the directory and files to a remote repository
* pulling from that remote repository to another local repository

---

#### 💡 Key Points:

✅ A local Git repository can be connected to one or more remote repositories

✅ `git push` copies changes from a local repository to a remote repository.

✅ `git pull` copies changes from a remote repository to a local repository.
