---
layout: post
title:  "Rails Project"
date:   2016-08-10 18:54:48 +0000
---


For my rails final project, I decided to build a web app that would allow employees in a client-service business (law, accountant, etc) to keep track of their hours worked on different projects. 

Models:

1. Diary: A diary is essentially a weekly time card. It belongs to a user and has many entries. It has a status which is an active record enum, either "open" or "submitted." It has methods to calculate the total hours, hours by day, and hours by project. Finally it has a #submit method, which changes its status to "submitted" and builds a new empty diary for its associated user.

2. Entry: This is a join table between diary and project, which allows records a specific instance of working on a project for the diary. In addition to diary_id and project_id, it has minutes and an enum for day. 

3. Project: Very basic, only has a name (in a more advanced version it would have client info, etc)

4. User: Implemented using devise and omniauth (for facebook login capability). A user has many diaries, one of which is the 'current diary' (only the current can be edited). There are instance methods for calculating the hours (current period and lifetime) and there is a class method (User.mvp) for finding the user with the highest total lifetime hours.

Features:

A user can login/sign up, either through the app or via Facebook and can sign out. When a user signs up, a new diary is automatically generated and set as that users 'current diary'. A logged in user can view all his past diaries. The header contains a link to view the current diary. A user can view any of his diaries; the view displays a table of all the entries. If the diary is the current diary, the user can add/delete entries or submit the diary. If the diary is not current, the user cannot edit.



