---
layout: essay
type: essay
title: "Meteor Gotchas"
date: 2017-03-09
labels:
  - Software Engineering
  - Meteor
---
## Problem 1: Start times

One of the biggest issues I encountered with the digits application was during the initial start time. First I ran ```meteor npm install``` , which did not bring up any issues. Once the libraries were installed we had to start the application with  ```meteor --settings ../config/settings.development.json```. It was noted in the documenation that this command would take some time, but after 20 minutes with no progress I knew something had to be wrong. Although I wanted to immediately ask for help, I instead went to the class Slack channel to see if anyone had posted about it. Sure enough many of my fellow class mates were also experiencing the same issue. 

  Apparently, the problem with the delayed start of the applicaiton had to do with my operating system and my antivirus. Windows operators who are running antivirus programs in the background see longer start times due to the on-demand scan being run concurrently with the starting of the application. In other words, starting the meteor application triggered the antivirus program to began an on-demand scan. This took a lot of my computers CPU and greatly slowed the process. Once the on- demand scan was disabled, I started the app at a comparitevely fast speed. 

## Problem 2: Refreshing the application

  Another problem that I experienced was issues with the application reflecting changes in the code. There were instances where I made some edits to the template that did no result in any visible changes. For example, I inserted an image into header.html using ```<img class="ui fluid image" src="/images/digits-header.jpg">```. This is code that I have used many times and felt confident that it should work. Upon checking the application for my new image, I was instead greeted with no changes and no error messages. This caused me to triple check my syntax and spelling, but I found no errors. Eventually I noticed that IntelliJ was unable to finish indexing and resulted in not getting my changes to the application. I first tried restarting IntelliJ, but that resulted in no change. Frustrated, I restarted meteor with ```meteor reset``` and then started the application again. This somehow ended up fixing the issues and my new changes in the code were reflected in the application. Unfortunately, I ended up experiencing this issue a few times while developing the digits app and it was quie disruptive to my workflow when I had to restart the app. 
