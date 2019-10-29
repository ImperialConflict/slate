# Empires

## Get a Specific Empire

This endpoint retrieves a specific empire.

### HTTP Request

`GET https://api.imperialconflict.com/empires/id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The Empire ID

```shell
curl "https://api.imperialconflict.com/empires/383727"
  -H "Authorization: Bearer API_AUTH_TOKEN"
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "type": "empires",
    "id": "383727",
    "attributes": {
      "user_id": 102051,
      "name": "fearl3ss",
      "ruler": "Dron3s",
      "banner_filename": null,
      "family_id": 4291,
      "family_role_type_id": 2,
      "population": 743553,
      "planets_count": 85,
      "networth": 1149234,
      "home_planet_coordinates": {
        "x": 72,
        "y": 91,
        "number": 7
      }
    },
    "relationships": {
      "round": {
        "data": {
          "type": "rounds",
          "id": "23"
        }
      },
      "race": {
        "data": {
          "type": "races",
          "id": "621562"
        }
      }
    }
  },
  "included": [
    {
      "type": "rounds",
      "id": "23",
      "attributes": {
        "name": "Milky Way 56"
      }
    },
    {
      "type": "races",
      "id": "621562",
      "attributes": {
        "name": "CFO"
      }
    }
  ]
}
```
