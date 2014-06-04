# Web Api 

***

Web Api interface api.esfxtv.com

# Channels

***

Channels allow to group streams.

| Endpoint | Description |
| ---- | --------------- |
| [GET /channel/list](/WebApiInterface.md#get-channellist) | Get list of channels |



| Endpoint | Description |
| ---- | --------------- |
| [GET /channels/:channel](/v2_resources/channels.md#get-channelschannel) | Get channel object|
| [GET /channel](/v2_resources/channels.md#get-channel) | Get channel object |
| [GET /channels/:channel/editors](/v2_resources/channels.md#get-channelschanneleditors) | Get channel's list of editors |
| [PUT /channels/:channel](/v2_resources/channels.md#put-channelschannel) | Update channel object |
| [GET /channels/:channel/videos](/v2_resources/channels.md#get-channelschannelvideos) | Get channel's list of videos |
| [GET /channels/:channel/follows](/v2_resources/channels.md#get-channelschannelfollows) | Get channel's list of following users |
| [DELETE /channels/:channel/stream_key](/v2_resources/channels.md#delete-channelschannelstream_key) | Reset channel's stream key |
| [POST /channels/:channel/commercial](/v2_resources/channels.md#post-channelschannelcommercial) | Start a commercial on channel |

[users]: /v2_resources/users.md
[streams]: /v2_resources/streams.md
[videos]: /v2_resources/videos.md

## `GET /channel/list`

Returns a channel object.

### Example Request

```bash
curl -H 'Accept: application/vnd.twitchtv.v2+json' \
-X GET https://api.twitch.tv/kraken/channels/test_user1
```

### Example Response

```json
{
  "name": "test_user1",
  "game": "World of Warcraft: Cataclysm",
  "created_at": "2011-02-24T01:38:43Z",
  "title": "test_user1",
  "updated_at": "2012-06-18T05:22:53Z",
  "banner": "http://static-cdn.jtvnw.net/jtv_user_pictures/test_user1-channel_header_image-7d10ec1bfbef2988-640x125.png",
  "video_banner": "http://static-cdn.jtvnw.net/jtv_user_pictures/test_user1-channel_offline_image-bdcb1260130fa0cb.png",
  "background": "http://static-cdn.jtvnw.net/jtv_user_pictures/test_user1-channel_background_image-eebc4eabf0686bb9.png",
  "_links": {
    "self": "https://api.twitch.tv/kraken/channels/test_user1",
    "chat": "https://api.twitch.tv/kraken/chat/test_user1",
    "videos": "https://api.twitch.tv/kraken/channels/test_user1/videos",
    "commercial": "https://api.twitch.tv/kraken/channels/test_user1/commercial",
    "follows":"https://api.twitch.tv/kraken/channels/test_user1/follows",
    "stream_key":"https://api.twitch.tv/kraken/channels/test_user1/stream_key",
    "features":"https://api.twitch.tv/kraken/channels/test_user1/features",
    "subscriptions":"https://api.twitch.tv/kraken/channels/test_user1/subscriptions",
    "editors":"https://api.twitch.tv/kraken/channels/test_user1/editors"
  },
  "logo": "http://static-cdn.jtvnw.net/jtv_user_pictures/test_user1-profile_image-7243b004a2ec3720-300x300.png",
  "_id": 20694610,
  "mature": true,
  "url": "http://www.twitch.tv/test_user1",
  "display_name": "test_user1"
}
```
