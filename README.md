#JSFBrowser [v0.1.0]

Uses the "JSFDB API" to search and view players and fighters in the JSFighter Online Database (JSFDB)

JSFBrowser is written in [Nodejs](https://nodejs.org/en/), using [Express.js](https://expressjs.com/) and [PUG templating engine](https://pugjs.org/api/getting-started.html).

Can currently:

- List all players
- List all fighters
- List all fighters that belong to a player
- Create new fighters

# API Documentation
# Fighter
The fighter.

## Methods
<b>POST</b> /search

Search for fighters.

<b>POST</b> /add

Create a fighter with the specified name and ID.

### Body Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
fightername | Required | String | The fighter name.
fighterID | Required | Integer | The fighter ID.

<b>GET</b> /list/fighters

List all of the fighters on the server.

<b>GET</b> /fighter/{fighterUID}

Search for a fighter with the specified <b>{fighterUID}</b>.

### Path Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
fighterUID | Required | Integer | The fighter UID.

# Player
The player.

## Methods
<b>GET</b> /list/players

List all of the players on the server.

<b>GET</b> /player/{player}

Search for a specific {player}.

### Path Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
player | Required | String | The player name.
