# Bracket
A bracket represents a series of games played during an Overwatch League match usually leading to a single winner.

## Bracket Data Dictionary

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