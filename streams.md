# Streams

***

Streams are video broadcasts. 

| Endpoint | Description |
| ---- | --------------- |
| [GET /stream/getqualities](/streams.md#get-streamgetqualities) | Get list of qualities in system |
| [GET /stream/getqualities/:stream](/streams.md#get-getqualitiesstream) | Get list of available available for stream |
| [GET /stream/geturl/:stream/:quality](/streams.md#get-geturlstreamquality) | Get broadcast url for stream  |

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

