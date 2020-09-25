---
layout: post
title: Pre-Commit Hook
category: WEB
---

I added an ```update:``` variable to ```_config.yml``` and a [pre-commit hook](https://stackoverflow.com/questions/14978474/how-to-show-the-modification-date-of-a-file-in-jekyll) at ```/git/hooks/precommit```. The ```update:``` variable is modified/updated with each commit in the ```_config.yml``` file and, also, wherever it appears in the "front-matter" of my site files.
The date can then be placed and formatted as desired in content of site pages by embedding jekyll-ruby code variables  in html such as: ``` page.update | date: "%b %-d, %Y" ```.