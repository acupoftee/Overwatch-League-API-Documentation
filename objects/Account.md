<img src="https://bnetcmsus-a.akamaihd.net/cms/content_entry_media/xr/XRDRIVHBBVI51538517475154.jpg"> 

# Account
Overwatch League teams and players each have their social media accounts for interacting with fans. Each Account object has an account ID, an account type, and an account URL.

## Account Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`id`|Int64|A unique integer identifier for an Account.|
|`type`|String|The type of social media account. The following account types are: `TWITTER`, `TWITCH`, `FACEBOOK`, `INSTAGRAM`, `DISCORD`, `YOUTUBE_CHANNEL`, `YOUTUBE_USER`, `WEIBO`, `REDDIT_SUB`, and `OTHER` |
|`url`|String|A URL for an Account.|
