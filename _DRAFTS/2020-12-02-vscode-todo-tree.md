---
layout: post
title:  "Setting up Todo Tree"
summary: Summary for the post goes here
author: Tim Smith
date: '2020-12-02 19:35:23 +0000'
categories: vs code
thumbnail: /assets/img/posts/code.jpg
keywords: vs code, todo, comments
permalink: /blog/welcome-to-devlopr-jekyll
---

This is what I ended up with.

I didn't like the inverted highlight for the TODO so I set it to green. It ends up slightly darker than the rest of the comment so it's just the right balance of getting attention and keeping distractions down. I think the gutter icons are probably going to be the main thing that gets my attention.

```json
"todo-tree.tree.showScanModeButton": false,
    "todo-tree.general.statusBar": "total",
    "todo-tree.highlights.customHighlight": {
        "type": "tag",
        "TODO": {
            "gutterIcon": true,
            "foreground": "green"
        },
        "BUG": {
            "icon": "bug",
            "foreground" : "red",
            "gutterIcon": true
        },
        "FIXME": {
            "icon": "flame",
            "foreground" : "yellow",
            "gutterIcon": true
        }
    }
```

There's some extra in a blog post I found [Configuring VSCode – ToDo Tree](https://blog.truesec.com/2020/01/22/configuring-vscode-todo-tree/). I'm not sure if I'll create new tags; it might be a bit much to get the rest of the team to use them but it's good to know the options there.
