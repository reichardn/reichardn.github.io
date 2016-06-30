---
layout: post
title:  "Sinatra project"
date:   2016-06-30 02:23:35 +0000
---


For my Sinatra project, I made a very, very basic version of a web app that would allow a corporate lawyer to manage all the tasks related to an M&A transaction. A user has a number of Deals associated with it and each deal has a number of related tasks. The user can add, edit, or delete tasks.

In order to build this, I built 3 models (Deal, User, Task) with a table for each. I built 3 application controllers to handle the different routes, to edit, create, delete Deals and Tasks, to sign up a new User and to login and logout . 
