# Streams

***

Streams are video broadcasts. 

| Endpoint | Description |
| ---- | --------------- |
| [GET /stream/getqualities](/streams.md#get-streamgetqualities) | Get list of qualities in system |
| [GET /stream/getqualities/:stream](/streams.md#get-streamgetqualitiesstream) | Get list of available available for stream |
| [GET /stream/geturl/:stream/:quality](/streams.md#get-streamgeturlstreamquality) | Get broadcast url for stream  |
| [GET /stream/getinfo/:stream/:channel](/streams.md#get-streamgetinfostreamchannel | Get info about stream to embed video on page |

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
            <td>Stream Friendly Name</td>
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
            <td>Stream Friendly Name</td>
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
            <td>Stream Friendly Name</td>
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
http://api.esfxtv.com/stream/getinfo/stucer
http://api.esfxtv.com/stream/getinfo/stucer/e-s-f-x-online
```

### Example Response

```json
{

    "StreamName": "Stucer",
    "OnlineView": 0,
    "Rating": {
        "Like": 32,
        "View": 432
    },
    "ChannelName": "E.S.F.X. Online",
    "ChannelPreviewUrl": "http://img.cdn.esfxtv.com/Channel/ChannelPreview/BoFm7ogs.cropped.png",
    "Description": "Здесь мы стримим всякие прикольные моменты из жизни проекта.\r\nхе хе хе",
    "IsOnline": false,
    "StreamHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/stream/share/stucer/esfxtv/e-s-f-x-online'></iframe>",
    "ChatHtmlValue": "<iframe height='100%' width='100%' src='http://esfxtv.com/ru/Chat/Popup/e-s-f-x-online'></iframe>"

}
```



