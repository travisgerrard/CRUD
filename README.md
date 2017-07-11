Demo CRUD document

Created with create-react-app

index.js
The entry way
Where we put all our critical dependencies

App.js
Renders the main page.
Defines all out paths, and loads them...

GamesPage.js
Connects to react
Fetches all games
Calls delete games
Renders GamesList

GamesList.js
given games array, loads the list with MapFx and then makes gameCard out of eatch entry
Connects to actions.js to carry out actions! (fetch, delete)

GameCard.js
Display element for each item in GamesList

GameFormPage.js
Handler for the form,
If editing, then pass props of editing game, vs null if new game (as discovered in mapStateToProps if it exists or not)
When "Save" button pressed, if exists updates, vs creating new
Connects to actions.js to carry out actions (save, fetch, update)

GameForm.js
The creation on updating form
Info controlled by GameFormPage
Error validation/handling for unfilled entries
Calls saveGame from gameformpage, with returns values, and then .catch catches any errors
Uses classnames module to help dynamically change css depending on state
[array.value] returns the string of the .value in ES6

actions.js
Makes calls to server with functions....

games.js
Imports actions.js
Tells redux how to handle actions to server on client side.
