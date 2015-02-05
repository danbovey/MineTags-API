# MineTags-API

The API endpoints start at `http://api.boveybrawlers.com/minetags`.

## Retreive MineTags by rank

To show a list of the top MineTags, send a POST request to `/top`.

| Name  | Type   | Default  |
|-------|--------|----------|
| page  | number | 0        |
| limit | number | 5        |

**Curl Example**

    curl -X POST -H 'Content-Type: application/json' -d '{"page":0,"limit":5}' "http://api.boveybrawlers.com/minetags/top"
    
**Request Headers**

    Content-type: application/json

**Response Headers**

    content-type: application/json; charset=utf-8
    status: 200 OK
    
**Response Body**

    {
      "minetags": [
        {
          "name": "AbsoluteCraft",
          "amount": 9
        },
        ...
      ]
    }

## Retreive MineTag by name

To get information about one MineTag, send a GET request to `/tag/$NAME`.

**Curl Example**

    curl -X GET "http://api.boveybrawlers.com/minetags/tag/AbsoluteCraft"
    
**Response Headers**

    content-type: application/json; charset=utf-8
    status: 200 OK
    
**Response Body**

    {
      "minetag": {
        "name": "AbsoluteCraft",
        "amount": 9
      }
    }
