---
title: "Making a github-hosted website"
tags:
- coding
- tool
- how-to
---

I use Jekyll for static-site generation, combining with Atom for git and Obsidian for writing. Here are the resources I use to pimp this site.

# How I do it (ver 1.0)
- First, I pull the theme from [gradfolio](https://github.com/jitinnair1/gradfolio/) to my repo and download the content to my machine.
- Install Jekyll locally so I can preview the website before `git push`
- I want to have a note section instead of blog post. So I use bi-directional link feature from [notenote.link](https://github.com/Maxence-L/notenote.link) inspired from [[notes/PKM|Obsidian]]
- The notes are showed randomly using the code in [generating a list of random notes](https://thornelabs.net/posts/a-better-way-to-display-random-jekyll-posts-on-page-load-or-refresh-using-jquery-and-json.html)
# The template based on Hugo
The current template this site  based on is [Quartz](https://github.com/jackyzha0/quartz), a PKM website template using Hugo. Similar to the ver. 1.0 I hacked together and provide a graph! The structures are more simple in that except the index page, every other page is just a note. It is free and is actively improved by the community. You are also welcome to donate to the creater Jacky Zhao.

Although both `[markdown](note/markdown.md)` and `[[markdown]]` and even `[[markdown|alias]]` all work, the path need to start from your absolute path under `content`, otherwise the graph will break. So for the time being better stay with the wikilinks plus absolute path and aliases that reduce the text.

## How to update
```bash
git checkout uhugo
git fetch upstream
git merge upstream/hugo
git checkout hugo
git merge uhugo --allow-unrelated-histories
```