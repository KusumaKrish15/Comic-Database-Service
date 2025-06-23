# Get all comic trade paperback books or a trade paperback book by title

Use the endpoints below to list all comic trade paperback books in the collection or a specific comic trade paperback book by title.

## Method

`GET`

## Endpoints
•	**List all comic trade paperback books**: `{base_url}/comicTradePaperBacks` <br>
•	**Get a comic trade paperback book by title**: `{base_url}/comicTradePaperBacks/{title}` 

## Base URL parameters
•	**Optional**: The title of a specific comic trade paperback book to list.

## Headers

`Content-Type: application/json`

## Request body

None required

### cURL example
Returns the comic trade paperback book with the title "conanTheBarbarian".

```
curl -X GET http://localhost:3000/comicTradePaperBacks/conanTheBarbarian
```

## Return body
Returns all comic trade paperback books or the specific comic trade paperback book requested. The following example shows the result of requesting the comic trade paperback book with the title "conanTheBarbarian":

```json
{
  "title": "conanTheBarbarian",
  "issueNumber": 1,
  "publisher": "Marvel_Comics",
  "date": "October_1970",
  "conditionGrade": "9.6",
  "status": "Restored",
  "upcCode": "4591364011",
  "tradePrice": 3500.00,
  "currency": "USD"
}
```

## Return status

| Status value | Return status | Description |
| ------------ | ------------- | ------------------------------------------------------------ |
| 200          | OK       | Request successful. The server has responded as required |
| 400          | Bad Request   | The server couldn't understand the request |
| 404 | Not Found | Requested resource could not be found |

This documentation provides details on how to fetch all comic trade paperback books or a specific comic trade paperback book by its title, using a cURL example.


<br>
<br>

<mark>**Next** ⏭️ [Add a new comic book](../api/Post-comic.md)</mark>
