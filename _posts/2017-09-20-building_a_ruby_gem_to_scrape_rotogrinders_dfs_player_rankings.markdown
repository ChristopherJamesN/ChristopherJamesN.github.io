---
layout: post
title:  "Building a Ruby Gem to Scrape Rotogrinders DFS Player Rankings"
date:   2017-09-19 22:44:30 -0400
---


I recently published my first Ruby Gem. You can check it out [here](https://rubygems.org/gems/DFS-player-rankings) as well as the [GitHub repo here](https://github.com/ChristopherJamesN/DFS-Player-Rankings-cli-app). 

The gem uses Nokogiri to scrape the top player rankings from Rotogrinders overall grinders rankings page and then provides the user with a command line interface to choose a set of players to drill down more deeply into. The CLI then displays that set of players and allows the user to select a specific player to get more information about that player.

The gem was built using object oriented ruby. The player class handles the initialization of new players as well as the storage and access of individual player attributes. The scraper class uses Nokogiri to scrape the rankings page and then iterates over the Nokogiri node set calling the .new_from_index_page method from the player class to create a new player from each node. The CLI class handles the user interface. All this is encapsulated in DFSPlayerRankings module.

The project is also setup to allow for development experimentation via the console file. The setup file installs all dependencies and rake spec can be used to run any tests that the developer wants to run.

Finally, the gemspec file provides all the information needed for rubygems publishing, including information like name, version number, and a short description. The development dependencies and versions required are also listed in this file. 

Please feel free to give me any feedback via the GitHub repo, thanks for reading and checking out the app!

