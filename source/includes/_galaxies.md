# Galaxies

## Get All Galaxies

This endpoint retrieves all galaxies.

### HTTP Request

`GET https://api.imperialconflict.com/galaxies`

### URL Parameters

Parameter | Description
--------- | -----------
page | An optional page number to retrieve items in sets of 20

```shell
curl "https://api.imperialconflict.com/galaxies"
  -H "Authorization: Bearer API_AUTH_TOKEN"
```

> The above command returns JSON similar to below.  The results have been shortened for readability:

```json
{
    "data": [
        {
            "type": null,
            "id": "1",
            "attributes": {
                "name": "Milky Way",
                "slug": "milky-way",
                "short_name": "MW",
                "official": 1
            }
        },
        {
            "type": null,
            "id": "2",
            "attributes": {
                "name": "Andromeda",
                "slug": "andromeda",
                "short_name": "Andro",
                "official": 1
            }
        },
        {
            "type": null,
            "id": "21",
            "attributes": {
                "name": "Terra",
                "slug": "terra",
                "short_name": "terra",
                "official": 0
            }
        }
    ],
    "meta": {
        "pagination": {
            "total": 26,
            "count": 20,
            "per_page": 20,
            "current_page": 1,
            "total_pages": 2
        }
    },
    "links": {
        "self": "https://api.imperialconflict.com/galaxies?page=1",
        "first": "https://api.imperialconflict.com/galaxies?page=1",
        "next": "https://api.imperialconflict.com/galaxies?page=2",
        "last": "https://api.imperialconflict.com/galaxies?page=2"
    }
}
```

## Get a Specific Galaxy

This endpoint retrieves a specific galaxy.

### HTTP Request

`GET https://api.imperialconflict.com/galaxies/<slug>`

### URL Parameters

Parameter | Description
--------- | -----------
slug | The slug (short-name) of the galaxy to retrieve

```shell
curl "https://api.imperialconflict.com/galaxies/milky-way"
  -H "Authorization: Bearer API_AUTH_TOKEN"
```

> The above command returns JSON structured like this:

```json
{
  "data": {
    "type": null,
    "id": "milky-way",
    "attributes": {
      "name": "Milky Way",
      "slug": "milky-way",
      "short_name": "MW",
      "official": 1
    }
  }
}
```
