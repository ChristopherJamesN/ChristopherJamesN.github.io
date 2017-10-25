---
layout: post
title:      "Using Rails to Create a Fanatasy Football Lineup Building Web Application"
date:       2017-10-19 12:04:03 -0400
permalink:  using_rails_to_create_a_fanatasy_football_lineup_building_web_application
---


Building and tracking my daily fantasy sports lineups has historically been a chore, so I created a web application using the Ruby on Rails framework that allows the user to create lineups and players, with each player having a name, position, actual points, and projected points attributes. This allows the user to track how their players have performed compared to their projections.

The application employs a model view controller framework. The devise gem is used to create a user model that allows the user to create a new account, sign in, and create, edit and delete fanatsy football lineups and players that belong to those lineups. The devise gem checks to ensure that users have entered a valid email address and have created a password that is at least 6 characters long.

In addition, the OmniAuth gem is used to allow users to signup and signin with their facebook credentials, so that they do not have to create a new account if they do not want to.

Flash alerts are used to alert the user whenever they have taken an action that is not allowed within the application, such as entering an incorrect password, trying to signup with a username that already exists, or adding a lineups without a lineup name.

The application is built with three classes, a User class, a Lineup class, and a Player class. A user has many lineups and a lineup belongs to a user. Players and lineups are connected via a join table, lineupsplayers, so a lineup has many players through lineupsplayers and a player has many lineups through lineupsplayers. Active Record is used to manage these associations as well as all other database interactions.

The Linuep and Player classes both have controllers that inherit from the application controller, which itself inherits from ActionController::Base. All create, read, update, and delete actions are defined in the Linuep and Player controllers.

Corresponding views are written with HTML and embedded Ruby, and Bootstrap is used to give some styling to the application.

If you want to play around with the appliction locally, the Github repo can be found [here](https://github.com/ChristopherJamesN/rails-daily-fantasy-lineup-builder).
