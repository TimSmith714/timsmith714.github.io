---
layout: post
title:  "Title HERE"
summary: Summary for the post goes here
author: Tim Smith
date: '2019-05-22 14:35:23 +0000'
categories: google analytics, websites, analytics, chrome 
thumbnail: /assets/img/posts/code.jpg
keywords: google analytics, websites, analytics, tracing, chrome, extensions
permalink: /blog/google-analytics-chrome-extension
---



There's direct link to [download the extension][extension-link]


Once installed it needs to be enabled. Click the Extensions icon in the toolbar and click the pin to make it visible all the time.

Click it once to turn on the debug mode and open the Javascript console to see what's going on.

In my case I was looking to see what Google Analytics Events were being fired on certain actions, ideally without messing up my stats in the process. To that end we have IP filters on our views - both ways. There's an exclude list to stop internal traffic being tracked in reports that are produced as well as an include list for this kind of debugging.

Luckily, years ago I set up some very basic scroll depth tracking so all that was reuireqd 



[extension-link]: https://chrome.google.com/webstore/detail/google-analytics-debugger/jnkmfdileelhofjcijamephohjechhna
