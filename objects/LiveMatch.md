<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/fd/FDUJX118NC1A1533593512518.jpg">

# Live Match
A Live match is a match currently streamed on Overwatch League's streaming channels. 

## Live Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique Integer identifier for an ongoing match.|
|`competitors`|Array of Competitor Objects|An array of two Overwatch League teams competitng in an ongoing match.|
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


## Sample Live Match JSON
```json
 "liveMatch": {
            "id": 21236,
            "competitors": [
                {
                    "id": 7694,
                    "availableLanguages": [
                        "en",
                        "ko",
                        "zh-cn"
                    ],
                    "handle": "paris.5582",
                    "name": "Paris Eternal",
                    "homeLocation": "Paris",
                    "primaryColor": "303d56",
                    "secondaryColor": "8d042d",
                    "game": "OVERWATCH",
                    "abbreviatedName": "PAR",
                    "addressCountry": "FR",
                    "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/qm/QM7JE0THABVT1542674071412.png",
                    "icon": "https://bnetcmsus-a.akamaihd.net/cms/page_media/w4/W4C99JABL26E1542674142979.svg",
                    "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/page_media/w4/W4C99JABL26E1542674142979.svg",
                    "type": "TEAM"
                },
                {
                    "id": 4404,
                    "availableLanguages": [
                        "en",
                        "zh-tw",
                        "zh-cn",
                        "th",
                        "ko",
                        "ru",
                        "ja",
                        "pt"
                    ],
                    "handle": "san-francisco.3862",
                    "name": "San Francisco Shock",
                    "homeLocation": "San Francisco, CA",
                    "primaryColor": "75787b",
                    "secondaryColor": "fc4c02",
                    "game": "OVERWATCH",
                    "abbreviatedName": "SFS",
                    "addressCountry": "US",
                    "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/YO24NN5KAOFL1508792362791.png",
                    "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/0SY7LHKHV86R1507822883113.svg",
                    "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/0SY7LHKHV86R1507822883113.svg",
                    "type": "TEAM"
                }
            ],
            "scores": [
                {
                    "value": 0
                },
                {
                    "value": 2
                }
            ],
            "conclusionValue": 4,
            "conclusionStrategy": "MINIMUM",
            "home": null,
            "state": "IN_PROGRESS",
            "status": "IN_PROGRESS",
            "statusReason": "NORMAL",
            "attributes": {},
            "games": [],
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
            "dateCreated": 1544630150124,
            "flags": [],
            "handle": "match-cb2d0345-1548-7d47-a956-fd39724611c5",
            "hyperlinks": [],
            "competitorStatuses": [
                "NORMAL",
                "NORMAL"
            ],
            "timeZone": "America/Los_Angeles",
            "actualStartDate": 1552244691303,
            "startDate": "2019-03-10T19:00:00.000Z",
            "endDate": "2019-03-10T20:30:00.000Z",
            "showStartTime": true,
            "showEndTime": true,
            "startDateTS": 1552244400000,
            "endDateTS": 1552249800000,
            "youtubeId": "",
            "wins": [
                0,
                2
            ],
            "ties": [
                1,
                1
            ],
            "losses": [
                2,
                0
            ],
            "videos": [
                {
                    "name": 1,
                    "description": "",
                    "vodLink": "",
                    "youtubeId": "",
                    "thumbnailUrl": ""
                }
            ],
            "timeToMatch": 3996218,
            "liveStatus": "LIVE"
        }
```