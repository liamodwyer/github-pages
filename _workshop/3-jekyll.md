---
title: Static Web and Jekyll     # The title of the page
nav: Intro to Jekyll
date: 0000-01-03    # Page order is set by date
---

![Jekyll Logo](assets/images/jekyll.png)

Unlike [WordPress](https://wordpress.com/) or [Drupal](https://www.drupal.org/), GitHub Pages is not a content management system or dynamic web application.
There is no database, server side processing, or admin interface.

This is known as a [Static Web](https://en.wikipedia.org/wiki/Static_web_page) host. 
Markdown, HTML, CSS, and JS stored in the repository are served to the user without dynamic changes.
You can think of a static site as a shared folder of read-only files exposed on the web.

| Static site (e.g. Github pages)              | Dynamic site (e.g. Wordpress)                |
| -------------------------------------------- | -------------------------------------------- |
| Uses client-side technologies e.g. HTML, CSS | Also uses server-side technologies (e.g. PHP, SQL) |
| Server shows website ‘as is’                 | Server generates pages ‘on the fly’          |
| Editing source files directly (html/css)     | GUI for editing content                      |
| Less computational load                      | Can change quickly and often                 |
| Minimal security vulnerabilities             | Hosting and ongoing maintenance more complex |

Database driven dynamic web sites have dominated the last decade, such as with social media sites with dynamic web applications, huge databases and features such as user authentication, live comments, and personalized streams. 
All this complex functionality requires heavy server-side infrastructure and processing - which may not be necessary or desireable for all web sites.

However static sites are increasing been seen as a viable alternative because they offer some advantages over that heavy infrastructure.

## Static Site Generators

Static Site Generators are software tools that bundle together a stack of web development packages used to transform a directory of source code into a static website. You can browse hundreds of these at [Jamstack Site Generators](https://jamstack.org/generators/) and [Static Site Generators](https://staticsitegenerators.net/).

<!-- These tools typically feature: 

- a command line interface (not GUI software)
- a development server (test your site on your computer)
- simplified markup based content (e.g. Markdown)
- web templating language (e.g. YAML)
- CSS preprocessor (e.g. Sass)
- file-based data options (create content from CSVs or JSON)
- plugin extensibility (add new functionality)
-->


## Jekyll

[Jekyll](https://jekyllrb.com/) is one of the most popular static site generators. It takes raw text files, runs it through a renderer and produces a publishable static website.

Originally focused on creating simple blogs from Markdown files, it has developed into a fully featured generator used on all types of web projects from tiny to huge (browse the [Showcase](https://jekyllrb.com/showcase/)).

Jekyll is written in the programming language [Ruby](https://www.ruby-lang.org/) and can be installed on your computer as a Ruby Gem. But  Github comes with its own integrated Jekyll service to save us the bother! With a couple of lines of code we can make use of Jekyll to build out our site. Each time we create or update our markdown content, this jekyll service will run in the background to build our site after each new commit.

## Jekyll Projects & Jekyll Themes

A basic Jekyll project is a folder of files that looks something like this:

![jekyll folder structure](assets/images/jekyllFolderStructure.png)

Content is written in Markdown in files such as `index.md` or items in the `_posts` folder.
The `_includes`, `_layouts`, and `_sass` directories can contain modular components that will flesh out the template of each web page, i.e. the website's theme.
Jekyll knits the content and theme together to build out your website.

However, **you don't need to start from scratch**.
Instead you can use an existing theme to jump start your Jekyll project.

A [Jekyll theme](https://jekyllrb.com/docs/themes/) is basically a packaged set of templates and styles (usually including folders `assets`, `_includes`, `_layouts`, and `_sass`) that can be referenced in your configuration or included directly as part of your project folder.

📌 Note: folder and file names starting with an underscore (`_`) are special to Jekyll. Be sure to name them correctly!

- [GitHub Pages docs](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages)
- [Using Jekyll on GitHub Pages docs](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
- [Jekyll docs](https://jekyllrb.com/docs/)
- Find [Jekyll themes on GitHub](https://github.com/topics/jekyll-theme)

<!--
#### 💡 Key Points:

✅ `git status` shows the status of a repository.

✅ Files can be stored in a project’s working directory (which users see), the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).

✅ `git add` puts files in the staging area.

✅ `git commit` saves the staged content as a new commit in the local repository.

✅ write a commit message that accurately describes your changes.
-->
