# News

***

| Endpoint | Description |
| ---- | --------------- |
| [GET /news/list](/news.md#get-newslist) | Get list of news |

## `GET /news/list`

Returns list of news.

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
http://api.esfxtv.com/news/list
http://api.esfxtv.com/news/list?pagenumber=1&pagesize=2
```

### Example Response

```json
[

    {
        "Name": "Team Empire отказываются от участия в DreamLeague",
        "Description": "<p>Было сделано официальное заявление<span lang=\"EN-US\"> Александром\n<strong>\"StrangeR\"</strong> Соломоновым:</span>\n\n</p>\n\n<p><em>\"К сожалению, в команде возникли противоречия, которые очень\nсложно разрешить в один день, и, скорее всего, будут замены. На данный момент у\nнас нет уверенности в положительном результате на Дримлиге и нет полного\nсостава, с которым мы могли бы туда поехать. </em><br><em>\nВзять иностранных стендинов и просто отыграть турнир - это не то, чего мы хотели,\nособенно учитывая то, что турнир будет длиться от 7 до 14 дней. Мы сразу же\nпоставили в известность администрацию турнира, чтобы у них ещё была возможность\nнайти замену. </em><br><em>\nСейчас наша основная задача урегулировать проблемы в составе и готовиться к следующим\nтурнирам. Подробная информация о случившихся событиях и решении менеджмента\nбудет анонсирована в ближайшие дни\"</em></p>\n\n<p>Бывший игрок <span lang=\"EN-US\"><strong>VP</strong></span><strong>.</strong><span lang=\"EN-US\"><strong>Polar</strong></span>, Роман <strong>\"</strong><span lang=\"EN-US\"><strong>Scandal</strong></span><strong>\"</strong> Садотенков, в\nпоследние дни фигурировал в качестве замены на место капитана, Романа <strong>\"</strong><span lang=\"EN-US\"><strong>Resolut</strong></span><strong>1</strong><span lang=\"EN-US\"><strong>on</strong></span><strong>\"</strong> Фоминка, который, по слухам,\nдолжен уйти из команды. <br></p>\n\n<p>Официальных комментариев от администрации <span lang=\"EN-US\"><strong>DreamLeague</strong></span> пока не было, как и объявления команды, которая займет освободившееся место. Хотя, вероятнее всего, это будет <span lang=\"EN-US\"><strong>Virtus.Pro</strong></span>.</p>\n\n<p>#Dota2, #TeamEmpire, #DreamLeague<br></p>",
        "ShortDescription": "Team Empire не будут принимать участие в DreamLeague Season 2 из-за разногласий внутри команды. Похоже, у команды просто нет подходящего состава для путешествия в Швецию. Подробнее читайте в новости.",
        "UrlFriendlyName": "team-empire-otkazyvayutsya-ot-uchastiya-v-dreamleague",
        "PreviewImageUrl": "http://i.imgur.com/MwZGIth.jpg",
        "DetailsLink": "/ru/news/team-empire-otkazyvayutsya-ot-uchastiya-v-dreamleague",
        "CreatorNickname": null,
        "Created": "2014-11-11T06:31:03.587",
        "Published": "2014-11-11T06:31:03",
        "Tags": [ ],
        "LatestUserNews": [ ],
        "User": {
            "Nickname": "WalterBlake",
            "AvatarUrl": "http://img.cdn.esfxtv.com/UserProfile/UserPreview/eGeXsQ4X.cropped.jpg",
            "UserInfoLink": "/ru/user/walterblake"
        },
        "View": 11
    },
    {
        "Name": "Alliance отказывается от участия в турнирах для переформирования команды",
        "Description": "\n \n\n<p><span lang=\"EN-US\"><strong>Akke</strong></span><span lang=\"EN-US\"> </span>публично заявил, что <span lang=\"EN-US\"><strong>Alliance</strong></span> откажутся от участия в «некоторых турнирах», для «перестройки»\nсвоего состава. В последнее время команду преследуют неудачи. <span lang=\"EN-US\"><strong>Chessie</strong></span> выбыл из строя на <span lang=\"EN-US\"><strong>WCA</strong></span><span lang=\"EN-US\"></span>,\nотборочные в <span lang=\"EN-US\"><strong>DreamLeague</strong></span>\nпровалились, да и вообще, их результаты по всем фронтам оставляют желать\nлучшего. </p>\n\n<p>Недавний проигрыш против <span lang=\"DE\"><strong>Team</strong></span><span lang=\"DE\"> </span><span lang=\"DE\"><strong>Tinker</strong></span> на <strong>D2L</strong>, уже далеко не первый в серии неудач, скорее\nвсего, стал последней каплей и причиной такого решения. В данный момент\nкоманда участвует только в <span lang=\"EN-US\"><strong>D</strong></span><strong>2</strong><span lang=\"EN-US\"><strong>L</strong></span> и <span lang=\"EN-US\"><strong>DotaCinema</strong></span><strong>'</strong><span lang=\"EN-US\"><strong>s</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>Captain</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>Draft</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>Season</strong></span><strong>2</strong>. Этим все и должно\nограничиться, пока не произойдут изменения в её составе.</p>\n\n<p><span lang=\"EN-US\"><strong>Alliance</strong></span>\nвсе чаще вынуждены были использовать замены. Так, из-за травмы спины <span lang=\"EN-US\"><strong>Chessie</strong></span>, им пришлось\nвоспользоваться услугами <span lang=\"EN-US\"><strong>H</strong></span><strong>4</strong><span lang=\"EN-US\"><strong>nni</strong></span> на <span lang=\"EN-US\"><strong>ESL</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>ONE</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>NY</strong></span>, и <span lang=\"EN-US\"><strong>Apemother</strong></span> на <span lang=\"EN-US\"><strong>Starladder</strong></span><span lang=\"EN-US\"> </span><span lang=\"EN-US\"><strong>X</strong></span>. А еще раньше <span lang=\"EN-US\"><strong>Key</strong></span> заменял <span lang=\"EN-US\"><strong>Akke</strong></span>, пока тот путешествовал в Японию.</p>\n\n<p><span lang=\"DE\"><strong>NaVi</strong></span><span lang=\"DE\"> </span>тоже недавно произвели изменения в своем составе, потому что\n<strong>62%</strong> побед показались им неприемлемыми. <span lang=\"EN-US\"><strong>Alliance</strong></span> же находится в гораздо более худшем положении после <span lang=\"EN-US\"><strong>TI</strong></span><strong>4</strong>, имея всего <strong>48,3%</strong> при 28\nпобедах и 30 поражениях. Так что их желание изменить свой состав вполне\nлогично.</p>\n\n<p><br></p><p>#Dota2, #Alliance<br></p>\n ",
        "ShortDescription": "Alliance не слишком хорошо живется после TI4. Поражения и несчастья преследуют команду по пятам, и вот теперь они, наконец, не вытерпев, решились на полномасштабное изменение состава. Подробнее читайте в новости.",
        "UrlFriendlyName": "alliance-otkazyvaetsya-ot-uchastiya-v-turnirax-dlya-pereformirovaniya-komandy",
        "PreviewImageUrl": "http://i.imgur.com/yoJBjYH.jpg",
        "DetailsLink": "/ru/news/alliance-otkazyvaetsya-ot-uchastiya-v-turnirax-dlya-pereformirovaniya-komandy",
        "CreatorNickname": null,
        "Created": "2014-11-11T06:08:25.453",
        "Published": "2014-11-11T06:08:25",
        "Tags": [ ],
        "LatestUserNews": [ ],
        "User": {
            "Nickname": "WalterBlake",
            "AvatarUrl": "http://img.cdn.esfxtv.com/UserProfile/UserPreview/eGeXsQ4X.cropped.jpg",
            "UserInfoLink": "/ru/user/walterblake"
        },
        "View": 50
    }

]
```

