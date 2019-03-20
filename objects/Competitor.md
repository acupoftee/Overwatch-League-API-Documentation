<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/fz/FZEX5FAOR8J61549992684261.jpg">

# Competitors
A Competitor is an Overwatch League team competiting in the current season. 

## Competitor IDs
Each Competitor has a unique ID should a user look up information for a specific team. Below is a list of team IDs:

| Team                   | ID   |
|:---------------------- |:-----|
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/32/32MTX0PLEDY31542673991836.png" height="20"> Atlanta Reign | 7698 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/43UINMGMA83X1513383982827.png" height="20"> Boston Uprising  | 4402 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/st/STKSER89UHKO1542674031469.png" height="20"> Chengdu Hunters  | 7692 | 
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/NO44N7DDJAPF1508792362936.png" height="20"> Dallas Fuel | 4523 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/4GO273NATVWM1508792362854.png" height="20"> Florida Mayhem   | 4407 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/sz/SZQVDGE3F1TE1542674048320.png" height="20"> Guangzhou Charge | 7699 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/QW4QD06XJUZY1544055635729.png" height="20"> Hangzhou Spark   | 7693 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/gallery/2YF5VLIMGZVA1546557680222.png" height="20"> Houston Outlaws | 4525 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/NW461AQIYQMK1508792363133.png" height="20"> London Spitfire | 4410 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/3AEMOZZL76PF1508792362892.PNG" height="20"> Los Angeles Gladiators | 4406 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/0D8BNUWVZP6B1508792362890.PNG" height="20"> Los Angleles Valiant | 4405 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/9r/9RYLM8FICLJ01508818792450.png" height="20"> New York Excelsior | 4403 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/qm/QM7JE0THABVT1542674071412.png" height="20"> Paris Eternal | 7694 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/3JZTLCPH37QD1508792362853.png" height="20"> Philadelphia Fusion | 4524 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/YO24NN5KAOFL1508792362791.png" height="20"> San Francisco Shock | 4404 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/LHRSIW3NWH211508792362796.png" height="20"> Seoul Dynasty | 4409 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/B0R64QSNCDLX1508792362793.png" height="20"> Shanghai Dragons | 4408 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/g0/G05QL2P5A92E1542674081932.png" height="20"> Toronto Defiant | 7695 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/gallery/F1WE9LBKIGHD1543976752064.png" height="20"> Vancouver Titans | 7696 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/95UE5OJKSFQF1543968718489.png" height="20"> Washington Justice | 7697 |

