---
title: Github Pages     # The title of the page
date: 0000-01-06    # Page order is set by date
---

_Github Pages_ is a github service which lets you publish a website directly on github from a git repository. You can use html to build web pages but they also provide Jekyll which renders __markdown__ into html.

Github Pages uses a branch in your repo to look for website content. By default the branch has the name `gh-pages` (though this can be changed).
You can do this directly on github but we’ll keep going on git as we have for most things.

```
$ git checkout –b gh-pages
touch index.md
echo “## this is my project website” > index.md
$ git push
```
But git doesn’t know where to push the changes! It guesses what we want to do – to push to gh-pages branch at origin. So lets do that.
```
$ git push --set-upstream origin gh-pages
```
(Note: When we did this for the master branch earlier, we did `git push –u origin master`.  The `--set-upstream` here is the same as the shortened version `-u`)
We can go to http://liamodwyer.github.io/gitlesson 	(and change theme on github settings)
