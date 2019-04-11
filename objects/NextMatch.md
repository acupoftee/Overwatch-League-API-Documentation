# Next Match 
The Next Match object is next live match to be streamed on Overwatch League's streaming channels. 

## Next Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique Integer identifier for an upcoming match.|
|`competitors`|Array of Competitor Objects|An array of two Overwatch League teams competitng in an upcoming match.|
|`scores`|Array of Score Objects|An array of 2 Integers representing the current match scores of both Competitors respectively. Each Score object contains a single `value` property, with the current score for a Competitor.|
|`conclusionValue`|Integer|An Integer denoting the conclusion value of a match. The conclusion value is the number of games to be played in a single Overwatch League match.|
|`conclusionStrategy`|String|A conclusion strategy determines how a match is concluded. For example, a minimum conclusion strategy determines a winner after the minimum number of games has been played in a match.|
|`state`|String|The current state of an Overwatch League match.|
|`status`|String|The current state of an Overwatch League match.|
|`game`|Array of Game Objects|A list of individual games taking place in a single Overwatch League match. Each game takes place on a different map.|
|`bracket`|Bracket Object|Denotes the current bracket for both Competitors.|
|`dateCreated`|Int64|An Integer representation of the date the match alert was created.|
|`handle`|String|The String representation of the match's handle.|
|`hyperlinks`|Array of Hyperlink Objects|An array of Hyperlink objects for all available streaming platforms for an Overwatch League match.|
|`competitorStatuses`|Array of Strings|A list of competitor statuses.|
|`timeZone`|String|The time zone used for the Overwatch League schedule.|
|`startDateTS`|Int64|The Integer time string representing the start date of a match.|
|`endDateTS`|Int64|The Integer time string representing the end date of a match.|
|`youtubeId`|String|The String identifier for a concluded match posted on YouTube.|
|`wins`|Array of Int64|An Integer array containing the number of wins for each Competitor respectively.|
|`ties`|Array of Int64|An Integer array containing the number of ties for each Competitor respectively.|
|`losses`|Array of Int64|An Integer array containing the number of losses for each Competitor respectively.|
|`videos`|Array of String|A String array containing URL links for an Overwatch League match.|
|`startDateTS`|Int64|The Integer time string representing the time until an upcoming match.|
|`liveStatus`|String|The Integer time string representing the start date of a match.|


## Sample Next Match JSON
```json
"nextMatch": {
        "id": 21266,
        "competitors": [
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
                "abbreviatedName": "LDN",
                "addressCountry": "GB",
                "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/NW461AQIYQMK1508792363133.png",
                "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/HCS229B4DP021507822883016.svg",
                "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/HCS229B4DP021507822883016.svg",
                "type": "TEAM"
            },
            {
                "id": 4408,
                "availableLanguages": [
                    "en",
                    "zh-tw",
                    "es-mx",
                    "ru",
                    "ja",
                    "th",
                    "zh-cn",
                    "es-es",
                    "ko",
                    "pt"
                ],
                "handle": "shanghai.1319",
                "name": "Shanghai Dragons",
                "homeLocation": "Shanghai",
                "primaryColor": "d22630",
                "secondaryColor": "000000",
                "game": "OVERWATCH",
                "abbreviatedName": "SHD",
                "addressCountry": "CN",
                "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/B0R64QSNCDLX1508792362793.png",
                "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/ZIVUVIWXNIFL1507822883114.svg",
                "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/ZIVUVIWXNIFL1507822883114.svg",
                "type": "TEAM"
            }
        ],
        "scores": [
            {
                "value": 0
            },
            {
                "value": 0
            }
        ],
        "conclusionValue": 4,
        "conclusionStrategy": "MINIMUM",
        "home": null,
        "state": "PENDING",
        "status": "PENDING",
        "statusReason": "NORMAL",
        "attributes": {},
        "games": [
            {
                "id": 20834,
                "number": 1,
                "attributes": {
                    "map": "nepal",
                    "mapGuid": "0x08000000000004B7"
                },
                "attributesVersion": "0.5.0",
                "state": "PENDING",
                "status": "PENDING",
                "statusReason": "NORMAL",
                "stats": null,
                "match": {
                    "id": 21266
                }
            }
        ],
        "clientHints": [],
        "bracket": {
            "id": 4671,
            "matchConclusionValue": 4,
            "matchConclusionStrategy": "MINIMUM",
            "winners": 8,
            "teamSize": 6,
            "repeatableMatchUps": 0,
            "stage": {
                "id": 6391,
                "availableLanguages": [
                    "en"
                ],
                "tournament": {
                    "id": 5062,
                    "availableLanguages": [
                        "en"
                    ],
                    "game": "OVERWATCH",
                    "featured": false,
                    "draft": false,
                    "handle": "tournament-9623163a-0f68-9b4e-b84e-c36788117572",
                    "title": "Overwatch League Stage 1",
                    "series": {
                        "id": 181
                    }
                }
            },
            "type": "OPEN_MATCH",
            "clientHints": [],
            "advantageComparing": "AFTER_MATCH",
            "thirdPlaceMatch": false,
            "allowDraw": false
        },
        "dateCreated": 1544630150250,
        "flags": [],
        "handle": "match-e95217ab-4d43-fe4b-9868-b3f8dd13ce97",
        "hyperlinks": [
            {
                "id": 7550,
                "contentLanguage": "en",
                "type": "TWITCH_ACCOUNT",
                "value": "https://www.twitch.tv/overwatchleague",
                "arguments": {
                    "account": "overwatchleague"
                }
            }
        ],
        "competitorStatuses": [
            "NORMAL",
            "NORMAL"
        ],
        "timeZone": "America/Los_Angeles",
        "startDate": "2019-03-10T20:30:00.000Z",
        "endDate": "2019-03-10T22:00:00.000Z",
        "showStartTime": true,
        "showEndTime": true,
        "startDateTS": 1552249800000,
        "endDateTS": 1552255200000,
        "youtubeId": "",
        "wins": [
            0,
            0
        ],
        "ties": [
            0,
            0
        ],
        "losses": [
            0,
            0
        ],
        "videos": [],
        "timeToMatch": 1403782,
        "liveStatus": "UPCOMING"
    }
}
```