---
layout: post
title:      "Adding Dynamic Features to a Rails App with jQuery"
date:       2017-10-27 18:34:09 +0000
permalink:  adding_dynamic_features_to_a_rails_app_with_jquery
---


For my fourth portfolio project, I worked on expanding the Rails project that I built in my previous project. The goal was to add dynamic features to the app using jQuery and a JSON API.

To briefly recap, the previous web app was a daily fantasy lineup building tool built on Rails. The app allows users to build new lineups and new players. So, a user has many lineups and a lineup has many players. Players can also be used across multiple lineups, so the players and lineups model is connected via a join table.

The new functionality allows the index page of a user's lineups to be rendered via jQuery and an Active Model Serialization JSON backend. The lineups are fetched via an AJAX GET request, with the backend rendering the lineups in JSON format, and then the lineups are appended to the page.

The lineups show pages can be sifted through using a next/previous button, with the next/previous lineup being fetched and rendered via jQuery/AJAX. The players that belong to that lineup are also rendered on the show page, through the JSON that is fetched via the AJAX GET request for the lineup JSON.

A user can also add a player to the lineup via the lineup show page without a page request. Upon form submission, the player is serialized, submitted via an AJAX post request, with the response being a new object in JSON that is appended to the DOM using JavaScript. The player prototype object has that formats submitted player positions into the correct format.

If you want to check out the project, you can visit the GitHub repo [here](https://github.com/ChristopherJamesN/rails-daily-fantasy-lineup-builder).

