---
layout: post
title:      "Building a NBA News Feed with React-Redux"
date:       2017-10-27 17:26:10 -0400
permalink:  building_a_nba_news_feed_with_react-redux
---

For my final project, I wanted to build a NBA news feed that allows users to view the most update to date NBA news as well as take and save notes on the news as it is reported.

The application has one HTML page that is used to render the react-redux application. React-bootstrap is used to provide styling for the application.

The application contains two container components, a news list container, which contains a news list component that displays the latest NBA related news. The application also contains a notes component, which contains a notes list component of all the notes that a user has created relating to any selected news story.

The application also includes 5 stateless components. A news list component, which is made up of individual news components, and a notes list component that is made up of multiple notes components. A text field component is used to build the individual notes components.

React-router is used to provide the user with routes to create a new note, view and edit an existing note, and to view an individual news item.

Rails is used to handle all data persistence, and fetch() is used within all actions to GET and POST data from the Rails API.

