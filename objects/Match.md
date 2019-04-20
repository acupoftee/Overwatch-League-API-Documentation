<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/fs/FSL62VB6TJAX1551920284158.jpg">

# Match
An Overwatch League Match consists of 4 games taking place in four different maps and game modes. Matches are normally determined with a "Best of" conclusion strategy. 

### Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|The unique Integer identifier for a singel Overwatch League Match|
|`competitors`|Array of Competitor Objects|An Array containing the information of two competitng teams for an Overwatch League Match.|
|`scores`|Array of Score Objects|An array of 2 Integers representing the current match scores of both Competitors respectively. Each Score object contains a single `value` property, with the current score for a Competitor.|
|`conclusionValue`|Integer|An Integer denoting the conclusion value of a match. The conclusion value is the number of games to be played in a single Overwatch League match.|
|`conclusionStrategy`|String|A conclusion strategy determines how a match is concluded. For example, a minimum conclusion strategy determines a winner after the minimum number of games has been played in a match.|
|`state`|String|The current state of a Match.|
|`status`|String|The current state of a Match.|
|`game`|Array of Game Objects|A list of individual games taking place in a single Overwatch League match. Each game takes place on a different map.|
|`winner`|Competitor Object|A Competitor object representing the winning team in an Overwatch League Match.|
|`home`|String|A string indicating the home location of a Match.|
|`bracket`|Bracket Object|A Bracket Object which denotes the tournament infornation and stage information.|
|`dateCreated`|Int64|An Integer representing the date a Match was scheduled.|
|`handle`|String|The current game handle for Overwatch League match.|
|`competitorStatuses`|Array of Strings|A list of competitor statuses. A competitor status denotes whether or not a competitor is able to compete.|
|`timeZone`|String|The current time zone used to display the start time of a Match on overwatchleague.com|
|`actualStartDate`|Int64|An Integer representing the date and time a Match has started.|
|`actualEndDate`|Int64|An Integer representing the date and time a Match has ended.|
|`startDate`|Int64|An Integer representing the scheduled start date of a Match.|
|`endDate`|Int64|An Integer representing the scheduled end date of a Match.|
|`showStartDate`|Boolean|A Boolean indicating whether or not the match start date should be seen on overwatchleague.com.|
|`showEndDate`|Boolean|A Boolean indicating whether or not the match end date should be seen on overwatchleague.com.|
|`rankings`|Array of Player Objects|An array of Players sorted by stat rankings. Players are sorted in descending order.|

## Sample Match JSON
```json
{
    "id": 21211,
    "competitors": [
        {
            "id": 4524,
            "availableLanguages": [
                "en",
                "it",
                "ru",
                "ja",
                "zh-cn",
                "th",
                "ko",
                "es-mx",
                "pt",
                "fr",
                "zh-tw"
            ],
            "handle": "fusion.2056",
            "name": "Philadelphia Fusion",
            "homeLocation": "Philadelphia, PA",
            "primaryColor": "000000",
            "secondaryColor": "f99f29",
            "game": "OVERWATCH",
            "attributes": {
                "city": null,
                "hero_image": null,
                "manager": null,
                "team_guid": "0x0D70000000000009"
            },
            "attributesVersion": "1.0.0",
            "abbreviatedName": "PHI",
            "addressCountry": "US",
            "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/3JZTLCPH37QD1508792362853.png",
            "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/LAKZ6R7QEG6S1507822883033.svg",
            "players": [],
            "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/LAKZ6R7QEG6S1507822883033.svg",
            "type": "TEAM"
        },
        {
            "id": 4410,
            "availableLanguages": [
                "en",
                "ru",
                "ja",
                "zh-cn",
                "th",
                "ko",
                "es-es",
                "es-mx",
                "pt",
                "zh-tw",
                "fr",
                "it"
            ],
            "handle": "london.6950",
            "name": "London Spitfire",
            "homeLocation": "London",
            "primaryColor": "ff8200",
            "secondaryColor": "59cbe8",
            "game": "OVERWATCH",
            "attributes": {
                "city": null,
                "hero_image": null,
                "manager": null,
                "team_guid": "0x0D70000000000003"
            },
            "attributesVersion": "1.0.0",
            "abbreviatedName": "LDN",
            "addressCountry": "GB",
            "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/NW461AQIYQMK1508792363133.png",
            "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/HCS229B4DP021507822883016.svg",
            "players": [],
    ],
    "scores": [
        {
            "value": 3
        },
        {
            "value": 1
        }
    ],
    "conclusionValue": 4,
    "conclusionStrategy": "MINIMUM",
    "winner": {},
    "home": null,
    "state": "CONCLUDED",
    "status": "CONCLUDED",
    "statusReason": "NORMAL",
    "attributes": {},
    "games": [
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
        },
    ],
    "clientHints": [],
    "bracket": {},
    "dateCreated": 1544630140226,
    "flags": [],
    "handle": "match-7e9b4d15-169c-164d-8ea8-dc8879dd9b25",
    "competitorStatuses": [
        "NORMAL",
        "NORMAL"
    ],
    "timeZone": "America/Los_Angeles",
    "actualStartDate": 1550189390348,
    "actualEndDate": 1550194577428,
    "startDate": 1550188800000,
    "endDate": 1550194800000,
    "showStartTime": true,
    "showEndTime": true,
    "rankings": []
}
```