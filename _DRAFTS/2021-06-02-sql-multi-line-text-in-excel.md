---
layout: post
title:  "Import multi line text into Excel from MS SQL Server"
summary: No more broken spreadsheets - so long as you ditch copy and paste
author: Tim Smith
date: '2021-06-02 20:35:23 +0000'
categories: ['excel', 'mssql']  
thumbnail: /assets/img/posts/code.jpg
keywords: excel, mssql
permalink: /blog/welcome-to-devlopr-jekyll
---

We've all been there, with some data to extract from a SQL table that includes a multi line text field. Copy and Paste won't work as it will insert extra rows.

The solution is to use the Import Data. You've likely already got the query ready to go anyway.

Date -> New Query -> From Database -> from SQL Server Database
