# Blog 

## Blog Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`blodId`|Int64|The unique Integer identifier for a Blog.|
|`created`|Int64|An Integer representing the date and time a Blog was created.|
|`updated`|Int64|An Integer representing the date and time a Blog was updated.|
|`publish`|Int64|An Integer representing the date and time a Blog was published.|
|`title`|String|The current title of a Blog.|
|`author`|String|The author of a Blog.|
|`locale`|String|The current locale of a Blog. The locale will change depending on the language you choose to view the main website.|
|`keywords`|Array of Strings|A list of keywords for a Blog.|
|`summary`|String|The current title of a Blog. The language of a summary changes depending on the locale.|
|`commentKey`|String|A key denoting the primary language for a Blog's comments.|
|`status`|String|The live status of a Blog.|
|`thumbnail`|Object|An object denoting the properties of a Blog's thumbnail.|
|`defaultCommunity`|String|The default target community for a specific Blog.|
|`defaultUrl`|String|The default URL for a Blog.|
|`commentsEnabled`|Boolean|Indicates whether or not comments are enabled for a Blog.|
|`pollAttached`|Boolean|Indicates whether or not polls are enabled for a Blog.|
|`communityBlogs`|Array of Objects|Indicates whether or not comments are enabled for a Blog.|



## Sample Blog JSON
```json
{
            "blogId": 22886963,
            "created": 1548955301880,
            "updated": 1550509208217,
            "publish": 1550505600000,
            "title": "What’s New with Overwatch Contenders in 2019",
            "author": "Blizzard Entertainment",
            "locale": "en_US",
            "keywords": [
                "news"
            ],
            "summary": "Here’s how we’re making the Path to Pro even more thrilling and high-profile. ",
            "commentKey": "us.en_us.blog.22886963",
            "status": "live",
            "thumbnail": {
                "mediaId": 22884297,
                "url": "//bnetcmsus-a.akamaihd.net/cms/blog_thumbnail/jb/JB0GKPW2D1BP1548895641792.jpg",
                "mimeType": "image/jpeg",
                "type": "fullsize",
                "size": 100876,
                "width": 640,
                "height": 360,
                "originalFileName": "OW_Contenders_Blog_Thumbnail-2019WhatsNew.jpg",
                "mediaType": 1
            },
            "defaultCommunity": "owc",
            "defaultUrl": "https://overwatchcontenders.com/en-us/news/22886963",
            "commentsEnabled": true,
            "pollAttached": false,
            "communityBlogs": [
                {
                    "communityId": 70,
                    "sticky": false,
                    "defaulted": false
                },
                {
                    "communityId": 76,
                    "sticky": true,
                    "defaulted": true
                }
            ],
            "localizationPublish": 1550505600000,
            "siteCategory": "COMMUNITY",
            "draft": false,
            "showPtr": false,
            "featuredMap": false,
            "showRating": false,
            "spotlight": false,
            "customPublish": false,
            "tags": [
                "owl-newspage-featured",
                "ow_p2p",
                "esports"
            ],
            "stickyForThisLocale": false,
            "embed": "https://overwatchleague.com/en-us/news/22886963"
        }
```