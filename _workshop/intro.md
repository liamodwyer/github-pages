---
title: Introduction to Github     # The title of the page
nav: Intro
date: 0000-01-02    # Page order is set by date
---

## Git, GitHub, & GitHub Pages

Before we get started, let's clarify some terms:

[Git]<(https://git-scm.com/) is a popular [free](https://www.gnu.org/philosophy/free-sw.en.html), [distributed version control](https://en.wikipedia.org/wiki/Distributed_version_control) system--i.e. a piece of software used to track the history of changes in a folder of files. 
Git can be used on your personal computer, or by online services to track the development of a project, such as...

[GitHub](https://github.com/), a popular web platform for hosting Git repositories--i.e. a place to store and sync your project files online.
Think of it as Google Drive for code with super robust "track changes" baked in.
Built around the powerful version control of Git, it provides a handy web interface for managing, editing, and collaborating on repositories.

Originally designed to manage large open-source software projects, GitHub's use has expanded to many other types of organizations and individuals, with [over 40 million users](https://octoverse.github.com/).
GitHub provides a bunch of built in project management features including...

[GitHub Pages](https://pages.github.com/), free static web hosting service available as part of every repository--this means with the *click of a button* you can fire up a new website!

Intended to host relatively simple sites for your GitHub portfolio or project documentation,
GitHub Pages is an ideal solution for creating an open educational resource or personal site to highlight your academic work. 
Because hosting through gh-pages is free and builds valuable transferable skills, this is a great option for teaching and learning.
Users have the opportunity to become creators and participants in global digital culture, developing critical digital literacy about the fabric of the web.

Many organizations and individuals are using GitHub to collaboratively create and publish public websites. 
For example, [Programming Historian](http://programminghistorian.org/), [The Carpentries](https://carpentries.org/), or this site!


There are *soft* limits and guidelines for gh-pages usage: sites should be < 1GB, use < 100GB bandwidth per month, and make < 10 builds per hour.
If your site exceeds these quotas, GitHub will send you a notice asking you to modify the repository.

All content must follow the [community guidelines](https://help.github.com/articles/github-community-guidelines/), e.g. no violence, obscene sex, or illegal stuff.


----------------

## GitHub Practice

Let's create a new repository, then write some Markdown and HTML to see how gh-pages works.

### Create a New Repository 

- Log into [GitHub](https://github.com/).
- Click the "+" plus icon in the upper right of the nav bar.
- Select "New repository".
- Fill in "Create a new repository" page:
    - "Owner" is you. Every repo is associated with an individual or organization.
    - "Repository name" is what you want to call this repo. It must be unique among the owner's repos. Since this repository will become a website, use all lowercase, no spaces, and no weird characters. Dash (`-`) or underscore (`_`) are okay.
    - "Public" / "Private". Anyone can visit a public repository--but that's okay! The entire web is public, so once you create a website, the code of your website is public anyway. GitHub is mostly open source code, i.e. public repositories with code people can view and copy for free (following the [license](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/licensing-a-repository) applied by the owner).
    - Check the "Add a README file" option. This makes it easier to get started.
- Finally, click the green "Create repository" button. You will be redirected to your brand new repository!

Take a minute to explore your new repository.
It currently contains one file, `README.md` that was automatically added. 
Check out the ["Issues" tab](https://guides.github.com/features/issues/), a great feature for starting conversations and tracking tasks related to the repository.

### Activate GitHub Pages

- Click the "Settings" tab.
- Scroll down to the "GitHub Pages" section.
- Under "Source", use the dropdown to select "main" branch and leave folder as "/ (root)".
- Click "Save".

GitHub Pages now allows *any* branch's root or "docs" folder to be [selected as the source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site). 
Following earlier conventions, creating a branch named `gh-pages` will automatically active it as the source. 

Keep in mind that until recently the default branch was called "master", rather than "main", so older documentation may still use that terminology. 


### README, Markdown, and Editing Intro

You will notice that by default the contents of the `README.md` file are displayed on the home page of your repository. 
This is a convention used in many code projects--README is a place to write the basics *about* your repository so users will understand what it contains, who made it, and any other information they should know. 
On GitHub READMEs are usually written in Markdown (thus the `.md` extension). 

Markdown is a standard to simplify writing content for the web designed to be easy to read and write. 
[GitHub Markdown Flavor](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax) can be used any where on GitHub to format your writing in comments, Issues, and `.md` files.
The basics are intuitive, much like formatting a plain text email, as can be seen in the [Mastering Markdown Guide](https://guides.github.com/features/mastering-markdown/).

Edit your README using Markdown:

- On your repo home page click the filename "README.md", which will bring you to the page for that file.
- On the upper right corner of the file click the "pencil" icon to start editing. This will open the web-based text editor.
- Edit your file:

```
# Heading One

## Heading Two

### Heading Three, etc.

Any text with no empty lines between will become a paragraph.
Leave an blank line between headings and paragraphs.
Font can be *Italic* or **Bold**.
Code can be highlighted with `backticks`.

Hyperlinks look like this [GitHub Help](https://help.github.com/).

A bullet list is created using `*`, `+`, or `-`, like:

- dog
- cat
- muffin

A numbered list is created using a number + `.`, like:

1. one
2. two
6. three
2. four

```

- When done editing, scroll to the bottom of the page to the "Commit changes" section. Commit is a git concept--basically taking a snap shot of the changes that will be permanently stored in your repository's history. Every commit records a user name, email, and message. 
- Fill in the first text box with your "commit message", i.e. a short description of what changes you have made. This is your message to the future to help understand the code.
- Click the green "Commit changes" button to complete your first `git commit`!

Once you commit, you will immediately see your README's updated content rendered on the page.
Behind the scenes GitHub is converting your Markdown code into HTML for display. 

### HTML, Index.html, and Create File Intro

Most of the Web is made up of HTML, CSS, and JS:

- **HTML** (Hypertext Markup Language) provides the structure and content, via a formal syntax for "tagging" the elements of a page such as headings, paragraphs, or lists.
- **CSS** (Cascading Style Sheets) provides the style.
- **JS** (JavaScript) provides the interactivity.

When you access a website, the server sends your computer the code which your browser renders into a web page that you can view and interact with.
Thus, one fascinating aspect of the web is that everyone must share code to participate.


<div class="row">
<div class="col-md-4 mb-2"><img class="img-fluid" src="{{ '/images/viewsource.png' | relative_url }}" alt="content menu with viewsource option"></div>
<div class="col-md-8" markdown="1">

Right click on any web page and select View page source to see the code that is being rendered by the browser (shortcut: `Ctrl + U`). 
Right click on any element in the page and select "Inspect" or "Inspect Element" to open your browser's built in developer tools.

This is a great way to learn about HTML and to understand how others created the sites you use.

To review the basic building blocks of the web, next let's create an HTML file. 
We will start with an index.html file because by default the server provides index as the home page of your site.

- Click the "Code" tab to go to your repository's home page.
- Click the "Add file" button and select "Create new file". This will open the web-based text editor.
- Type in the name for your file: `index.html`.
- Put your cursor in the editor and write some HTML:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Example Title - appears in browser tab</title>
    </head>
    <body>
        <h1>Header One: Big Text</h1>
        <p>An example paragraph.</p>
        <h2>Header Two</h2>
        <p>Paragraph with <strong>Bold text</strong>.</p>
        <p>A link to <a href="https://github.com">GitHub</a>.</p>
    </body>
</html>

```

- When done editing, scroll to the bottom of the page to the "Commit changes" section. 
- Fill in your "commit message" and click the green "Commit changes" button.

After you commit, you will be redirected to your repo home page.
Clicking on the word "commits" in the upper right of the file box will bring you to the history of your repository. 
Each commit is represented on the page displaying your commit messages. 
Clicking on the *hash* (the series of numbers to the right of the commit message) will display all the information about the commit, including all the changes made to files. 

Now that we have an `index.html`, let's visit our new website. 
The URL for any GitHub Pages site follows the pattern: 

`https://username.github.io/repositoryname/`

You can also find the link by looking back in your Settings once gh-pages has been activated.

Each time you make a commit GitHub Pages will re-deploy your files, which might take a minute. 
Once it is complete (assuming everything goes well!), a green check will appear next to your commit in the history.

-------------

Git & GitHub:

- [GitHub Guides](https://guides.github.com/), see [Hello World](https://guides.github.com/activities/hello-world/) for an introduction.
- [GitHub Learning Lab](https://lab.github.com/)

Markdown:

- [Mastering Markdown GitHub Guide](https://guides.github.com/features/mastering-markdown/)
- [GitHub Markdown documentation](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)
- [Markdown and Pandoc for Academic Writing](https://evanwill.github.io/write-md/)
- [Markdown](https://daringfireball.net/projects/markdown/) (original spec by John Gruber)

HTML:

- [w3schools HTML Tutorial](https://www.w3schools.com/html/default.asp)
- [HTML Basics, MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)
- [Web Crash Course!](https://evanwill.github.io/web-crash-course/)


--------------------

When we use Git on a new computer for the first time, we need to configure a few things.
* our name and email address
* what our preferred text editor is
* and that we want to use these settings globally (i.e. for every project)

On a command line, Git commands are written as `git` `verb` `options`, where `verb` is what we actually want to do and `options` is additional  information which may be needed for the verb.

Open __Git Bash__ from wherever you installed it. There is a GUI for Git and you may have installed it but for this lesson we will be working mostly in the command line.

#### Account setup:
First we’ll configure your __name__ and __email address__.
```
git config --global user.name "<username>"
git config --global user.email "<email address>"
```

This user name and email account will be associated with your subsequent Git activity. Any changes pushed to GitHub or another Git host server after this lesson will include this information. In this lesson, we will be interacting with GitHub and so __*the email address used should be the same as the one used when setting up your GitHub account*__.

📌 __Keeping your email private__: If you are concerned about privacy, you can read [here](https://github.blog/2017-04-11-private-emails-now-more-private/) how to keep your email address private.

#### Branch naming:
All file changes are associated with a “branch.” For now, it’s enough to know that branches exist. By default, Git creates a branch called `master` when you create a new repository with `git init` (as explained in the next Episode).

In 2020, most Git code hosting services transitioned to using `main` as the default branch. Any new repository in GitHub and GitLab defaults to `main`. However, Git has not yet made the same change. To change the default on Git to match, enter the following command:

```
$ git config --global init.defaultBranch main
```

Note that if this value is unset in your local Git configuration, the init.defaultBranch value defaults to master. You can check your settings at any time:

```
$ git config --list
```
---

📌 __Line endings__: As with other keys, when you hit Return on your keyboard, your computer encodes this input as a character. Different operating systems use different character(s) to represent the end of a line. (You may also hear these referred to as newlines or line breaks.) Because Git uses these characters to compare files, it may cause unexpected issues when editing a file on different machines. Though it is beyond the scope of this lesson, you can read more about this issue in the [Pro Git book](https://www.git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_core_autocrlf).

You can change the way Git recognizes and encodes line endings using the core.autocrlf command to git config. The following settings are recommended:

* On macOS and Linux:
   ```
   $ git config --global core.autocrlf input
   ```
* And on Windows:
   ```
   $ git config --global core.autocrlf true
   ```

📌 __Text editors__: We'll be working within our Git Bash window for most of this lesson but for some operations Git needs to open an associated text editor. _Vim_ is the default on most installs.

If you haven’t used Vim before and wish to exit a session without saving your changes, press `Esc` then type `:q!` and hit `Return`. If you want to save your changes and quit, press `Esc` then type `:wq` and hit `Return`.

Or we can also set our favorite text editor if you didn't select one on your Git install:

| __Editor__                         | __Configuration command__                                                                                                |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Atom                               | $ git config --global core.editor "atom --wait"                                                                          |
| Nano (Mac)                         | $ git config --global core.editor "nano -w"                                                                              |
| Notepad (Win)	                     | $ git config --global core.editor "notepad"                                                                              |
| Notepad++ (Win, 64-bit install)    | $ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin" |
| Sublime Text (Win, 64-bit install) | $ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"                                |


I use atom so I will switch to that:
```
$ git config --global core.editor "atom --wait"
```

📌 __Shell Commands__: As well as Git commands we’ll be using some shell commands in this lesson:
* `pwd` (print working directory) is useful to orient yourself
* `cd` (change directory) on its own will get you to your home directory
* `mkdir` (make directory)

We have a cheat sheet pdf with more shell and git commands [here](./assets/documents/GitCheatSheet.pdf)

---

### Creating a repository

A Git _repository_ is a data structure used to track changes to a set of project files over time.

Repositories are stored within the same directory as these project files, in a hidden directory called `.git`. We can create a new git repository either remotely via our GitHub account, or locally via the command line. Let’s use the command line.

* First, we will create a new directory for our project and enter that directory.
* Go to your desktop and make a folder called _gitlesson_. (It doesn’t really matter where, as long as you know, but if you are not familiar with shell commands then desktop is easiest).
* Then move into that folder you have created.
```
$ cd ~/desktop
$ mkdir gitlesson
$ cd gitlesson
```
We can check if there is anything in our folder using `ls` which lists the contents of the directory you’re in
```
$ ls
```

We have an empty folder.  Now create an empty Git repository using `git init` (short for _initialise_)
```
$ git init
  Initialized empty Git repository in <your file path>/gitlesson/.git/
```

📌 _When we use Git via the command line, we preface each command with `git`, so that the computer knows we are trying to get Git to do something, rather than some other program._

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
  On branch main
  Initial commit
  Nothing to commit
```
If yours shows branch `master` enter the following command to switch it to `main`. This will be important later.
```
git checkout -b main
```

***
#### 💡 Key Points:

✅ Use `git config` with the `--global` flag to configure user name, email address, editor once per machine

✅ `git init` initializes a repository

✅ Git stores all of its repository data in the `.git` directory
