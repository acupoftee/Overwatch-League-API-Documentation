<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/sd/SDUN2UM5NL751550705773905.jpg">

# Players

A Player is a member of a competing Overwatch League team. 

## Player Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique integer identifier for an Overwatch League Player|
|`availableLanguages`|Array of Strings object|An array of language abbreviations indicating the avaliable languas for player information.|
|`handle`|String|The name of the Player's Battle.net account.|
|`name`|String|The Player's Overwatch username.|
|`homeLocation`|String|The Player's hometown.|
|`accounts`|Array of Account objects|An array containing all of the Player's social media accounts.|
|`game`|String|The name of the game associated with the Player.|
|`attributes`|Attribute Object|An Object containing information about a Player's most played heroes, player number, preferred slot, and role.|
|`attributesVersion`|String|A String representation of the attribute version.|
|`familyName`|String|The Player's last name.|
|`givenName`|String|The Player's first name.|
|`nationality`|String| A two letter abbrevition denoting the player's home country.|
|`headshot`|String|A String represenation of a Player's headshot URL.|
|`teams`|Array of [Competitor](Competitor.md) Objects|An array of the Player's teams|
|`stats`|Object|An object consisting of the Players average stats per 10 minutes(i.e.  eliminations, deaths, hero damage, healing, final blows), total time played in the Overwatch League, and top heroes.|
|`statRank`|Stats Object|An object consisting of the Players stat ranks. Ranked stats include stats per 10 minutes (i.e.  eliminations, deaths, hero damage, healing, final blows) and total time played in the Overwatch League.|
|`team`|[Competitor](Competitor.md) Object|An object consisting of the Player's Team information.

## Sample Player JSON
```json
{
    "data": {
        "player": {
            "id": 3380,
            "availableLanguages": [
                "en"
            ],
            "handle": "taimou.6010",
            "name": "Taimou",
            "homeLocation": "Juankoski",
            "accounts": [
                {
                    "id": 6422,
                    "competitorId": 3380,
                    "value": "https://www.twitch.tv/TaimouTv",
                    "accountType": "TWITCH",
                    "isPublic": true
                },
                {
                    "id": 6349,
                    "competitorId": 3380,
                    "value": "https://www.youtube.com/channel/UC8jnvzv_KW1ChKtdQYZUeAw",
                    "accountType": "YOUTUBE_CHANNEL",
                    "isPublic": true
                },
                {
                    "id": 6358,
                    "competitorId": 3380,
                    "value": "https://twitter.com/DF_Taimou",
                    "accountType": "TWITTER",
                    "isPublic": true
                },
                {
                    "id": 13241,
                    "competitorId": 3380,
                    "value": "https://www.facebook.com/Taimouu",
                    "accountType": "FACEBOOK",
                    "isPublic": true
                },
                {
                    "id": 13242,
                    "competitorId": 3380,
                    "value": "https://www.instagram.com/taimou_",
                    "accountType": "INSTAGRAM",
                    "isPublic": true
                }
            ],
            "game": "OVERWATCH",
            "attributes": {
                "hero_image": null,
                "heroes": [
                    "mccree",
                    "widowmaker",
                    "roadhog"
                ],
                "hometown": null,
                "player_number": 13,
                "preferred_slot": "1",
                "role": "offense"
            },
            "attributesVersion": "1.0.0",
            "familyName": "Kettunen",
            "givenName": "Timo",
            "nationality": "FI",
            "headshot": "https://bnetcmsus-a.akamaihd.net/cms/gallery/DFRBV085AX601550194285520.png",
            "teams": [
                {
                    "team": {
                        "id": 4523,
                        "availableLanguages": [
                            "en",
                            "ru",
                            "ja",
                            "zh-tw",
                            "zh-cn",
                            "th",
                            "ko"
                        ],
                        "handle": "fuel.6990",
                        "name": "Dallas Fuel",
                        "homeLocation": "Dallas, TX",
                        "primaryColor": "0c2340",
                        "secondaryColor": "0072ce",
                        "accounts": [
                            {
                                "id": 2268,
                                "competitorId": 4523,
                                "value": "https://twitter.com/DallasFuel",
                                "accountType": "TWITTER",
                                "isPublic": true
                            },
                            {
                                "id": 2424,
                                "competitorId": 4523,
                                "value": "https://discord.gg/dallasfuel",
                                "accountType": "DISCORD",
                                "isPublic": true
                            },
                            {
                                "id": 2372,
                                "competitorId": 4523,
                                "value": "https://www.instagram.com/DallasFuel",
                                "accountType": "INSTAGRAM",
                                "isPublic": true
                            },
                            {
                                "id": 2267,
                                "competitorId": 4523,
                                "value": "https://www.facebook.com/TheDallasFuel",
                                "accountType": "FACEBOOK",
                                "isPublic": true
                            },
                            {
                                "id": 2269,
                                "competitorId": 4523,
                                "value": "https://www.youtube.com/channel/UCj4XSmDqIhRT4frKzRTMyrA",
                                "accountType": "YOUTUBE_CHANNEL",
                                "isPublic": true
                            }
                        ],
                        "game": "OVERWATCH",
                        "attributes": {
                            "city": null,
                            "hero_image": null,
                            "manager": null,
                            "team_guid": "0x0D70000000000002"
                        },
                        "attributesVersion": "1.0.0",
                        "divisions": [
                            {
                                "competitor": {
                                    "id": 4523
                                },
                                "division": {
                                    "id": 61
                                }
                            },
                            {
                                "competitor": {
                                    "id": 4523
                                },
                                "division": {
                                    "id": 80
                                }
                            }
                        ],
                        "abbreviatedName": "DAL",
                        "addressCountry": "US",
                        "logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/NO44N7DDJAPF1508792362936.png",
                        "icon": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/YX6JZ6FR89LU1507822882865.svg",
                        "secondaryPhoto": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/YX6JZ6FR89LU1507822882865.svg",
                        "type": "TEAM"
                    },
                    "player": {
                        "id": 3380,
                        "type": "PLAYER"
                    },
                    "flags": []
                }
            ],
            "type": "PLAYER"
        },
        "stats": {
            "all": {
                "eliminations_avg_per_10m": 0,
                "deaths_avg_per_10m": 0,
                "hero_damage_avg_per_10m": 0,
                "healing_avg_per_10m": 0,
                "ultimates_earned_avg_per_10m": 0,
                "final_blows_avg_per_10m": 0,
                "time_played_total": 0
            },
            "heroes": []
        },
        "statRanks": {
            "eliminations_avg_per_10m": null,
            "deaths_avg_per_10m": null,
            "hero_damage_avg_per_10m": null,
            "healing_avg_per_10m": null,
            "ultimates_earned_avg_per_10m": null,
            "final_blows_avg_per_10m": null,
            "time_played_total": null
        },
        "team": {},
    "meta": {}
}
```