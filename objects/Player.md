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
