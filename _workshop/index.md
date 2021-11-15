---
title: Version Control with Git  # The title of the page
date: 0000-01-01    # Page order is set by date
---

### What is Version Control?
Version control is a name used for software which can help you record changes you make to the files in a directory on your computer.

It can be useful to keep track of when you made changes to your own work and when, and without getting into this situation:

<p align="center">
  <img src="./assets/images/phdcomics_final.png">
</p>
[“Piled Higher and Deeper”](https://phdcomics.com/comics/archive.php?comicid=1531) by Jorge Cham

### Why Should I Use It?
Version control software and tools such as __Git__ and __SVN__ are often associated with software development and did originate from that community. But __*version control isn't just for code.*__ It's for anything you want to track.

For example, using Git to manage a writing project enables you to
* view multiple drafts at the same time
* see differences between those drafts
* roll back changes
* and if you're comfortable doing so, you can then share your work with others on GitHub or other central git repositories.

So at its most basic level, __*version control software helps us register and track sets of changes made to files on our computer*__.

***

#### Benefits of using version control
- [x] __Collaboration__ - Version control allows us to define formalized ways we can work together and share writing and code. For example merging together sets of changes from different parties enables co-creation of documents and software across distributed teams.
- [x] __Versioning__ - Having a robust and rigorous log of changes to a file, without renaming files (v1, v2, final_copy)
- [x] __Rolling Back__ - Version control allows us to quickly undo a set of changes. This can be useful when new writing or new additions to code introduce problems.
- [x] __Understanding__ - Version control can help you understand how the code or writing came to be, who wrote or contributed particular parts, and who you might ask to help understand it better.
- [x] __Backup__ - While not meant to be a backup solution, using version control systems mean that your code and writing can be stored on multiple other computers.

***

### What are Git and GitHub?
We often hear the terms Git and GitHub used interchangeably but they are slightly different things.

**_Git_** is one of the most widely used version control systems in the world. It is a free, open source tool that can be downloaded to your local machine and used for logging all changes made to a group of files (referred to as a “git repository” or “repo” for short) over time. It can control file versions locally on your computer, or on files worked on by groups of people.

Git saves (or in Git parlance, _commits_) changes as snapshots, and manages all these snapshots for you in the background. We can access a log of all the changes that have been made. And all earlier versions of each file still remain in their original form: they are not overwritten, should we ever wish to “roll back” to them.

Git was originally developed to help software developers work collaboratively, but it can be and is used for managing revisions to any file type, including text documents and spreadsheets.
(_Note: certain file types like MS Word and PDF contain special formatting which Git unfortunately cannot version control, though both can be stored in git repositories._)

**_GitHub_**, on the other hand, is a website for hosting and sharing git repositories. It offers a web interface and functionality for working with such repositories.

* As with git, a lot of the content on GitHub is software-related, though increasingly it is being used for other projects such as open access journals (e.g. Journal of Open Source Software), blogs, and academic text books.
* There are other Git hosting services that offer many similar features to Github such as GitLab and Bitbucket.
* Github is an alternative means for publishing content online. Any GitHub repository can have its own project website, blog and wiki using GitHub Pages.
* GitHub hosts many open-licensed projects. By _forking_ a project, any GitHub user can almost instantaneously create their own version of an existing project. A _forked_ project could be the basis for a new project, or it could be used to test new features and later be merged back into the original.

So git and GitHub are related, but different. You can choose to
1. use git by itself to track changes and resolve conflicts or
2. use GitHub to host a project that users can collaborate on or to publish it

Git will preserve the original metadata as well as all edits. GitHub will facilitate discussion about what changes should be made, who should make them, and why.

***

#### 💡 Key Points:

✅ Version control helps track changes to files and projects, like an unlimited 'undo'

✅ It can be useful for both individuals and groups of people

✅ Git and github are not the same
