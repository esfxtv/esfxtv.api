# Chat

***

Chat is where users can interact with each other while watching a [stream][streams] on [channel][channels].

[streams]: /streams.md
[channels]: /channels.md

| Endpoint | Description |
| ---- | --------------- |
| [GET /chat/info/:channel](/chat.md#get-chatinfochannel) | Get links object to other chat endpoints |
| [GET /chat/getinfo/:channel](/chat.md#get-chatgetinfochannel) | OBSOLETE! Will be removed. Use /chat/info. Get links object to other chat endpoints |

## `GET /chat/info/:channel`

Get links object to other chat endpoints.

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
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/chat/info/e-s-f-x-online
```

### Example Response

```json
"<iframe height='100%' width='100%' src='http://esfxtv.com/ru/chat/popup/e-s-f-x-online'></iframe>"
```

## `GET /chat/getinfo/:channel`

Get links object to other chat endpoints.

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
    </tbody>
</table>

### Example Request

```bash
http://api.esfxtv.com/chat/info/e-s-f-x-online
```

### Example Response

```json
"<iframe height='100%' width='100%' src='http://esfxtv.com/ru/chat/popup/e-s-f-x-online'></iframe>"
```


