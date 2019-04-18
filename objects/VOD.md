# VOD
A VOD is an acronym short for Video On Demand. These are post recorded matches that can be found on Overwatch League's website.

## VOD Data Dictionary
| Attribute           | Type  | Description |
|:--------------------|:------|:------------|
|`unique_id`|String|The unique String identifier for a  VOD.|
|`user_id`|Int64|An Integer identifier for a user interacting with a VOD.|
|`organization_id`|String|A unique String identifier for the VOD organizers.|
|`video_type`|String|The type of video listed on overwatchleague.com.|
|`title`|String|The title of a VOD.|
|`description`|String|The current description of a VOD. The language of a description changes depending on the locale.|
|`length`|Int64|The Integer representing the length of a VOD.|
|`status`|String|The status of a VOD upload. A status can be either "compelte" or "processing."|
|`available`|Int64|The number of VODs available with the same content.|
|`thumbnail`|String|A URL for the VOD thumbnail.|


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