# Game Mode

## Game Mode Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`Id`|String|A unique string representation of the Map GUID.|
|`Name`|String|The name of the game mode.|
|`Key`|Object|An object containing an API key for the game's data. Each Key has a `href` property with a URL to the data.|

```json
{
    "Id": "0x0230000000000014",
    "Name": "Assault",
    "Key": {
        "href": "http://us.game-data-api.blizzard:8080/api/data/overwatch/gamemodes/0x0230000000000014?auth=UYu3k4vrTKIjtIZZ69RNSYVgtvlpVIrt&namespace=1_32_1_0_54356l"
    }
}
```