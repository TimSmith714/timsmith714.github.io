---
layout: post
title:  "Get your external IP address with PowerShell"
summary: A handy tip for getting your external IP address when you have PowerShell but no browser
author: Tim Smith
date: '2020-08-18 19:54:23'
categories: powershell azure
thumbnail: /assets/img/posts/powershell-ip-address.png
keywords: azure, powershell, web development, 
permalink: /blog/get-external-ip-powershell
---

This is a common need, and one that gets more complicated with services hosted in Azure Apps and Virtual machines.

Normally I'd just search "What's my IP address" but that isn't possible with an Azure App Service.

But I did discover that the Kodu Powershell is available, In the left hand menu of your App Service, look for Development Tools and click Advanced Tools and then Go. Click Debug Console and then PowerShell.

You can now follow massively useful tip by [Chrissy LeMaire](https://twitter.com/cl)  at https://blog.netnerds.net/2013/09/powershell-two-liner-get-external-ip-address/ and run

`Invoke-RestMethod https://ipinfo.io/json`
