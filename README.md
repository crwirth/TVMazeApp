# TVMaze Application

In this project, I completed a web application that is a front-end for the TVMaze API.

## Functionality

There are two main files:
- tvmaze.html
    - All the HTML for the application
- tvmaze.js
    - JavaScript for the application
    - populateShows() deals just with inserting the passed-in shows into the DOM. This makes this testable without having to have it tied to the code that gets data from the API
    - My handleSearch event handler ties the two together: it gets the search term, gets the shows using searchShows, and fills in the DOM with populateShows.
    - the getEpisodes function, which is given a show ID, returns an array of objects with basic information on the episodes for that show
    -  The populateEpisodes function , which is provided an array of episodes info, populates that into the #episodes-list part of the DOM. The episodes list is a simple <ul>, and the individual episodes are just basic <li> elements

You can type part of a TV show title into the search form and, on submission, it will return information about a hard coded show. It will show a series of cards with information on the show.

## Note how I have structured this code:

- By having a separate function for searchShows, you can test the “search API for shows” without having to do deal with anything related to the DOM in tests. This also makes this function re-usable if I built a different version of this app with a different front-end (like in React); we could re-use searchShows.

## Screenshot of Application

![Image of Application](https://github.com/crwirth/TVMazeApp/blob/master/Screen%20Shot%202020-02-10%20at%2012.28.55%20PM.png)


You can access the application here:

https://crwirth.github.io/TVMazeApp/
