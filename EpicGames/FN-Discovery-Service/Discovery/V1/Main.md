## FN - Discovery Service: Discovery Surface (V1)

URL: https://fn-service-discovery-live-public.ogs.live.on.epicgames.com/api/v1/discovery/surface/:accountId \
Method: POST \
Auth Required: Yes (`discovery:{accountId}:surface:query READ`)

## Headers

`User-Agent`: From FN, e.g. `Fortnite/++Fortnite+Release-18.40-CL-18163738 Windows/10`

<br/>

```json
{
  "surfaceName": "",
  "revision": -1,
  "partyMemberIds": [],
  "matchmakingRegion": "EU",
  "isCabined": true,
  "platform": "Windows"
}
```

## Path Parameters

`accountId`: Your Account Id

## Parameters

`surfaceName`: See [Surfaces](../README.md#surfaces) <br/>
`revision`: Leave -1 for latest <br/>
`partyMemberIds`: Array of the party member account ids (or an empty array) <br/>
`matchmakingRegion`: Your matchmaking region (e.g. `EU`) <br/>
`isCabined`: If your Account is in Cabined Mode (from [own account info](../../../AccountService/Account/Lookup/AccountId.md)) <br/>
`platform`: Your platform (e.g. `Windows`)

## Query Parameters

`appId`: `Fortnite`

---

_Example Response (shortened)_

```json
{
  "panels": [
    {
      "panelName": "RecentlyPlayed",
      "pages": [
        {
          "results": [
            {
              "lastVisited": "2023-05-18T21:13:29.825Z",
              "linkCode": "set_habanero_playlists",
              "isFavorite": false,
              "globalCCU": 157402
            }
          ],
          "hasMore": true
        }
      ]
    },
    {
      "panelName": "Favorites",
      "pages": [
        {
          "results": [
            {
              "linkCode": "1234-1234-1234",
              "isFavorite": true,
              "globalCCU": -1
            }
          ],
          "hasMore": true
        }
      ]
    }
  ],
  "testCohorts": ["librarytest"]
}
```