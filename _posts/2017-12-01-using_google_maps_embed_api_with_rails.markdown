---
layout: post
title:      "Using Google Maps Embed API with Rails"
date:       2017-12-01 22:29:57 +0000
permalink:  using_google_maps_embed_api_with_rails
---


I recently built a web application on Rails to help users in the Katy, Texas area to locate maintained hiking trails nearby. As part of the application, I wanted users to be able to see a map of the trail and the surrounding area quickly. In order to accomplish this, I used the Google Maps Embed API.

The process was relatively simple, thanks to the ease of use of the API. Within the show page of my trails view, I simply added an iframe content tag, and within the tag set the source to `"https://www.google.com/maps/embed/v1/place?key=#{ENV['GOOGLE_MAPS_EMBED_API_KEY']}&q=#{@trail.name.gsub!(/\s/,'+')}+Trail,Houston+TX" `. I had already generated a key from the Google Maps Embed API developer page, and luckily for me most of the trails in the database where already mapped on Google Maps.

I did have to reformat the name of each trail slightly, in order to get the best possible search results from Google, but other than that, the process was relatively painless, and each trail that is added to the database can be quickly mapped without having to add any additional code.

The project demo is hosted on Heroku [here](https://katy-hiking-trails.herokuapp.com/), and the GitHub repo can be found [here](https://github.com/ChristopherJamesN/katy-hiking-trails).

Thanks for reading!


