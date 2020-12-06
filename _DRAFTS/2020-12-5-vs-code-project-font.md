---
layout: post
title:  Use a custom font for a specific project
summary: Summary for the post goes here
author: Tim Smith
date: '2019-05-22 14:35:23 +0000'
categories: comma deliminted, use catergory for single 
thumbnail: /assets/img/posts/code.jpg
keywords: comma, deliminated
permalink: /blog/welcome-to-devlopr-jekyll
---

Most of the time I use Fira Code in Visual Studio Code. It looks good and supports ligatures. My most frequent project is my Foam notes repository and as that's mostly prose (and a little poetry) a mono-spaced font isn't ideal. The Project settings file created by VS Code allows you to set the font for that project while leaving the others the same.

Assuming you've opened the project with the Open Folder option, look for the .vscode folder and the settings.json within it. Add a line like

{% highlight json %}
  "editor.fontFamily": "Ubuntu",
{% endhighlight %}  


