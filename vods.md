# Vods

***

Vod - Video on Demand. Vod relates to [stream][streams].

| Endpoint | Description |
| ---- | --------------- |
| [GET /vod/list](/vods.md#get-vodlist) | Get list of vods |
| [GET /vod/info/:vod](/vods.md#get-vodinfovod) | Get vod details info |

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
http://api.esfxtv.com/vod/info/prdota2
```

### Example Response

```json

```
