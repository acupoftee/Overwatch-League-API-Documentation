# Bracket
A bracket represents a series of games played during an Overwatch League match usually leading to a single winner.

## Bracket Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|The Integer identifier of a Bracket.|
|`matchConclusionValue`|Int64|The maximum number of games in an Overwatch League match.|
|`matchConclusionStrategy`|String|The strategy used to clonclude an Overwatch League match.|
|`winners`|Int64|The number of winners in a single Bracket.|
|`teamSize`|Int64|The required team size for an Overwatch League Match.|
|`repeatableMatchUps`|Int64|The number of repeated match ups in a Bracket|
|`stage`|Stage Object|An object describing the current Stage for a Bracket.|
|`type`|String|Denotes the type of match in a Bracket.|
|`advantageComparing`|String|The moment in a match where Competitor advantages are evaluated.|
|`thirdPlaceMatch`|Boolean|A boolean indicating whether or not a third place match will take place.|
|`allowDraw`|Boolean|A boolean indicating whether or not a draw is allowed.|


## Sample Bracket JSON
```json
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
            "attributes": {
                "program": {
                    "environment": "prod",
                    "phase": "stage",
                    "season_id": "2019",
                    "stage": {
                        "format": "regular_season",
                        "number": 1
                    },
                    "type": "owl"
                }
            },
            "attributesVersion": "1.1.0",
            "subEvents": [
                {
                    "id": 24507,
                    "availableLanguages": [
                        "en"
                    ],
                    "tournament": {
                        "id": 5062
                    },
                    "name": "Stage 1/Week 1 - Sat. Feb 16th",
                    "startDate": 1550304000000,
                    "endDate": 1550304000000,
                    "showStartTime": true,
                    "showEndTime": true,
                    "timeZone": "America/Los_Angeles"
                },
            ],
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
}
```