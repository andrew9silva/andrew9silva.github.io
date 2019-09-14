---
layout: post
title:      "CLI Portfolio Project. "
date:       2019-09-14 22:21:46 +0000
permalink:  cli_portfolio_project
---


Starting this project was a bit intimdating for me.  It is one thing to just state your knowledge of Ruby and its mechanics (this is a class, this is an instance, this is how you scrape a website) but it is another thing when you need to apply those priniciples to a blank canvas.  For those about to start their project, I recommend taking something you love and using that to create your CLI.  It will help keep your interest and keep you motivated during periods where you are struggling.  Going with that, my CLI helps the user find information on some of the best ski resorts in North America.

I was able to narrow down how man classes I needed to 4; one class for the scraper, one for the CLI, one for States (where the resorts are located) and finalyy one for Mountain (the actual resorts).  Initially, in my Scraper class I had two methods to scrape information for each of my States and Mountain class.  Later on I found it more efficient to just scrape for my Mountain class and upon initialization of a new Mountain, to create a new State (unless the State already existed with the same name).

Once I cleaned up my scraping an initialization and scraping I found getting my program to go through the process once was very easy, but having it loop if the user wanted to find another resort caused all kinds of errors.  This is where I discovered one of the instance methods I was using, .keep_if, seemed to be exactly what I wanted on the surface, but did not work in a loop.  .keep_if is great to just find one object in an array one time, but since it jsut returns Nil for all objects that do not match what you want, when you go back through you get an error, since no methods can be executed on Nil.  I decided .detect is what I actually needed to use.  Once I switched to .detect I no longer had errors when I was looping back through the program and everything was working just as I wanted it to.

To sum up my experience here, while it can be intimidating having to start from scratch and having much more limited help available, struggling is the best way to learn.  It forced me to do my own research and try and understand concepts without someone walking me through it.  I encourage all students doing this project to embrace the struggles and use them as an opportunity to look at a concept from a different angle rather than cause it to discourage you.
