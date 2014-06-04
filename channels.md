# Channels

***

Channels allow to group streams.

| Endpoint | Description |
| ---- | --------------- |
| [GET /channel/list](/WebApiInterface.md#get-channellist) | Get list of channels |
| [GET /channel/live](/WebApiInterface.md#get-channellive) | Get list of live channels |



## `GET /channel/list`

Returns list of channels.

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th width="50">Type</th>
            <th width=100%>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>pagenumber</code></td>
            <td>optional</td>
            <td>int</td>
            <td>Page number (1 or more).</td>
        </tr>
        <tr>
            <td><code>pagesize</code></td>
            <td>optional</td>
            <td>int</td>
            <td>Page size (1 or more).</td>
        </tr>
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/channel/list
http://api.esfxtv.com/channel/list?pagenumber=1&pagesize=2
```

### Example Response

```json
[
    {
        "Name": "PLOMBEER",
        "Description": "SWAG VS HF",
        "Created": "2014-02-09T15:44:51.77",
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/kiJIfGxX.cropped.png",
        "FriendlyName": "plombeer",
        "HasAnyStreamInLive": false,
        "Rating": {
            "Like": 1846,
            "View": 529
        },
        "Creator": {
            "Nickname": "PLOMBEER",
            "AvatarUrl": ""
        }
    },
    {
        "Name": "Sweaty Cup 2",
        "Description": "Relax, Power Rangers, Dream Team(The Retry),Team DOG, \"Duza Gaming, Oslic Gaming, zeRAGE и т.д.",
        "Created": "2014-04-16T14:04:10.47",
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/-tpWL2G4.cropped.jpg",
        "FriendlyName": "potcup",
        "HasAnyStreamInLive": false,
        "Rating": {
            "Like": 1293,
            "View": 56415
        },
        "Creator": {
            "Nickname": "Sweaty_cup",
            "AvatarUrl": "http://img.cdn.esfxtv.com/UserProfile/UserPreview/-_lJiYUR.cropped.png"
        }
    }
]
```


## `GET /channel/live`

Returns list of live channels.

### Parameters

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Required?</th>
            <th width="50">Type</th>
            <th width=100%>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>pagenumber</code></td>
            <td>optional</td>
            <td>int</td>
            <td>Page number (1 or more).</td>
        </tr>
        <tr>
            <td><code>pagesize</code></td>
            <td>optional</td>
            <td>int</td>
            <td>Page size (1 or more).</td>
        </tr>
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/channel/live
http://api.esfxtv.com/channel/live?pagenumber=1&pagesize=2
```

### Example Response

```json
[

    {
        "Name": "E.S.F.X. Online",
        "Description": "Здесь мы стримим всякие прикольные моменты из жизни проекта.\r\nхе хе хе",
        "Created": "2013-07-10T06:41:21.19",
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/BoFm7ogs.cropped.png",
        "FriendlyName": "e-s-f-x-online",
        "Rating": {
            "Like": 15,
            "View": 228
        },
        "Creator": {
            "Nickname": "Stucer",
            "AvatarUrl": "http://img.cdn.esfxtv.com/UserProfile/Cropped_hTF6l6fZ.jpg"
        }
    }
]
```
