---
layout: post
title:  "Simulate an input event in Nightwatchjs"
summary: How to test a text input with a javascript event on input
author: Tim Smith
date: '2019-08-21 10:54:23'
category: nightwatchjs
thumbnail: /assets/img/posts/dispatchEvent.png
keywords: nightwatchjs, testing, web development, javascript
permalink: /blog/simulate-input-event-nightwatchjs
---

Adding a value to an input box is fairly straightforward in Nightwatchjs, even though .setValue() doesn't seem to be working at the moment.

{% highlight javascript %}
.execute(function () { document.querySelector("#calculator > div > form > div:nth-child(2) > input").value = "300000" })
{% endhighlight %}

But the page I was testing depends on a Javascript event firing on input. Simply setting the value like this wasn't enough. Although the form was completed correctly the javascript variable used for the eventual calculation remained the same.

The solution is to fire dispatchEvent on the element after setting the value

{% highlight javascript %}
.execute(function()document.querySelector("#homewise-calculator > div > form > div:nth-child(2) > input").dispatchEvent(new Event('input'))})
{% endhighlight %}

## Some helpful references

This answer on StackOverflow describes the dispatch even though it's a different event type [How to trigger event in Javascript][https://stackoverflow.com/a/50587874/3066321]

