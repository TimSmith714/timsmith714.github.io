---
layout: post
title:  "Hide text in Excel cells"
summary: Do not rely on colour formatting to keep numbers hidden
author: Tim Smith
date: '2020-10-26 19:35:23'
categories: Excel, Conditional Formatting, reporting
thumbnail: /assets/img/posts/excel-custom-formatting.png
keywords: excel, conditional formatting, reports, office
permalink: /blog/hide-text-in-excel-fields
---

One limitation of Conditional Formatting is that it's applied to the cell with the value. I'm happy to be proved wrong or ignorant (though, let me be clear, just in this very specific context) but there isn't a way to apply the conditional formatting based on the adjacent cell's value. This is frustrating if you want to show a graphic without the value showing.

Changing the colour of the text is one option, but that leaves the risk of the value suddenly appearing if the cell colour is changed.

A custom formatting option is the answer. Select the cell and press Ctrl+1 to show the Format Cells window. Click the Number tab and then custom in the left-hand Category list.

Click in the Type text box in the main part of the window and enter `;;;`

The text has now disappeared. If I still want to show a value, just not alongside the conditional formatting, I set the conditional formatting cell to pull in that adjacent value, something simple like `=c5`.

## How it works

A custom format has four elements, each separated by a semi-colon:

- Positive numbers
- Negative numbers
- Zero
- Text

So in this a custom format defined as `;;;` displays nothing regardless of the cell contents.

## One step further

So as I was writing this I was wondering if there might be a use case where you would want to see text - a formula error was the obvious one that sprang to mind. Otherwise you run the risk of a silent error, the type that's most likely to spoil your day.

The solution is to leave the numeric options blank but use the @ glyph to include text, thusly `;;;@`

![Screenshot showing error but number is hidden](/assets/img/posts/excel-custom-formatting-small.png)

## Or you could do it the easy way

If you're only planning on using an icon set rather than colours, Excel offers this an option in the Edit Formatting Rule window. (I would only find this after writing the rest of the post!). Select "Show Icon Only" to make the contents of cell disappear. I was very pleased to see that error text is shown so there won't be any silent errors.

![Screenshot showing error but number is hidden](/assets/img/posts/excel-icon-set.png)

[Official Microsoft documentation](https://support.microsoft.com/en-us/office/review-guidelines-for-customizing-a-number-format-c0a1d1fa-d3f4-4018-96b7-9c9354dd99f5)