# Streams

***

Streams are video broadcasts. 

| Endpoint | Description |
| ---- | --------------- |
| [GET /stream/getqualities](/streams.md#get-streamgetqualities) | Get list of qualities in system |
| [GET /stream/getqualities/:stream](/streams.md#get-streamgetqualitiesstream) | Get list of available available for stream |
| [GET /stream/geturl/:stream/:quality](/streams.md#get-streamgeturlstreamquality) | Get broadcast url for stream  |
| [GET /stream/getinfo/:stream/:channel](/streams.md#get-streamgetinfostreamchannel) | Get info about stream to embed video on page |
| [GET /stream/embedinfo/:stream/:channel](/streams.md#get-streamembedinfostreamchannel) | Get info about stream (without link to channel) to embed video on page |

## `GET /stream/getqualities`

Returns list of available qualities.

### Example Request

```bash
http://api.esfxtv.com/stream/getqualities
```

### Example Response

```json
[

    {
        "Name": "480p",
        "Width": 640,
        "Height": 480,
        "OrderNumber": 1
    },
    {
        "Name": "Source",
        "Width": 1920,
        "Height": 1080,
        "OrderNumber": 3
    }

]
```

## `GET /stream/getqualities/:stream`

Returns list of available qualities for stream.

### Request Parameters

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
            <td><code>:stream</code></td>
            <td>required</td>
            <td>string</td>
            <td>Stream Name</td>
        </tr>
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/stream/getqualities/stucer
```

### Example Response

```json
[

    {
        "Name": "480p",
        "Width": 640,
        "Height": 480,
        "OrderNumber": 1
    },
    {
        "Name": "Source",
        "Width": 1920,
        "Height": 1080,
        "OrderNumber": 3
    }

]
```


## `GET /stream/geturl/:stream/:quality`

Returns broadcast url for stream.

### Request Parameters

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
            <td><code>:stream</code></td>
            <td>required</td>
            <td>string</td>
            <td>Stream Name</td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <td><code>:quality</code></td>
            <td>required</td>
            <td>string</td>
            <td>Quality Name</td>
        </tr>
    </tbody>    
</table>

### Example Request

```bash
http://api.esfxtv.com/stream/geturl/stucer/480p
```

### Example Response

```json
"rtmp://str001.cdn.esfx.tv/liveedge/stucer.480p"
```

## `GET /stream/getinfo/:stream/:channel`

Returns information to embed video on page. Request must contains :channel to get information about chat and link stream to channel. Parameter :channel required to save full statistic information about views and likes on external sites.

### Request Parameters

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
            <td><code>:stream</code></td>
            <td>required</td>
            <td>string</td>
            <td>Stream Name</td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <td><code>:channel</code></td>
            <td>recomended</td>
            <td>string</td>
            <td>Channel Friendly Name</td>
        </tr>
    </tbody>    
</table>

### Example Request

```bash
http://api.esfxtv.com/stream/getinfo/moon
http://api.esfxtv.com/stream/getinfo/moon/prdota2
```

### Example Response

```json
{

    "StreamName": "moon",
    "OnlineView": 0,
    "Rating": {
        "Like": 72,
        "View": 5110
    },
    "ChannelName": "PowerRangersDota2",
    "ChannelPreviewUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/_JPiVumS.cropped.png",
    "Description": "This is official stream's channel of PowerRangers Dota 2 team. Here you can find all streams of our players and our games.",
    "IsOnline": false,
    "StreamHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/stream/share/moon/esfxtv/prdota2'></iframe>",
    "ChatHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/ru/Chat/Popup/prdota2'></iframe>"

}
```

## `GET /stream/embedinfo/:stream/:channel`

Returns information to embed video and on page. Can be used without link stream to channel

### Request Parameters

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
            <td><code>:stream</code></td>
            <td>required</td>
            <td>string</td>
            <td>Stream Name</td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <td><code>:channel</code></td>
            <td>recomended</td>
            <td>string</td>
            <td>Channel Friendly Name</td>
        </tr>
    </tbody>    
</table>

### Example Request

```bash
http://api.esfxtv.com/stream/embedinfo/moon
http://api.esfxtv.com/stream/embedinfo/moon/prdota2
```

### Example Response

```json

{

    "StreamName": "moon",
    "OnlineView": 0,
    "Rating": {
        "Like": 89,
        "View": 6318
    },
    "ChannelName": "",
    "ChannelPreviewUrl": "",
    "Description": "",
    "IsOnline": false,
    "StreamHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/stream/share/moon/esfxtv'></iframe>",
    "ChatHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/ru/Chat/Popup/moon'></iframe>"

}

{

    "StreamName": "moon",
    "OnlineView": 0,
    "Rating": {
        "Like": 89,
        "View": 6318
    },
    "ChannelName": "PowerRangersDota2",
    "ChannelPreviewUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/_JPiVumS.cropped.png",
    "Description": "This is official stream's channel of PowerRangers Dota 2 team. Here you can find all streams of our players and our games.",
    "IsOnline": false,
    "StreamHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/stream/share/moon/esfxtv/prdota2'></iframe>",
    "ChatHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/ru/Chat/Popup/prdota2'></iframe>"

}
```

