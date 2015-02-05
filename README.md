# MineTags-API

## Retreive MineTags by rank

To show a list of the top MineTags, send a GET request to `/api/top`.

| Name  | Type   | Default  |
|-------|--------|----------|
| page  | number | 0        |
| limit | number | 5        |

**Curl Example**

    curl -X GET -H 'Content-Type: application/json' "http://boveybrawlers.com/minetags/api/top"
    
**Request Headers**

    Content-type: application/json

**Response Headers**
    content-type: application/json; charset=utf-8
    status: 200 OK

## Retreive MineTag by name

To get information about one MineTag, send a GET request to `/api/tag/$HASHTAG`.

