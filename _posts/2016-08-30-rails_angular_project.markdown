---
layout: post
title:  "Rails/Angular Project"
date:   2016-08-30 00:40:09 +0000
---


This is the first time in this process where I felt like I could see how things kind of fit together (I think..). For this final project I reprised the app I initially made for my sinatra assessment. redX (like the mark of a red pen checking an item off a checklist), is an app to manage the documents required for a corporate transaction (I was thinking about this from the perspective of a corporate attorney working on the deal). The user creates a new deal and chooses from a list of options for what type of deal it will be. Based on the type, the app generates a few required documents, and the user can then add additional documents are required. Each document is initialized without content and with its status set to incomplete. The user can either add content to the document or, alternatively, import the content from a preexisting document of the same type (from a past project). The user can then set the documents status to complete. On the view page for each deal, it sorts the documents by their status (complete/incomplete). Each deal and document can also be deleted.

The rails backend for this project is relatively simple. There are two models Deal and Document, with a belongs_to/has_many relationship between the two. Each has a controller with appropriate actions to interface with the angular front end. I used the active record serializer gem to customize the json that the controllers render when queried. 

The front end is created solely through angular. This project got off the a very slow start because I was at a loss as to how to logistically connect rails and angular (there was nothing in the lessons about how to do this). At first, this was very frustrating , but ultimately after reading through various online tutorials, I got it working. I used bower-rails, which I was unfamiliar with before this project, to manage the frontend dependencies. Ultimately I set up an angular directory in the existing assets/javascripts folder and then adhered to the file structure from the angular lessons within that folder.

Having cleared that logistical hurdle, I was on to the substance of the front end. Compared to rails, angular/js in general gives much less intuitive error messages. In rails when something goes wrong, it usually shows you the exact line where the problem is, whereas in angular sometimes the page just doesn't load but displays no errors, so I would find myself combing through my recent additions line be line to find the error. 

Eventually I finished the project, using most of the different features from the angular unit. I really enjoyed designing the interaction between angular and rails. I think that rails makes more intuitive sense when it is used solely as an API (as was the case here). I liked working with angular more than the rails .erb views.