## Competitor Data Dictionary
See [Team Data Dictionary](../README.md#team-data-dictionary)

| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`                   | Int64 | The unique integer identifier for the Overwatch League Team. Example: <br><br><pre lang="json">"id": 4523</pre>
|`divisionId` | Int64 | The unique integer identifier for the Team's Overwatch League [Division](objects/Division.md). Example:<br><br><pre lang="json">"divisionId": 80</pre>
|`handle` | String | A String representation of an Overwatch League team's handle. Example: <br><br><pre lang="json">"handle": "fuel.6990"</pre>
|`name` | String | A String representation of an Overwatch League team's name. Example: <br><br><pre lang="json">"name": "Boston Uprising"</pre>
|`abbreviatedName` | String | A String representation of an Overwatch League team's 3 letter abbreviated name. Example: <br><br><pre lang="json">"abbreviatedName": "ATL"</pre>
| `logo` | [Logo](Logo.md) Object | A Logo object containing an Overwatch League team's logo in SVG and PNG formats.|
|`hasFallback` | Boolean | Indicates whether or not a team has media queries which specific browsers cannot handle, such as logo files and headshot files. Example: <br><br><pre lang="json">"hasFallback": false</pre>
|`location` | String | A String representation of an Overwatch League team's base location. Example: <br><br><pre lang="json">"location": "Boston, MA"</pre>
| `players` | Array of [Player](objects/Player.md) Object |A Player roster for a competing Overwatch League Team. Additionally, see Player object for more info. |
|`website` | String | A String representation of an Overwatch League team's website url. Example: <br><br><pre lang="json">"website": "https://fuel.overwatchleague.com"</pre>
|`placement` | Int64 | The current standing of an Overwatch League Team. Example: <br><br><pre lang="json">"placement": 1</pre>
|`advantage` | Int64 | An integer indicating the advantage an Overwatch League Team has over its competitors. Example: <br><br><pre lang="json">"advantage": 0</pre>
| `records` | [Records](Records.md) Object | A Records object containing an Overwatch League team's league records. See Records object for more info.|

## Sample Competitor JSON
```json
{
    "data": {
        "id": 4523,
        "divisionId": 80,
        "handle": "fuel.6990",
        "name": "Dallas Fuel",
        "abbreviatedName": "DAL",
        "logo": {
            "main": {
                "svg": "https://bnetcmsus-a.akamaihd.net/cms/template_resource/YX6JZ6FR89LU1507822882865.svg",
                "png": "https://bnetcmsus-a.akamaihd.net/cms/page_media/NO44N7DDJAPF1508792362936.png"
            },
            "mainName": {
                "svg": "https://bnetcmsus-a.akamaihd.net/cms/page_media/Q8TMKNUFIJL51519747890664.svg",
                "png": "https://bnetcmsus-a.akamaihd.net/cms/page_media/Q8TMKNUFIJL51519747890664.svg"
            },
            "altDark": {
                "svg": "https://bnetcmsus-a.akamaihd.net/cms/page_media/LLMV1UTBVHN11544055825034.svg",
                "png": "https://bnetcmsus-a.akamaihd.net/cms/page_media/YUUL7E0CSF591544055626557.png"
            }
        },
        "hasFallback": false,
        "location": "Dallas, TX",
        "players": [],
        "colors": {
            "primary": {
                "color": "#032340",
                "opacity": 1
            },
            "secondary": {
                "color": "#0072CE",
                "opacity": 1
            },
            "tertiary": {
                "color": "#9EA2A2",
                "opacity": 1
            }
        },
        "accounts": [
            {
                "id": 2268,
                "type": "TWITTER",
                "url": "https://twitter.com/DallasFuel"
            },
            {
                "id": 2424,
                "type": "DISCORD",
                "url": "https://discord.gg/dallasfuel"
            },
            {
                "id": 2372,
                "type": "INSTAGRAM",
                "url": "https://www.instagram.com/DallasFuel"
            },
            {
                "id": 2267,
                "type": "FACEBOOK",
                "url": "https://www.facebook.com/TheDallasFuel"
            },
            {
                "id": 2269,
                "type": "YOUTUBE_CHANNEL",
                "url": "https://www.youtube.com/channel/UCj4XSmDqIhRT4frKzRTMyrA"
            }
        ],
        "website": "https://fuel.overwatchleague.com",
        "placement": 13,
        "advantage": 0,
        "records": {
            "matchWin": 1,
            "matchLoss": 1,
            "matchDraw": 0,
            "matchBye": 0,
            "gameWin": 3,
            "gameLoss": 5,
            "gameTie": 0,
            "gamePointsFor": 0,
            "gamePointsAgainst": 0,
            "comparisons": [
                {
                    "key": "MATCH_DIFFERENTIAL",
                    "value": 0
                },
                {
                    "key": "MATCH_GAME_DIFFERENTIAL",
                    "value": -2
                },
                {
                    "key": "GAME_HEAD_TO_HEAD_DIFFERENTIAL",
                    "value": null
                },
                {
                    "key": "MATCH_HEAD_TO_HEAD_DIFFERENTIAL",
                    "value": null
                },
                {
                    "key": "ADVANTAGE",
                    "value": 0
                }
            ]
        }
    },
    "meta": {
        "strings": {
            "owl.team.header.atlantic": "Atlantic",
            "owl.team.header.pacific": "Pacific",
            "owl.team.view-all": "View All",
            "owl.teams.recent-match-vods": "Recent Matches",
            "owl.team.header.social": "Social",
            "owl.team.header.w": "W",
            "owl.team.header.l": "L",
            "owl.standings.header.alt.division": "Division",
            "owl.team.league-standing": "League Standing",
            "owl.team.location": "Location",
            "owc.content-modules.round-robin.match-record": "Match Record",
            "owl.teams.roster.team-website": "Team Website",
            "owl.team.upcoming-matches": "Upcoming Matches",
            "owl.team.no-matches-scheduled": "No matches scheduled",
            "owl.matches.game.roster": "Roster",
            "owl.content-modules.recent-news.title": "Recent News",
            "owl.players.roles.offense": "Damage",
            "owl.players.roles.defense": "Damage",
            "owl.players.roles.tank": "Tank",
            "owl.players.roles.support": "Support",
            "owl.players.roles.flex": "Flex",
            "owl.schedule.today": "Today",
            "owl.schedule.match-details": "Match Details",
            "owl.labels.news": "News",
            "owl.labels.feature": "Feature",
            "owl.labels.announcement": "Announcement",
            "owl.labels.training": "Training",
            "owl.labels.path-to-pro": "Path to Pro",
            "owl.labels.highlight": "Highlight",
            "owl.labels.analysis": "Analysis"
        }
    }
}
```