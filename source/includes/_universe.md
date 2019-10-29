# Universe

## Get Universe

This endpoint retrieves information about the Imperial Conflict universe.

### HTTP Request

`GET https://api.imperialconflict.com/universe`

```shell
curl "https://api.imperialconflict.com/universe "
  -H "Authorization: Bearer API_AUTH_TOKEN"
```

> The above command returns JSON structured like this:

```json
{
  "name": "Imperial Conflict",
  "description": "Imperial Conflict is a free online browser-based massively multiplayer online strategy game set in space. Players interact in cooperation and against other players in a quest to \"Rule The Galaxy\".",
  "tags": [
    "space",
    "strategy",
    "military"
  ],
  "players": {
    "registered": 49387,
    "active": 248
  },
  "links": {
    "website": "https://imperialconflict.com",
    "forum": "https://discourse.imperialconflict.com",
    "discord": "https://discord.gg/yVZjc4M",
    "patreon": "https://www.patreon.com/imperialconflict",
    "facebook": "https://www.facebook.com/imperialconflict/",
    "twitter": "https://twitter.com/ic_game",
    "reddit": "https://www.reddit.com/r/ImperialConflict/",
    "pbbg.com": "https://pbbg.com/games/imperial-conflict",
    "PBBG Wiki": "https://wiki.pbbg.com/wiki/Imperial_Conflict"
  },
  "data": {
    "empires": {
      "active": 301
    },
    "galaxies": {
      "active": 4
    },
    "patreon_subscriber_credits": [
      "RUNIC",
      "Rivan",
      "Jets",
      "Ushanewnewba",
      "SCORP",
      "kingray",
      "Zeraph",
      "RenegadeDamon",
      "Goddess_of_the_Dead",
      "Tishxo",
      "Zeratel",
      "Usha"
    ]
  }
}
```
