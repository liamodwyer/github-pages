---
title: Themes     # The title of the page
nav: Using templates
date: 0000-01-05    # Page order is set by date
---

# Using Jekyll Themes and Templates

![Academic Pages Template](assets/images/academicPagesTemplate.png)

In the last example we build up the site pretty much from scratch, using a very stripped-back Minima theme. There are lots of other jekyll-based themes and templates that can make the process of building your site a lot quicker. In fact, often it is more a case of stripping out what you don't need from these templates. Knowledge of the Jekyll structure covered in section three above is useful in this process, knowing where to change the relevant content.

In this section we will work through a few examples of this and create a few Github Pages sites in the process.

## Forking and Templates

Forking and Templates are *sort of* similar for the purposes we are using them here i.e. they both enable us to make a copy of an existing theme to use as a jumping off point for a website. However it should be noted that they are different concepts:
 
- Templates are repositories specifically intended to be used a as a boilerplate to copy and build off - for example, for a website. Not all repositories are templates.
- Forking is possible with *all* public repositories on Github. While your copy is independent of the source repository, it keeps a link to it. This is because forking is often done for collaborative work where the person forking may want to contribute back to the source project. 
- When forking, you should check the licence statement of the source repository to correctly credit it

## Creating a repository from a template

Creating a repository from a template

- Navigate to the main page of the repository.
- Above the file list, click `Use this template`
- Select `Create a new repository`

![Template screenshot](assets/images/createByTemplate.png)

## Forking a repository

- Navigate to the main page of the repository
- Click on the "Fork" button
![fork button](assets/images/forkButton.png)
- By default, forks are named the same as the source repositories. You can change the name to distinguish it further.
- A forked copy will then be added to your own repositories. The small text below the repo name confirms this is a fork.

In both cases you are free to experiment with the repository you have copied, without affecting the original project.

# Practice!

We will take a few of these in turn and look at how to customise them, mainly using `_config.yml` and looking around at some of the other folders like `_data` and `_posts` . 

:pushpin: **With all of these we begin by switching on the Github Pages setting as in section 4.**

-----------

### Minimal Mistakes (Template)

![Academic Pages Template](assets/images/minimalMistakes.png)

- [Minimal Mistakes](https://github.com/mmistakes/mm-github-pages-starter)
- a very popular github pages template
- Edit _config.yml
	- url:
	- baseurl:
	- repository
- Upload profile image
- Edit _data/navigation.yml to remove categories and tags
- *an academic profile template based on this this is also available: [academicpages.github.io](https://github.com/academicpages/academicpages.github.io)* 

-----------

###  Minimal Light (Template)

![Academic Pages Template](assets/images/minimalLight.png)

- [Minimal Light](https://github.com/yaoyao-liu/minimal-light)
- A nice one-page site template

-----------

### The Plain Academic (Template)

![Academic Pages Template](assets/images/plainOne.png)

- [The Plain Academic](https://github.com/brenov/the-plain-academic)
- Another academic-themed template

-----------

### Academic Pages (Fork)

![Academic Pages Template](assets/images/academicPagesTemplate.png)

- [Academic Pages](https://github.com/academicpages/academicpages.github.io)
- Based on the Minimal Mistakes theme above
- Quite a content-heavy theme with a lot to strip out to begin with

-----------

# Wrap Up

## Finding templates

If you want to look for more of these kinds of templates to find one you like, there is a handy topic list on github of over 200 repositories categorised as ['academic websites'](https://github.com/topics/academic-website).

## Deleting repositories
When you've finished practicing or if you run into any problems you can delete repositories you don't want to keep by going to:
- Settings > Scroll to bottom
- Delete this repository

Github will ask you are you sure you want to do this but this is only a problem if it is a site you are intending to do further work on. And you can always re-fork or re-use a template you tried out already if you want to go back to it

