---
layout: post
title:  "Dealbook Gem"
date:   2016-06-21 20:58:45 -0400
---


I wasn't sure what gem to make for this assignment, so I decided to make one that would list the articles on the New York Times DealBook website and then give the user the option to read the synopsis of any one of the articles. 

I built an Article class that would represent instances of individual articles as well as provide class methods that used open-uri and nokogiri to scrape the NYT page. The self.articles method scraped the website and saved each article as an instance of Article with a title and description.

Next, I built the CLI class to provide the interface for the user. The #call method would use the Article.articles to create an array of articles and then put the headline and of each to the console. Then it would allow the user to type in the number of an article to view that articles synopsis. The user could also type 'exit' in order to exit the CLE.
