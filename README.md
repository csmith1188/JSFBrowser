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

<b>POST</b> /fighter

Create a fighter with the specified name and ID.

### Body Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
fightername | Required | String | The fighter name.
fighterID | Required | Integer | The fighter ID.

<b>GET</b> /fighter/list

List all of the fighters on the server.

### Sample Response

[
    {
        "fighter_UID": 1,
        "fighter_name": "SMC",
        "fighter_player_UID": 3,
        "stat_atk": 5,
        "stat_def": 5,
        "stat_tek": 5,
        "rec_wins": 0,
        "rec_losses": 0
    },
    {
        "fighter_UID": 2,
        "fighter_name": "undefined",
        "fighter_player_UID": "undefined",
        "stat_atk": 5,
        "stat_def": 5,
        "stat_tek": 5,
        "rec_wins": 0,
        "rec_losses": 0
    },
    {
        "fighter_UID": 3,
        "fighter_name": "aaron",
        "fighter_player_UID": "undefined",
        "stat_atk": 5,
        "stat_def": 5,
        "stat_tek": 5,
        "rec_wins": 0,
        "rec_losses": 0
    }
]

<b>GET</b> /fighter/show/{fighterUID}

Search for a fighter with the specified <b>{fighterUID}</b>.

### Path Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
fighterUID | Required | Integer | The fighter UID. Min is 1.

### Sample Response

{
    "fighter_UID": 1,
    "fighter_name": "SMC",
    "fighter_player_UID": 3,
    "stat_atk": 5,
    "stat_def": 5,
    "stat_tek": 5,
    "rec_wins": 0,
    "rec_losses": 0,
    "player_UID": 3,
    "player_name": "Mr. Smith"
}

# Player
The player.

## Methods
<b>GET</b> /player/list

List all of the players on the server.

### Sample Response

[
    {
        "player_UID": 3,
        "player_name": "Mr. Smith"
    }
]

<b>GET</b> /player/show/{playerUID}

Search for a player with the specified {playerUID}.

### Path Parameters

Parameter | Required/Optional | Data Type | Description
------------ | ------------- | ------------- | -------------
player | Required | Integer | The player UID.

### Sample Response

[
    {
        "fighter_UID": 1,
        "fighter_name": "SMC",
        "fighter_player_UID": 3,
        "stat_atk": 5,
        "stat_def": 5,
        "stat_tek": 5,
        "rec_wins": 0,
        "rec_losses": 0,
        "player_UID": 3,
        "player_name": "Mr. Smith"
    }
]
