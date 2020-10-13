# Use try/catch in Google Tag Manager

The big advantage of Google Tag Manager is it makes it easy for people not normally involved in development to add code to the website. The big disadvantage of Google Tag Manager is it makes it easy for people.... well, you've probably guessed the rest.

One lesson I've learnt the hard way is to ensure Javascript Tags are robust. At the most basic that means adding try/catch so an error won't bring down Javascript. I don't know why Google doesn't put a try/catch around every tag behind the scenes but 
