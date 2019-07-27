<p align=center>
<img src="tracer.png", width="50%">
  </p>

 <h1 align=center>Overwatch League API Community Documentation </h1>
<p align=center>A community analysis of the Overwatch League API.

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
</p>

# Disclaimer
The Overwatch League API is not officially supported by Blizzard, and is subject to change at any time. The documentation for the API is  developed by the community, and may or may not be complete. [Use at your own risk](https://i.imgur.com/Yr6WHNn.png).

# Contributing
<a href="https://discord.gg/PBwan6u">Join our **Unofficial Discord Server**</a> you want to contribute, ask questions, or share projects using the OWL API!

You can also create an issue or a PR. Before creating an issue,please ensure that it hasn't already been reported/suggested, and double-check the documentation.
See the <a href=".github/Contributing.md">contribution guide</a> if you'd like to submit a PR.

Let's get in touch on [Twitter](https://twitter.com/dustybuttongg) or Discord if you have any questions or comments!

# Getting Started
The Overwatch League is on a mission to celebrate fans and afford them opportunities to become champions through a professional esports ecosystem that embraces passion and rewards excellence. This API enables developers to have real time information about teams, players, match updates, and much more!


### The API is a RESTful Resource
Overwatch League API endpoints conform to the design principles of Representational State Transfer (REST). This API uses the JSON data format for responses.

### The API is HTTP-based over SSL
A GET request is required to retrieve data from the Overwatch League API.
Methods that submit, change or destroy data require a POST. A DELETE request is also accepted for methods that destroy data. API methods that require a particular HTTP method will return an error if not invoked using the correct endpoint or style. 

# Root URL
You can access the base API here at 
https://api.overwatchleague.com (China: https://api.overwatchleague.cn). Upon entering you'll see the following easter egg:

```
GET /

{
    "the world": "could always use more heroes"
}
```

# API Endpoints Overview
Here are the endpoints used to access Overwatch League's information such as player information, match updates, league standings, news reports, and much more. This document will be going over these objects in more detail.

## Endoints and Objects

### User Endpoints
[GET /login](#get-login) <br>
[GET /auth/bnet/callback?code=:code](#get-authbnetcallbackcodecode)<br>
[GET /user](#get-user)<br>
[GET /user/favorites](#get-userfavorites)<br>
[POST /user/favorites](#post-userfavorites)<br>
[POST /user/favorites/order](#post-userfavoritesorder)<br>
[DELETE /user/favorites/:id](#delete-userfavoritesid)<br>

### Team Endpoints
[GET /v2/teams](#get-v2teams) <br>
[GET /v2/teams/:id](#get-v2teamsid)<br>
[GET /ranking](#get-ranking)<br>
[GET /standings](#get-standings)<br>

### Player Endpoints
[GET /players](#get-players)<br>
[GET /players/:id](#get-playersid)<br>

### Match Endpoints
[GET /matches](#get-matches)<br>
[GET /matches/:id](#get-matchesid)<br>
[GET /live-match](#get-live-match)<br>
[GET /schedule](#get-schedule)<br>
[GET /streams](#get-streams)<br>
[GET /vods](#get-vods)<br>
[GET /maps](#get-maps)<br>
[GET /news](#get-news)<br>

### Additonal Endpoints
GET /playlist/owl-app-playlist<br>
GET /about<br>

### Objects
* [Account](/objects/Account.md)
* [Blog](objects/Blog.md)
* [Bracket](objects/Bracket.md)
* [Colors](objects/Colors.md)
* [Competitor](objects/Competitor.md)
* [Game](objects/Game.md)
* [Game Mode](objects/GameMode.md)
* [Live Match](objects/LiveMatch.md)
* [Logo](objects/Logo.md)
* [Match](objects/Match.md)
* [Next Match](objects/NextMatch.md)
* [Player](objects/Player.md)
* [Records](objects/Records.md)
* [VOD](objects/VOD.md)

## Endpoint Locales
Reponses can be returned in several locales (a language and region identidier). The data will then be returned in the specified language.
* Locales
  * `de_DE` - German
  * `en_US` - English (United States)
  * `en_GB` - English (Great Britain)
  * `es_ES` - Spanish (Spain)
  * `es_MX` - Spanish (Mexico)
  * `fr_FR` - French
  * `it_IT` - Italian
  * `pt_BR` - Portuguese
  * `pl_PL` - Polish
  * `ru_RU` - Russian
  * `ko_KR` - Korean
  * `ja_JP` - Japanese
  * `zh_TW` - Chinese (Taiwan)
  * `zh_CH` - Chinese (China)
    * It is recommended to use the root URL for China listed above.
# API Endpoint Guides
Here this guide will go over in detail each use of the above endpoints.

## Authentication Endpoints
The following endpoints involve authenticating a Battle.net account, and authorizatino code use: 
### GET /login
* Redirects clients to the Battle.net login page. 
* **NOTE**: This may direct you to a page that cannot be opened by your browser if you are already logged into your Battle.net account.
  
### GET /auth/bnet/callback?code=:code
* Callback 
* `code` - Battle.net authorization code

## User Endpoints
The following endpoints retrieve user information.

### GET /user
* Returns Uaer info. Token required.

### GET /user/favorites
* Returns the User's favorite Overwatch League Teams. 

### POST /user/favorites
* Adds an Overwatch League Team to a User's Favorite Teams collection.
```
POST /user/favorites
{
  "id" : "4525",
  "tags" : [
    "owl"
  ],
  "franchise" : "overwatch"
}
```
### POST /user/favorites/order
* Updates the order of the User's favorite teams.
```
POST /user/favorites/order
{
    "ids": [
        "4525"
    ]
}
```

### DELETE /user/favorites/:id
Deletes a favorite team from a User.

## Team Endpoints
The following endpoints retrieve information for Overwatch League Teams. 

### <a name="team-ids">Team IDs</a>
Each Overwatch League Team has a unique integer identifier (ID) which can be found upon visiting each team page on https://overwatchleague.com. For example, at the end of this URL is the ID for [Atlanta Reign](https://overwatchleague.com/en-us/teams/7698):

`https://overwatchleague.com/en-us/teams/7698`

We see that Atlanta Reign's ID following `/teams/` is `7698`. We can use this to retrieve information about Atlanta Reign's players, statistics, and more.

Below is a table of all team IDs for retrieving information for specific teams: 

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
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/0D8BNUWVZP6B1508792362890.PNG" height="20"> Los Angeles Valiant | 4405 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/9r/9RYLM8FICLJ01508818792450.png" height="20"> New York Excelsior | 4403 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/qm/QM7JE0THABVT1542674071412.png" height="20"> Paris Eternal | 7694 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/3JZTLCPH37QD1508792362853.png" height="20"> Philadelphia Fusion | 4524 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/YO24NN5KAOFL1508792362791.png" height="20"> San Francisco Shock | 4404 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/LHRSIW3NWH211508792362796.png" height="20"> Seoul Dynasty | 4409 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/B0R64QSNCDLX1508792362793.png" height="20"> Shanghai Dragons | 4408 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/g0/G05QL2P5A92E1542674081932.png" height="20"> Toronto Defiant | 7695 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/gallery/F1WE9LBKIGHD1543976752064.png" height="20"> Vancouver Titans | 7696 |
| <img src="https://bnetcmsus-a.akamaihd.net/cms/page_media/95UE5OJKSFQF1543968718489.png" height="20"> Washington Justice | 7697 |


### GET /v2/teams
Returns all competing Overwatch League teams.

#### Teams Data Dictionary 

| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`                   | Int64 | The unique integer for this League season. Example: <br><br><pre lang="json">"id": 61</pre>
|`availableLanguages`   |Array of String| Indicates a list of country and language codes. Example:<br><br><pre lang="json">"availableLanguages": ["en", "en-gb", "es-mx", "es-es", "pt", "de", "fr", "it", "pl", "ru", "ja", "ko", "zh-tw", "zh-cn"]</pre><i>Languages: Engish, English (Great Britian), Spanish (Mexico), Spanish (Spain), Portuguese, German, French, Italian, Polish, Russian, Japanese, Korean, Chinese (Taiwan), Chinease (China)</i><br><br>
|`name`               |  String| The name of the League. Example:<br><br><pre lang="json">"name": "The Overwatch League"</pre>
|`description`         | String | A summary of the Overwatch League. Example: <br><br><pre lang="json">"description": "The Overwatch League is on a mission to celebrate fans and afford them opportunities to become champions through a professional esports ecosystem that embraces passion and rewards excellence."</pre>
|`competitors`          | Array of [Competitor](/objects/Competitor.md) Object | Competitors are Overwatch League Teams competing in the current Overwatch League Season. Additionally, see Competitor Object for more info.
|`game`                 | String | The String representation of the game being played. Example: <br><br><pre lang="json">"game": "OVERWATCH"</pre> |
|`logo`  | String | A URL leading to the Overwatch League Logo. Example: <br><br><pre lang="json">"logo": "https://bnetcmsus-a.akamaihd.net/cms/page_media/JEUWQ6CN33BR1507857496436.svg"</pre>
|`competitorType` | String| Describes the type of Competitors competing in the Overwatch League. Example:<br><br><pre lang="json">"competitorType": "TEAM"</pre>
| `owl_division` | Array of Division Objects | The Divisions making up the Overwatch League. Example:<br><br><pre lang="json">owl_divisions": [<br>&thinsp;{<br>&emsp;&emsp;&emsp;"id": "79",<br>&emsp;&emsp;&emsp;"string": "owl.teams.divisions.atlantic",<br>&emsp;&emsp;&emsp;"name": "Atlantic Division",<br>&emsp;&emsp;&emsp;"abbrev": "ATL"<br>&thinsp;},<br>&thinsp;{<br>&emsp;&emsp;&emsp;"id": "80",<br>&emsp;&emsp;&emsp;"string": "owl.teams.divisions.pacific",<br>&emsp;&emsp;&emsp;"name": "Pacific Division",<br>&emsp;&emsp;&emsp;"abbrev": "PAC"<br>&thinsp;}<br>]</pre>

### GET /v2/teams/:id
Returns information for a single Overwatch League Team given a [Team ID](#team-ids). For exmaple, to retrieve information about Boston Uprising we can add Boston Uprising's ID at the end of the URL:

`https://api.overwatchleague.com/v2/teams/4402`
### Team Data Dictionary 

| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`                   | Int64 | The unique integer identifier for the Overwatch League Team. Example: <br><br><pre lang="json">"id": 4523</pre>
|`divisionId` | Int64 | The unique integer identifier for the Team's Overwatch League Division. The Atlanatic Division has an id of 79, and the Pacific Division's id is 80.  Example:<br><br><pre lang="json">"divisionId": 80</pre>
|`handle` | String | A String representation of an Overwatch League team's handle. Example: <br><br><pre lang="json">"handle": "fuel.6990"</pre>
|`name` | String | A String representation of an Overwatch League team's name. Example: <br><br><pre lang="json">"name": "Boston Uprising"</pre>
|`abbreviatedName` | String | A String representation of an Overwatch League team's 3 letter abbreviated name. Example: <br><br><pre lang="json">"abbreviatedName": "ATL"</pre>
| `logo` | [Logo](objects/Logo.md) Object | A Logo object containing an Overwatch League team's logo in SVG and PNG formats.|
|`hasFallback` | Boolean | Indicates whether or not a team has media queries which specific browsers cannot handle, such as logo files and headshot files. Example: <br><br><pre lang="json">"hasFallback": false</pre>
|`location` | String | A String representation of an Overwatch League team's base location. Example: <br><br><pre lang="json">"location": "Boston, MA"</pre>
| `players` | Array of [Player](objects/Player.md) Object |A Player roster for a competing Overwatch League Team. Additionally, see [Player Object](objects/Player.md) for more info. |
|`website` | String | A String representation of an Overwatch League team's website url. Example: <br><br><pre lang="json">"website": "https://fuel.overwatchleague.com"</pre>
|`placement` | Int64 | The current standing of an Overwatch League Team. Example: <br><br><pre lang="json">"placement": 1</pre>
|`advantage` | Int64 | An integer indicating the advantage an Overwatch League Team has over its competitors. Example: <br><br><pre lang="json">"advantage": 0</pre>
| `records` | [Records](objects/Records.md) Object | A Records object containing an Overwatch League team's league records. See Records object for more info.|

### GET /ranking
Returns an Array of Competitors ordered by placement in the Overwatch League.

### Ranking Data Dictionary 

| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
| `content`           | Array of [Competitor](objects/Competitor.md) Object| An Array of Competitors competing in the current Overwatch League Season
| `comparisons`| Array of String| An Array containing the differentials used to rank all Overwatch League Competitors. Example:<br><br><pre lang="json">"comparisons": [<br>"MATCH_DIFFERENTIAL",<br>"MATCH_GAME_DIFFERENTIAL",<br>"GAME_HEAD_TO_HEAD_DIFFERENTIAL", <br>"MATCH_HEAD_TO_HEAD_DIFFERENTIAL", <br>"ADVANTAGE"<br>]</pre>|
|`totalMatches`|Int64| Total numbers of matches to be played in the current Overwatch League season. Example:<br><br><pre lang="json"> "totalMatches": 280</pre>|
|`matchesConcluded`|Int64|The number of matches that have been played in the current Overwatch League season. Example:<br><br><pre lang="json"> "matchesConcluded": 16</pre>|
|`playoffCutoff`|Int64|The number of teams eligible to compete in the Overwatch League Playoffs. Example:<br><br><pre lang="json">"playoffCutoff": 6</pre>

### GET /standings
Returns an Array of Competitors ordered by placement in the Overwatch League.

### Standings Data Dictionary 

| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`owl_divisions`|Array of Division Object| Contains all the divisions for the current Overwatch League Season. Example:<br><br><pre lang="json">owl_divisions": [<br>&thinsp;{<br>&emsp;&emsp;&emsp;"id": "79",<br>&emsp;&emsp;&emsp;"string":&emsp;"owl.teams.divisions.atlantic",<br>&emsp;&emsp;&emsp;"name": "Atlantic Division",<br>&emsp;&emsp;&emsp;"abbrev": "ATL"<br>&thinsp;},<br>&thinsp;{<br>&emsp;&emsp;&emsp;"id": "80",<br>&emsp;&emsp;&emsp;"string":&emsp;"owl.teams.divisions.pacific",<br>&emsp;&emsp;&emsp;"name": "Pacific Division",<br>&emsp;&emsp;&emsp;"abbrev": "PAC"<br>&thinsp;}<br>]</pre>
|`playoff_separators`|Array of Int64| An Array of Integers indicating the stages for the current season of the Overwatch League Playoffs|
|`season`|Array of [Competitor](/objects/Competitor.md) Objects|A season is comprised of Competitors organized in Divisions. This will return two groups of Competitor arrays inside a parent Division object.|
|`ranks`|Array of [Competitor](/objects/Competitor.md) Objects|An Array of Competitors sorted by current standinds in the Overwatch League. Comparison values include match differentials, match game differentials, game head to head differentials, match head to head differentials, and advantage.


## Player Endpoints
The following endpoints retrieve information for Overwatch League Teams. 

### GET /players
Returns a Array of [Player Objects](objects/Player.md) representing players competitng in the current Overwatch League season.

### GET /players/:id
Returns a single Overwatch League Player when given the Player's ID.

### Player Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique integer identifier for an Overwatch League Player.  Example: <br><br><pre lang="json">"id": 3380</pre>|
|`availableLanguages`|Array of Strings Objects|An array of language abbreviations indicating the avaliable languas for player information. Example: <br><br><pre lang="json"> "availableLanguages": [ "en" ]</pre>|
|`handle`|String|The name of the Player's Battle.net account. Example: <br><br><pre lang="json">"handle": "taimou.6010"</pre>|
|`name`|String|The Player's Overwatch username. Example: <br><br><pre lang="json">"name": "Taimou"</pre>|
|`homeLocation`|String|The Player's hometown. Example: <br><br><pre lang="json">"homeLocation": "Juankoski"</pre>|
|`accounts`|Array of [Account](objects/Account.md) Objects|An array containing all of the Player's social media accounts.|
|`game`|String|The name of the game associated with the Player. Example: <br><br><pre lang="json">"game": "OVERWATCH"</pre>|
|`attributes`|Attribute Object|An Object containing information about a Player's most played heroes, player number, preferred slot, and role.|
|`attributesVersion`|String|A String representation of the attribute version.|
|`familyName`|String|The Player's last name. Example: <br><br><pre lang="json">"familyName": "Kettunen"</pre>|
|`givenName`|String|The Player's first name. Example: <br><br><pre lang="json">"givenName": "Timo"</pre>|
|`nationality`|String| A two letter abbrevition denoting the player's home country. Example: <br><br><pre lang="json">"nationality": "FI"</pre>|
|`headshot`|String|A String represenation of a Player's headshot URL. Example: <br><br><pre lang="json">"headshot": "https://bnetcmsus-a.akamaihd.net/cms/gallery/DFRBV085AX601550194285520.png"</pre>|
|`teams`|Array of [Competitor](objects/Competitor.md) Objects|An array of the Player's teams|
|`stats`|Object|An object consisting of the Players average stats per 10 minutes(i.e.  eliminations, deaths, hero damage, healing, final blows), total time played in the Overwatch League, and top heroes.|
|`statRank`|Object|An object consisting of the Players stat ranks. Ranked stats include stats per 10 minutes (i.e.  eliminations, deaths, hero damage, healing, final blows) and total time played in the Overwatch League.|
|`team`|Object|An object consisting of the Player's Team information.

## Match Endpoints
The following endpoints retrieve information for Overwatch League Matches. 

### GET /matches
Returns an array of Match objects. This denotes  all matches in the Overwatch League.

### GET /matches/:id
Returns information about a single Overwatch League Match given a Match ID.

### Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|The unique Integer identifier for a singel Overwatch League Match|
|`competitors`|Array of [Competitor](objects/Competitor.md) Objects|An Array containing the information of two competitng teams for an Overwatch League Match.|
|`scores`|Array of Int64|An array containing the currents scores for two Overwatch League Competitors respectively.|
|`conclusionValue`|Int64|The number of games for a single Overwatch League Match|
|`conclusionStrategy`|String|A string representation of an Overwatch League Match conclusion.|
|`winner`|[Competitor](objects/Competitor.md) Object|A Competitor object representing the winning team in an Overwatch League Match.|
|`home`|String|A string indicating the home location of a match.|
|`bracket`|Bracket Object|A Bracket Object which denotes the tournament infornation and stage information.|

### GET /live-match
Returns information regarding an ongoing live match.

### Live Match Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`liveMatch`|[Live Match](objects/LiveMatch.mb) Object| A Live Match object with information about the current match.|
|`nextMatch`|[Next Match](objects/NextMatch.mb) Object| A Next Match object with information about the next match.|

### GET /schedule
Returns the schedule for the current Overwatch League season.

### Schedule Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|String|A String identifier indicating the year of the current Overwatch League Season. Example:<br><br><pre lang="json">"id": "2019"</pre>|
|`startDate`|String|A String representing the start date of the current Overwatch League season. Example:<br><br><pre lang="json">"startDate": "02-14-2019"</pre>|
|`endDate`|String|A String representing the end date of the current Overwatch League season. Example:<br><br><pre lang="json">"endDate": "08-27-2019"</pre>|
|`endDateMS`|Int64|An Integer representing the end date of the current Overwatch League season. Example:<br><br><pre lang="json">"endDateMS": 1566975540000</pre>|
|`seriesId`|Int64|A unique integer identifier for the Overwatch League series. Example:<br><br><pre lang="json">"series": 181</pre>|
|`stages`|Array of Stage Objects|A list of all stages for the Overwatch League|


### GET /streams
Returns Overwatch League's stream information

### Streams Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique integer identifier for the Overwatch League's stream.|
|`name`|String|The stream title.|
|`slug`|String|The partt of a URL which identifies the Overwatch League stream on the stream's site.|
|`subtitle`|String|The sub text for the stream.|
|`description`|String|The current stream description.|
|`stream_name`|String|The name of the stream's host channel.|
|`is_hidden`|Boolean|Indicates if a stream information is hidden or not on the Overwatch League website.|
|`image_6_9_small`|String|A URL of the Overwatch League stream icon.|
|`tags`|Array of Strings|A list of tags for the Overwatch League streams.|
|`status`|Integer|Indicates whether or not the stream is visible and live|
|`channel_id`|Int64|A unique integer identifier for the Overwatch League's Twitch channel.|
|`cdn`|String|The name of the cache measurement mechanism for content delivery|

### GET /vods
Returns a list of videos on demand from https://overwatchleague.com

### VODs Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`status`|String|Indicates if the list of vods were retrieved or not.|
|`code`|Int64|Indicates if the list of vods were retrieved or not.|
|`data`|Array of [VOD](/objects/VOD.md) Objects|A List of available VODs on https://overwatchleague.com|

### GET /maps
Returns all of the available maps in Overwatch.

### Maps Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`guid`|Int128| A Globally Unique Identifier for an Overwatch Map.|
|`name`|Name object|An object with the name of a map in different languages.|
|`gameModes`|Array of Game Mode Objects|A list of available modes for a map. Each Game Mode has an `Id`, `Name`, and `Key`.|
|`id`|String|A string identifier of the map. This is typically the english name of the map.|
|`icon`|String|A URL of the map icon.|
|`thumbnail`|String|A URL of the map thumbnail.|
|`type`|String|The type of map. There are four types of maps used in the Overwatch League: Control, Hybrid, Assault, and Escort.|

### GET /news
Returns Overwatch League news nformation.

### News Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`totalBlogs`|Int64|An integer indicating the total number of blogs published on the Overwatch League website.|
|`pageSize`|Int64|The number of blog posts per page.|
|`page`|Int64|The current page of blogs as seen on https://overwatchleague.com|
|`totalPages`|Int64|The total number of blog post pages available on https://overwatchleague.com|
|`blogs`|Array of [Blog](objects/Blog.md) Objects|A lists of blog posts on a specified page.|

<hr>
Thank you for reading! If you have anymore questions or want to share your work, <a href="https://discord.gg/PBwan6u">click here</a> to join the server if you haven't already!
