#JSFBrowser [v0.1.0]

Uses the "JSFDB API" to search and view players and fighters in the JSFighter Online Database (JSFDB)

JSFBrowser is written in [Nodejs](https://nodejs.org/en/), using [Express.js](https://expressjs.com/) and [PUG templating engine](https://pugjs.org/api/getting-started.html).

Can currently:

- List all players
- List all fighters
- List all fighters that belong to a player
- Create new fighters

Look, I said it did it. Not did it well.

# Fighter
The fighter.

## Methods
<b>POST</b> /search

Searches for a specific fighter.

<b>POST</b> /add {fightername}{fighterID}

Creates a new fighter with the specified name and ID.

<b>GET</b> /list/fighters

Lists all of the fighters on the server.

<b>GET</b> /fighter/{fighterUID}

Searches for a fighter with the specified ID.

# Player
The player.

## Methods
<b>GET</b> /list/players

Lists all of the players on the server.

<b>GET</b> /player/{player}

Searches for a player with the specified name.
