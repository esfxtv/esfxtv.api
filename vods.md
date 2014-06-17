# Vods

***

Vod - Video on Demand. Vod relates to [stream][streams].

| Endpoint | Description |
| ---- | --------------- |
| [GET /vod/list](/vods.md#get-vodlist) | Get list of vods |
| [GET /vod/info/:vod](/vods.md#get-vodinfovod) | Get vod details info |
| [GET /channel/:channel/vods](/vods.md#get-channelchannelvods) | Get list of vods for channel |

[streams]: /streams.md

## `GET /vod/list`

Returns list of vods.

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
http://api.esfxtv.com/vod/list
http://api.esfxtv.com/vod/list?pagenumber=1&pagesize=2
```

### Example Response

```json
[

    {
        "Name": "moon",
        "Description": "",
        "Code": "LnzOdAcmvkiYIfoClrzYzg",
        "Start": "2014-06-04T10:36:52",
        "End": "2014-06-04T10:53:27",
        "Duration": 995,
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/oDtjLZIW.jpg",
        "Rating": {
            "Like": 0,
            "View": 0
        },
        "Stream": {
            "Name": "moon",
            "TypeName": "EsfxTv"
        },
        "ItemsCount": 1
    },
    {
        "Name": "dota_vitya",
        "Description": "",
        "Code": "Ene0VScoWEGX2vDxQ8bNUw",
        "Start": "2014-06-04T09:48:52",
        "End": "2014-06-04T10:30:53",
        "Duration": 2521,
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/LTyv0pZL.jpg",
        "Rating": {
            "Like": 0,
            "View": 0
        },
        "Stream": {
            "Name": "dota_vitya",
            "TypeName": "EsfxTv"
        },
        "ItemsCount": 3
    }

]
```

## `GET /vod/info/:vod`

Returns information about vod.

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
            <td><code>:vod</code></td>
            <td>required</td>
            <td>string</td>
            <td>Vod unique code</td>
        </tr>
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/vod/info/Ene0VScoWEGX2vDxQ8bNUw
```

### Example Response

```json
{

    "Name": "dota_vitya",
    "Description": "",
    "Code": "Ene0VScoWEGX2vDxQ8bNUw",
    "Start": "2014-06-04T09:48:52",
    "End": "2014-06-04T10:30:53",
    "Duration": 2521,
    "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/LTyv0pZL.jpg",
    "Rating": {
        "Like": 0,
        "View": 0
    },
    "Stream": {
        "Name": "dota_vitya",
        "TypeName": "EsfxTv"
    },
    "Items": [
        {
            "ViewUrl": "http://str001.cdn.esfx.tv/esfxtv.com/dota_vitya/2014-06-04_09-48_1.mp4",
            "PartNumber": 1,
            "Code": 635374721320000000,
            "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/LTyv0pZL.jpg",
            "Start": "2014-06-04T09:48:52",
            "End": "2014-06-04T10:18:52",
            "Duration": 1800
        },
        {
            "ViewUrl": "http://str001.cdn.esfx.tv/esfxtv.com/dota_vitya/2014-06-04_10-18_2.mp4",
            "PartNumber": 2,
            "Code": 635374739320000000,
            "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/R3GWDa7q.jpg",
            "Start": "2014-06-04T10:18:52",
            "End": "2014-06-04T10:28:18",
            "Duration": 566
        },
        {
            "ViewUrl": "http://str001.cdn.esfx.tv/esfxtv.com/dota_vitya/2014-06-04_09-45_3.mp4",
            "PartNumber": 3,
            "Code": 635374719300000000,
            "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/cgzHD_Ud.jpg",
            "Start": "2014-06-04T09:45:30",
            "End": "2014-06-04T09:48:05",
            "Duration": 155
        }
    ]

}
```

## `GET /channel/:channel/vods`

Returns list of vods for channel.

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
            <td><code>:channel</code></td>
            <td>required</td>
            <td>string</td>
            <td>Channel friendly name</td>
        </tr>
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
http://api.esfxtv.com/channel/prdota2/vods
http://api.esfxtv.com/channel/prdota2/vods?pagenumber=1&pageSize=2
```

### Example Response

```json
[

    {
        "Name": "moon",
        "Description": "",
        "Code": "4yFGUTNNPUGVqsuxrIx1NA",
        "Start": "2014-06-16T07:44:52",
        "End": "2014-06-16T08:54:18",
        "Duration": 4166,
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/VAXZHhUo.jpg",
        "Rating": {
            "Like": 0,
            "View": 0
        },
        "Stream": {
            "Name": "moon",
            "TypeName": "EsfxTv"
        },
        "ItemsCount": 3
    },
    {
        "Name": "alexei_lipai",
        "Description": "",
        "Code": "3m6Uti5RKUedIBCrg8fmdw",
        "Start": "2014-06-13T15:43:18",
        "End": "2014-06-13T18:48:49",
        "Duration": 11131,
        "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/LyHt1ECu.jpg",
        "Rating": {
            "Like": 0,
            "View": 0
        },
        "Stream": {
            "Name": "alexei_lipai",
            "TypeName": "EsfxTv"
        },
        "ItemsCount": 7
    }

]
```
