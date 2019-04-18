# VOD
A VOD is an acronym short for Video On Demand. These are post recorded matches that can be found on Overwatch League's website.

## VOD Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`unique_id`|String|The unique String identifier for a  VOD.|
|`user_id`|Int64|An Integer identifier for a user interacting with a VOD.|
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
|`localizationPublish`|Int64|An Integer representing the date and time a localized Blog was published.|
|`siteCategory`|String|The section of the Overwatch League website containing the Blog post.|

## Sample VOD JSON
```json
 {
            "unique_id": "GrJcuGLXCAc",
            "parent_unique_id": null,
            "user_id": 53,
            "organization_id": "9632a417-8a39-43bb-9d71-5892cdfc4c81",
            "video_type": "VOD",
            "video_sub_type": null,
            "title": "Game 1 PAR @ VAN | Stage 1 Week 4",
            "description": "08-MAR-2019 | Stage 1 Week 4 Day 2",
            "length": null,
            "privacy": null,
            "status": "processing",
            "available": 1,
            "user_content": 0,
            "thumbnail": "https://s3.amazonaws.com/mlg-profile-production/forge/784248eb-eebe-4e02-8174-1896e089265b-1280x720?v=1552098683",
            "video_thumbnail_id": 49592,
            "location": null,
            "eve_slug": null,
            "stream_name": null,
            "channel_slug": null,
            "channel_id": null,
            "views": null,
            "likes": null,
            "dislikes": null,
            "favorites": null,
            "publish_type": "auto",
            "stats_at": null,
            "recorded_at": "2019-03-09T02:00:03.000Z",
            "broadcasted_at": null,
            "available_at": "2019-03-09T02:30:00.000Z",
            "starts_at": null,
            "created_at": "2019-03-09T02:00:03.000Z",
            "updated_at": "2019-03-09T02:32:09.000Z",
            "share_url": "https://video.majorleaguegaming.com/GrJcuGLXCAc",
            "thumbnails": [
                {
                    "id": 49591,
                    "video_id": 9882,
                    "source_thumbnail_id": null,
                    "thumbnail_type": "auto",
                    "thumbnail_url": "https://d3m037qqkidp3x.cloudfront.net/ISP/m/2RJqwy/media.jpg",
                    "size": "original",
                    "width": null,
                    "height": null,
                    "time_at": null,
                    "created_at": "2019-03-09T02:00:03.000Z",
                    "updated_at": "2019-03-09T02:00:03.000Z"
                },
            ],
            "video_assets": [
                {
                    "id": 18212,
                    "unique_id": "uMYzFV5xrByq",
                    "video_id": 9882,
                    "source": "akamai",
                    "source_id": "61ceae21-ffe0-4fbe-a2d5-471700e37b94",
                    "source_url": null,
                    "source_host": null,
                    "source_path": null,
                    "source_data": "GrJcuGLXCAc-en-US.mp4",
                    "format": "hls",
                    "asset_type": "ORIGINAL",
                    "status": "processing",
                    "available": null,
                    "created_at": "2019-03-09T02:00:03.000Z",
                    "updated_at": "2019-03-09T02:32:23.000Z"
                }
            ],
            "tags": [
                {
                    "id": 1684,
                    "tag_type_id": 19,
                    "tag_type": "blizzard",
                    "tag_value": "esports-player-3987",
                    "created_at": "2019-03-09T02:32:00.000Z"
                },
            ],
            "embed": "https://player2.majorleaguegaming.com/api/v2/player/embed/vod/owl-web?vid=GrJcuGLXCAc&lang=undefined"
        }
```