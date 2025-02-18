# Authentication

Imperial Conflict uses an API auth token to allow access to the API. This token is generated by passing API client credentials to an authentication endpoint.  You can request these credentials by joining our [Volunter Developers group](https://discourse.imperialconflict.com/g/volunteer_developers).

## Retrieving API Auth Token

Once you have your API client credentials, you can POST them to /ouath/token to retrieve your API auth token to be used for subsequent requests.

### HTTP Request

`POST https://api.imperialconflict.com/oauth/token`

> To retrieve an auth token, send your credentials with the following post body:

```shell
curl -v https://api.imperialconflict.com/oauth/token \
   -H "Accept: application/json" \
   -u "CLIENT_ID:CLIENT_SECRET" \
   -d "scope":"*" \
   -d "grant_type=client_credentials"
```

> The above command returns JSON structured like this:

```json
{
    "token_type": "Bearer",
    "expires_in": 31622400,
    "access_token": "API_AUTH_TOKEN"
}
```

<aside class="notice">
Make sure to replace <code>CLIENT_ID</code> and <code>CLIENT_SECRET</code> with your actual values.
</aside>

## Passing API Auth Token

Imperial Conflict expects for the API auth token to be included in all API requests to the server in a header that looks like the following:

> To authorize, use this code:

```shell
curl "api_endpoint_here"
  -H "Authorization: Bearer API_AUTH_TOKEN"
```

`Authorization: Bearer API_AUTH_TOKEN`

<aside class="notice">
Make sure to replace <code>API_AUTH_TOKEN</code> with an actual token.
</aside>
