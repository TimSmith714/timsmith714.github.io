---
title: Get your external IP address with PowerShell
---

This is a common need, and one that gets more complicated with services hosted in Azure Apps and Virtual machines.

Normally I'd just search "What's my IP address" but that isn't possible with an Azure App Service.

But I did discover that the Kodu Powershell is available, In the left hand menu of your App Service, look for Development Tools and click Advanced Tools and then Go. Click Debug Console and then PowerShell. 

You can now follow massively useful tip by [Chrissy LeMaire](https://twitter.com/cl)  at https://blog.netnerds.net/2013/09/powershell-two-liner-get-external-ip-address/ and run

`Invoke-RestMethod https://ipinfo.io/json`
