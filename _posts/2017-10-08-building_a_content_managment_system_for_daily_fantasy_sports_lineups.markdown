---
layout: post
title:      "Building a content managment system for Daily Fantasy Sports Lineups"
date:       2017-10-08 14:45:28 -0400
permalink:  building_a_content_managment_system_for_daily_fantasy_sports_lineups
---


I wanted to have a way to easily create and share daily fantasy sports lineups with my friends, so I created a web application using the Ruby framework Sinatra to do just that.

The application employs a model view controller framework, that allows the user to create a new account, sign in, and create, edit and delete fanatsy football lineups.

Users can also view all the lineups that other user have created, however, they will not be able to edit or delete lineups that they have not created themselves.

Sinatra flash alerts are used to alert the user whenever they have taken an action that is not allowed within the application, such as entering an incorrect password, trying to signup with a username that already exists, or adding a lineups without a lineup name.

The application is built with two classes, a User class and a Lineup class. A user has many lineups and a lineup belongs to a user. Active Record is used to manage these associations as well as all other database interactions.

The User and Linuep classes both have controllers that inherit from the application controller, which itself inherits from Sinatra::Base. A logged_in? and current_user helper method are defined in the applications controller, and all create, read, update, and delete actions are defined in the User and Linuep controllers.

Corresponding views are written with HTML and embedded Ruby, and Bootstrap is used to give some styling to the application.

If you want to play around with the appliction locally, the Github repo can be found [here](https://github.com/ChristopherJamesN/sinatra-daily-fantasy-lineup-sharing).
