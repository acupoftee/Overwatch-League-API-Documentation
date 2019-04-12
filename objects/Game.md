
<img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/rq/RQTO5OFDOFO11551381261494.jpg">

# Game
A game is a portion of an Overwatch League Match. A game is played on a single map.

## Game Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|The integer identifier for a game in an Overwatch League match.|
|`number`|Int64|The game/map number in an Overwatch League match.|
|`points`|Array of Int|An Array of two Integers representing the map score for each Competitor respectively.|
|`attributes`|Attribute Object|An object containing various attributes for the current Map.|
|`attributesVersion`|String|The current Map attribute version.|
|`players`|Array of Player Objects|An array of players currently playing in the game.|
|`state`|String|The current state of a game.|
|`status`|String|The current status of a game.|
|`handle`|String|The current game handle for Overwatch League streams.|
|`match`|Object|An Object containing an Integer id for a Match.|

## Sample Game JSON
```json
{
    "id": 20822,
    "number": 1,
    "points": [
        2,
        1
    ],
    "attributes": {
        "build": 54892,
        "instanceID": "05c00f0a08000002:03643ee6063d0343",
        "map": "ilios",
        "mapGuid": "0x080000000000066D",
        "mapScore": {
            "team1": 2,
            "team2": 1
        }
    },
    "attributesVersion": "0.5.0",
    "players": [],
    "state": "CONCLUDED",
    "status": "CONCLUDED",
    "statusReason": "NORMAL",
    "stats": null,
    "handle": "matchgame-9d7af953-d38d-ea4b-a215-0f6af2d08ec3",
    "match": {
        "id": 21211
    }
}
```