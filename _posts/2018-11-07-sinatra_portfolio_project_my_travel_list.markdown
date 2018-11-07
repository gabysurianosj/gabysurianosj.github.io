---
layout: post
title:      "Sinatra portfolio project: My Travel List "
date:       2018-11-07 06:42:30 -0500
permalink:  sinatra_portfolio_project_my_travel_list
---

![](http://www.tripcrazed.com/wp-content/uploads/2015/10/TravellingTips_TOPBANNER.jpg)

Inspired by my love for traveling and also by one of my favorite movies, the [Bucket List](https://www.youtube.com/watch?v=vc3mkG21ob4), I created this application for my Sinatra portfolio project. The app aims to enable its users to add wish destinations and new adventures, and even get inspired by others!

There is no limit to what the user wants to create, for example: I (a user of the app) love hiking, so I am making sure I am listing all my future hiking destinations all grouped under one same category so I can access them quicker. I can also view other users 'hiking' experiences to get inspiration for my own future adventures. 

![](https://static1.squarespace.com/static/58352289197aeac1e8c8ce6d/t/59fde6bcf9619a4291805ef7/1509811905873/hiking-gear-checklist?format=1000w)

The below was the process I went through to create this app: 

* I started off creating a tree structure, making sure I included the main functionalities asked for by the project requirements. 
* From the tree structure I created my tables by following the basic logic of the app, which at the time it was (short-version) thought as follows: Users class needs basic info like name, email and password, Experiences would need a description, User ID and country ID. Then the Category and Country class would need a Name. Experiences would belong to a User and a Country and can also have many categories... so from these, I created each model class and used `has_many` and `belongs_to` relationships, depending on the logic outlined. 
* Then, I went on to create User accounts where each user has the ability to sign up, log in, log out and even have the app check that the user is appropriately logged in while trying to access routes. For this, I added several things to my code `enable :sessions`,  added helper methods, and Sinatra filters. 
* In order to meet the next requirement (validating uniqueness of user login) I decided to go for a password verification feature. Using `has_secure_password` and `bcrypt` gem, I was able to authenthicate a user's login. The user is not allowed to access and edit an individual Travel List without its corresponding password stored in the database
* `CRUD`ing along... a User can create/edit by: adding a new experience, editing an experience and/or adding a new experience from another user. 
* Finally, I used Bootstrap for the styling of the website. I had a lot of fun doing this part by simply figuring out what looked best for the user interface. 

I hope you enjoy it as much as I have! 



