# Streams

***

Streams are video broadcasts. 

| Endpoint | Description |
| ---- | --------------- |
| [GET /stream/getqualities](/streams.md#get-streamgetqualities) | Get list of qualities in system |
| [GET /stream/getqualities/:stream](/streams.md#get-streamgetqualitiesstream) | Get list of available available for stream |
| [GET /stream/geturl/:stream/:quality](/streams.md#get-streamgeturlstreamquality) | Get broadcast url for stream  |

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


## `GET /stream/getqualities/:stream/:quality`

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

