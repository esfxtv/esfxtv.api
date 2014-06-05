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
http://api.esfxtv.com/voditem/info/prdota2
```

### Example Response

```json

```
