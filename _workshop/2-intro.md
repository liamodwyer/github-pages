---
title: Git, GitHub, & GitHub Pages     # The title of the page
nav: Git & Github
date: 0000-01-02    # Page order is set by date
---

We are just using Github Pages as a means to publish a website but before we begin with that let's briefly look at these things called Git, Github and Github pages and how they all inter-relate.

## Git
![Git Logo](https://upload.wikimedia.org/wikipedia/commons/6/62/Git-logo-orange.svg) 

[Git](https://git-scm.com/) is a [distributed version control](https://en.wikipedia.org/wiki/Distributed_version_control) system. That is, a piece of software used to track the history of changes in a file or a set of files. In Git, this set of files is known as a **_repository_**. 

> Git has its own terminology for various functions - *branching, forking, cloning* etc. - which can be a little off-putting if you haven't used it before. In this workshop we'll only deal with what we need to know for the purposes of creating our website. 

Git can be used locally, on your personal computer, or by online services to track the development of a project, such as...

## Github
![Github Logo](assets/images/github-logo.png)

[GitHub](https://github.com/), a popular web platform for hosting Git repositories--i.e. a place to store and sync your project files online.

Built around the powerful version control of Git, it provides a handy web interface for managing, editing, and collaborating on repositories.

Github was originally designed to manage large open-source software projects, but its use has expanded to many other types of organizations and individuals, with [over 40 million users](https://octoverse.github.com/).
GitHub provides lots of additional project management features and functionalities, one of which is...

## Github Pages
![Github Pages Logo](assets/images/githubPagesLogoSmall.png)
[GitHub Pages](https://pages.github.com/), is a free static web hosting service available as part of every repository. 

Initially designed for user blogs or project documentation but offers a good solution for open educational resources, research project sites or academic profiles.

Many organizations and individuals are using GitHub to collaboratively create and publish public websites. 
For example, [Programming Historian](http://programminghistorian.org/), [The Carpentries](https://carpentries.org/), or this site!


> There are *soft* limits and guidelines for gh-pages usage: 
> - site content < 1GB
> - < 100GB bandwidth per month
> - < 10 builds per hour
> If your site exceeds these quotas, GitHub will send you a notice asking you to modify the repository.

> All content must follow the [community guidelines](https://help.github.com/articles/github-community-guidelines/), e.g. no violence, obscene, or illegal stuff.

-----------------

# Practice Time!

Let's create a new repository, then write some Markdown to see how github pages works.

### 1. Create a New Repository 

- Log into [GitHub](https://github.com/).
- Click the `+` icon in the top right of the github screen.
- Select `New repository`.
- Fill in "Create a new repository" form:
    - `Owner` is you
    - `Repository name` is what you want to call this repo. The name of your repository will become part of the website url so don't use spaces or special characters apart from `-` or `_`. Lowercase is better too.
    - `Public` / `Private` - choose `Public` here, as you want your website to be visible. GitHub is mostly public repositories with code people can view and copy for free (following the [license](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/licensing-a-repository) applied by the owner).
    - Check the `Add a README file` option.
	- Finally, click the green `Create repository` button to create your new repository.

Your new repo contains one file, `README.md`. Before we do anything else we'll turn on the *Github Pages* setting.

### 2. Activate GitHub Pages
- Click `Settings`
- Click `Pages` in the left-hand menu
- Under `Source`, select `main` branch and leave folder as `"/ (root)"`
- Click `Save`
![Github Pages Settings Screenshot](assets/images/GithubPagesSettings.png)

> ### README, Markdown, and Editing
> 
> 📌 You will notice that by default the contents of the `README.md` file are displayed on the home page of your repository. 
> This is a convention used in many code projects. **README** is a place to write the basics *about* your repository so users will understand what it contains, who made it, and any other information they should know. 
> On GitHub READMEs are usually written in Markdown (thus the `.md` extension). 

> 📌 **Markdown** is a standard to simplify writing content for the web designed to be easy to read and write. 
> [GitHub Markdown Flavor](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax) can be used any where on GitHub to format your writing in comments, Issues, and `.md` files.
> The basics are intuitive, much like formatting a plain text email, as can be seen in the [Mastering Markdown Guide](https://guides.github.com/features/mastering-markdown/).

### 3. Edit your README using Markdown:

- On your repo home page click the filename `README.md`, which will bring you to the page for that file.
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

- When done editing, scroll to the bottom of the page to the `Commit changes` section. 

-----------------

📌 Commit is a git concept--basically taking a snap shot of the changes that will be permanently stored in your repository's history. Every commit records a user name, email, and message. 

-----------------

- Fill in the first text box with your "commit message", i.e. a short description of what changes you have made. This is your message to the future to help understand the code.
- Click the green `Commit changes` button to complete your first "git commit"!

Once you commit, you will immediately see your `README` updated content rendered on the page.
Behind the scenes GitHub is converting your Markdown code into HTML for display. 

### 4. Create an Index.md

Most of the Web is made up of HTML, CSS, and JS:

- **HTML** (Hypertext Markup Language) provides the structure and content, via a formal syntax for "tagging" the elements of a page such as headings, paragraphs, or lists.
- **CSS** (Cascading Style Sheets) provides the style.
- **JS** (JavaScript) provides the interactivity.

When you access a website, the server sends your computer the code which your browser renders into a web page that you can view and interact with.
Thus, one fascinating aspect of the web is that everyone must share code to participate.

We will start with an index.md file because by default the server provides index as the home page of your site.

- Click the `Code` tab to go to your repository's home page.
- Click the `Add file` button and select `Create new file`. This will open the web-based text editor.
- Type in the name for your file: `index.md`.
- Put your cursor in the editor and write some Markdown

```

## 
# Header One: Big Text</h1>
 
An example paragraph

## Header Two

Paragraph with **Bold text**

A link to [Github](https://github.com)


```

- When done editing, scroll to the bottom of the page to the "Commit changes" section. 
- Fill in your "commit message" and click the green "Commit changes" button.

After you commit, you will be redirected to your repo home page.
Clicking on the word `commits` in the upper right of the file box will bring you to the history of your repository. 
Each commit is represented on the page displaying your commit messages. 
Clicking on the *hash* (the series of numbers to the right of the commit message) will display all the information about the commit, including all the changes made to files. 

Now that we have an `index.md`, let's visit our new website. 
The URL for any GitHub Pages site follows the pattern: 

`https://<username>.github.io/<repositoryname>/`

You can also find the link by looking back in your Settings once gh-pages has been activated.

Each time you make a commit GitHub Pages will re-deploy your files, which might take a minute. 
Once it is complete (assuming everything goes well!), a green check will appear next to your commit in the history.

-------------

📌 Git & GitHub:

- [GitHub Guides](https://guides.github.com/), see [Hello World](https://guides.github.com/activities/hello-world/) for an introduction.
- [GitHub Learning Lab](https://lab.github.com/)

📌 Markdown:

- [Mastering Markdown GitHub Guide](https://guides.github.com/features/mastering-markdown/)
- [GitHub Markdown documentation](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)
- [Markdown and Pandoc for Academic Writing](https://evanwill.github.io/write-md/)
- [Markdown](https://daringfireball.net/projects/markdown/) (original spec by John Gruber)


--------------------

#### 💡 Key Points:

✅ Use `git config` with the `--global` flag to configure user name, email address, editor once per machine

✅ `git init` initializes a repository

✅ Git stores all of its repository data in the `.git` directory
