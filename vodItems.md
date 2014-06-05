# Vod Items

***

Vod Item it's part of [vod][vods].

| Endpoint | Description |
| ---- | --------------- |
| [GET /voditem/info/:voditem](/voditems.md#get-voditeminfovoditem) | Get vod item details info |

[vods]: /vods.md

## `GET /voditem/info/:voditem`

Returns information about voditem.

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
            <td><code>:voditem</code></td>
            <td>required</td>
            <td>string</td>
            <td>Vod item unique code</td>
        </tr>
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/voditem/info/635374739320000000
```

### Example Response

```json
{

    "ViewUrl": "http://str001.cdn.esfx.tv/esfxtv.com/dota_vitya/2014-06-04_10-18_2.mp4",
    "PartNumber": 2,
    "Code": 635374739320000000,
    "PreviewImageUrl": "http://img.cdn.esfxtv.com/Vod/R3GWDa7q.jpg",
    "Start": "2014-06-04T10:18:52",
    "End": "2014-06-04T10:28:18",
    "Duration": 566

}
```
