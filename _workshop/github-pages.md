---
title: Github Pages     # The title of the page
date: 0000-01-06    # Page order is set by date
---

_Github Pages_ is a GitHub service which lets you publish a website directly on GitHub from a Git repository. You can use html to build web pages but they also provide Jekyll which renders __markdown__ into html. And we have a markdown file we've made!

---
### Why GitHub Pages is awesome!
GitHub Pages allows you to version control your website. This is useful for a lot of different reasons. It allows you to keep a record of what changes you have made. It allows people to reference your website at a particular point in time and (if you make your source open) to see what it was like at that particular point in time. This is very useful for academic citations. Most people have had the experience of following up a reference to a website and either getting a 404 error or seeing something completely different. Although using versions on your site doesn’t guarantee this won’t happen, it does make it easier to manage old versions of your site.
---

### Enable GitHub Pages
GitHub Pages is turned off by default for all new repositories, and can be turned on in the settings menu for any repository.

Let’s set up a new site by enabling GitHub Pages for our project.

Go to the Pages section of your repository’s Settings:

<p align="center">
  <img src="./assets/images/github-repo-settings-pages.png">
</p>

### Source branch (required)
Pages needs to know the branch in your repository from which you want to serve your site. This can be any branch, including `main`. Here we will use `main`.

Select then save the source branch:
<p align="center">
  <img src="./assets/images/github-repo-settings-pages-branch.png">
</p>
<p align="center">
  <img src="./assets/images/github-repo-settings-pages-save.png">
</p>

### Theme (optional)
GitHub Pages provides different themes to visually style and organize your site’s content. Choosing a theme is optional, and themes can be interchanged quickly.
<p align="center">
  <img src="./assets/images/github-repo-settings-pages-theme.png">
</p>

### View your site
If we now visit <https://<username>.github.io/gitlesson/article>, we should see the contents of the article.md file that we created earlier.

Usually it’s available instantly, but it can take a few seconds and in the worst case a few minutes if GitHub are very busy.

📌 __Make a home page for our new site__

If we want to give our project site a home page we can create a new `index.md` page on GitHub - or you can create it locally and `push` like we did already for `article.md`. For now it could just have a markdown header (e.g. "_# This is my project site_")

This index.md page will resolve at a root url of <https://<username>.github.io/gitlesson/> (Sometimes with GitHub Pages you need to change the theme to refresh the site index to include your new home page.)

---

#### 💡 Key Points:

✅ GitHub Pages offer an automated way to create a website that is version controlled and accessible for collaboration
