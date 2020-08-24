---
layout: post
title:  "Set a Visual Studio Code theme for a specific project"
summary: A simple and consistent way to distinguish between project windows
author: Tim Smith
date: '2020-08-24 08:30:00 +0000'
category: vs-code
thumbnail: /assets/img/posts/vs-code-workspace-color-theme.png
keywords: vs-code, vs code themes, productivity
permalink: /blog/set-a-vscode-theme-for-a-project
---

Having decided to start a 

A good way to distinguish between several projects open at the same time is to use a separate [[VS Code Theme]] for each one.
This will create a .vscode folder in your project so bear that in mind in shared projects.
- First make sure you have the Themes you want to use has been installed
-  Click File, Preferences, Settings
-  Click the Workspace tab. I had: User, Remote [WSL: Ubuntu 20.04], Workspace
-  Open Workbench in the left hand menu and click the Appearance submenu
-  Scroll to Color Theme in the main window and select the desired theme
-  The change should happen automatically and you can check for a .vscode folder in your project. If there are no other customised settings the settings.json file should look something like this 

{% highlight json %}
{
    "workbench.colorTheme": "Solarized Dark"
}
{% endhighlight %}