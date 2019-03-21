<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/fs/FSL62VB6TJAX1551920284158.jpg">

# Match

### Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|The unique Integer identifier for a singel Overwatch League Match|
|`competitors`|Array of Competitor Objects|An Array containing the information of two competitng teams for an Overwatch League Match.|
|`scores`|Array of Int64|An array containing the currents scores for two Overwatch League Competitors respectively.|
|`conclusionValue`|Int64|The number of games for a single Overwatch League Match|
|`conclusionStrategy`|String|A string representation of an Overwatch League Match conclusion.|
|`winner`|Competitor Object|A Competitor object representing the winning team in an Overwatch League Match.|
|`home`|String|A string indicating the home location of a match.|
|`bracket`|Bracket Object|A Bracket Object which denotes the tournament infornation and stage information.|

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
    "rankings": [],
    "meta": {
        "strings": {
            "owl.matches.countdown.unit.days": "Days",
            "owl.matches.countdown.unit.hours": "Hrs",
            "owl.matches.countdown.unit.minutes": "Min",
            "owl.matches.maps.title.upcoming": "Match Preview",
            "owl.matches.maps.title.finished": "Match Summary",
            "owl.matches.game": "Game ##",
            "owl.matches.game.final": "Final",
            "owl.matches.game.final-ot": "Final (OT)",
            "owl.matches.game.overview": "Overview",
            "owl.matches.game.type": "## Map Set",
            "owl.matches.game.type.minimum": "{0} Map Set",
            "owl.matches.game.type.best-of": "Best of {0}",
            "owl.matches.game.result": "Game Result",
            "owl.matches.game.roster": "Roster",
            "owl.matches.pagination.previous": "Prev Match",
            "owl.matches.pagination.versus": "vs",
            "owl.matches.pagination.next": "Next Match",
            "owl.players.roles.tank": "Tank",
            "owl.players.roles.offense": "Damage",
            "owl.players.roles.defense": "Damage",
            "owl.players.roles.support": "Support",
            "owl.players.roles.flex": "Flex"
        }
    }
}
```