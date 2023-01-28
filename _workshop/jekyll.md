---
title: Static Web and Jekyll     # The title of the page
nav: Jekyll
date: 0000-01-03    # Page order is set by date
---

![Github Pages Logo](assets/images/jekyll.jpg)

## Static Web

Unlike [WordPress](https://wordpress.com/) or [Drupal](https://www.drupal.org/), GitHub Pages is not a content management system or dynamic web application.
There is no database, server side processing, or admin interface.

This is known as a [Static Web](https://en.wikipedia.org/wiki/Static_web_page) host. 
HTML, CSS, and JS stored in the repository are served to the user without dynamic changes.
You can think of a static site as a shared folder of readonly files exposed on the web.

In the *olden days* static web was the norm, but database driven dynamic web sites have dominated the last decade.
For example, think of social media sites, where dynamic web applications and huge databases enable features such as user authentication, live comments, and personalized streams. 
All this complex functionality requires heavy server-side infrastructure and processing--which may not be necessary or desireable for all web sites.

Thus, despite their limitations static sites are experiencing a [recent boom](https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/) as a viable alternative because they offer some advantages over that heavy infrastructure:

- faster performance (easy caching / CDN, low bandwidth, no processing time).
- minimal hosting requirements (basic web servers, no dependencies, simple development environment).
- minimal security vulnerabilities (no software or server programming language to get hacked).
- easy version control (everything is plain text).

## Static Site Generators

Static Site Generators are software tools that bundle together a stack of web development packages used to transform a directory of source code into a complete website.
With growing interest in static web approaches, such as [Jamstack](https://jamstack.org/), hundreds of Static Site Generators have sprung onto the scene - browse lists at [Jamstack Site Generators](https://jamstack.org/generators/) and [Static Site Generators](https://staticsitegenerators.net/).

These tools typically feature: 

- a command line interface (not GUI software).
- a built-in development server (test your site on your computer). 
- simplified markup based content (e.g. write in Markdown).
- web templating language (build a site from modular components pulled together with basic logic).
- CSS preprocessor (e.g. Sass).
- file-based data options (create content from CSVs or JSON).
- plugin extensibility (add new functionality).

----------

## Jekyll 

[Jekyll](https://jekyllrb.com/) is one of the most popular and actively developed static site generators, in part because of its direct integration with GitHub Pages.
Originally focused on creating simple blogs from Markdown files, it has developed into a fully featured generator used on all types of web projects from tiny to huge (browse the [Showcase](https://jekyllrb.com/showcase/)).

Jekyll is written in the programming language [Ruby](https://www.ruby-lang.org/) and can be installed on your computer as a Ruby Gem--however, *you don't need to know anything about Ruby to get started using it!*

In fact, in the next section of the workshop we will build a Jekyll-powered blog without installing anything and editing entirely in the GitHub web interface.
Once you set up the repository, GitHub Pages' integrated Jekyll service will automatically build out the site after each new commit.

## Jekyll Projects

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


#### 💡 Key Points:

✅ `git status` shows the status of a repository.

✅ Files can be stored in a project’s working directory (which users see), the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).

✅ `git add` puts files in the staging area.

✅ `git commit` saves the staged content as a new commit in the local repository.

✅ write a commit message that accurately describes your changes.
