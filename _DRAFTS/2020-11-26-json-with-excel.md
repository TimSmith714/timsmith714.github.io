---
layout: post
title:  Using Excel to read JSON
summary: As XML seems to be falling out of favour compared to JSON, I look at working with this file format
author: Tim Smith
date: '2020-11-26 19:35:23 +0000'
categories: excel, json
thumbnail: /assets/img/posts/code.jpg
keywords: excel, json
permalink: /blog/json-with-excel
---

Turns out it's not quite as simple, though that cost does deliver some more flexibility.

That's because you'll access the JSON data with Power Query.

I took a JSON file from an API giving me the posts from a blog I'm working on.

Start Excel with a blank workbook. Click the Data tab and then the Get Data menu button. Click From File and then From JSON. Choose and open a JSON file.

This JSON file had a handful of top level nodes (such as telling me the limit on the number of records) and then and "objects" node with the individual blog posts.

Once this is shown in PowerQuery click the Into Table button that appears in the Ribbon. Right click List in the ojbects row and click Drill Down. Click To Table in the Ribbon and then again. Leave the options in the window as they are and click OK.

Click the Expand icon in the Column1 title. This gives the option to choose which fields to include in your data. This can get a little complicated so I'd recomment having the JSON file open in an editor at the same time for reference. This is particularly helpful when there are subnodes.