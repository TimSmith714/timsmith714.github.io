---
layout: post
title:  Using Excel to read XML
summary: Excel has some surprisingly powerful tools for working with XML documents
author: Tim Smith
date: '2020-11-26 19:35:23 +0000'
categories: excel, xml
thumbnail: /assets/img/posts/code.jpg
keywords: excel, xml
permalink: /blog/xml-with-excel
---

Excel might not be the first 

Start Excel and open the XML file as you would any other file. Excel will then prompt with three different ways to open the file:

- As an XML table
- As a read-only workbook
- **Use the XML Source task pane**

It's the last option that you want.

This opens the structure of the XML document in a Task Pane on the right. You'll probably see a message warning "The specified XML source does not refer to a schema. Excel will create a schema based on the XML source data". It's nothing to worry about, in fact, I can't remember when I haven't seen this warning opening an XML file!

Drag and drop elements from the pane into the worksheet to build a table. Some familiarity with the structure of the XML file can be useful here. When writing this, I added the title and Publication date for the channel node of a blog into the spreadsheet. That was only a single node - what I actually wanted was the title and Publication date inside the item node.

Once you've added some fields click the Refresh button in the Data Ribbon Tab to populate the table.
