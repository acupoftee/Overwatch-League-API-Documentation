# Competitors
A Competitor is an Overwatch League team competiting in the current season. 

## Competitor Data Dictionary
See [Team Data Dictionary](#team-data-dictionary)
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`                   | Int64 | The unique integer identifier for the Overwatch League Team. Example: <br><br><pre lang="json">"id": 4523</pre>
|`divisionId` | Int64 | The unique integer identifier for the Team's Overwatch League [Division](objects/Division.md). Example:<br><br><pre lang="json">"divisionId": 80</pre>
|`handle` | String | A String representation of an Overwatch League team's handle. Example: <br><br><pre lang="json">"handle": "fuel.6990"</pre>
|`name` | String | A String representation of an Overwatch League team's name. Example: <br><br><pre lang="json">"name": "Boston Uprising"</pre>
|`abbreviatedName` | String | A String representation of an Overwatch League team's 3 letter abbreviated name. Example: <br><br><pre lang="json">"abbreviatedName": "ATL"</pre>
| `logo` | [Logo](objects/Logo.md) Object | A Logo object containing an Overwatch League team's logo in SVG and PNG formats.|
|`hasFallback` | Boolean | Indicates whether or not a team has media queries which specific browsers cannot handle, such as logo files and headshot files. Example: <br><br><pre lang="json">"hasFallback": false</pre>
|`location` | String | A String representation of an Overwatch League team's base location. Example: <br><br><pre lang="json">"location": "Boston, MA"</pre>
| `players` | Array of [Player](objects/Player.md) Object |A Player roster for a competing Overwatch League Team. Additionally, see Player object for more info. |
|`website` | String | A String representation of an Overwatch League team's website url. Example: <br><br><pre lang="json">"website": "https://fuel.overwatchleague.com"</pre>
|`placement` | Int64 | The current standing of an Overwatch League Team. Example: <br><br><pre lang="json">"placement": 1</pre>
|`advantage` | Int64 | An integer indicating the advantage an Overwatch League Team has over its competitors. Example: <br><br><pre lang="json">"advantage": 0</pre>
| `records` | [Records](objects/Records.md) Object | A Records object containing an Overwatch League team's league records. See Records object for more info.|
