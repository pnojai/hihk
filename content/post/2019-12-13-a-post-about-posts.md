---
title: A post about posts
author: Jai
date: '2019-12-13'
slug: a-post-about-posts
categories:
  - Web
tags:
  - Blogdown
  - Hugo
  - R
description: ''
thumbnail: ''
---

# Static
A static website is a convenient platform for a blog. It serves fast, and it's easy to maintain (if there are no bugs).

- Hugo makes it easy to generate pages.
- The `blogdown` R package makes it easy to author content in Markdown.
- If you maintain it on GitHub, you have an effective collaboration tool.
- Netlify hosting gets you automated deployment from a GitHub repo.

# A beginning is a delicate time
Here's how our team sets up to publish together.

## Tools
I prefer to install tools in a virtual machine dedicated to a particular development environment. I use Ubuntu Linux in VirtualBox.

- [Install R](https://www.r-project.org/).
- [Install RStudio](https://www.rstudio.com/).
- Install `blogdown`. In RStudio, install it from CRAN.

`install.packages("blogdown")`

-  Install Hugo, which `blogdown` uses to generate pages. `blogdown` has a helper function to get that for you. In RStudio:

`blogdown::install_hugo()`

- [Install Git](https://git-scm.com).

# Access content
- [Create a GitHub account](https://github.com).
- [Fork the hihk repo](https://github.com). HIHK is a stub website name. I used to write a blog I called "Heaven in Hell's Kitchen."
- Clone the repo to your local environment.

# Write
- Create a Git branch. This supports development of multiple posts and releasing them selectively. My convention is to name the branch with the word "article" and a slug. The branch for this article is `article_hugo`.
- In RStudio, click Addins in the toolbar. Select New Post. If your post includes code chunks, you need to create R Markdown. If it's text only, just Markdown.
- Write your post.

# Publish
- Commit your changes in Git.
- Push to GitHub.
- Create a pull request into the master branch of the parent repo, [pnojai/hihk](https://github.com/pnojai/hihk). When I merge your pull request it, your post is deployed.
- After I merge your article's development branch into master, you can delete your development branch.

# View
This blog is live at a spare domain, [www.steelwig.com](https://www.steelwig.com). It has my picture and some stuff about me. The intention is to update that to reflect team contributions.

# But wait, there's more.
This online book details the architecture and process I outline here.

[Creating Websites with R Markdown](https://bookdown.org/yihui/blogdown/). Yihui Xie, Amber Thomas, Alison Presmanes Hill.