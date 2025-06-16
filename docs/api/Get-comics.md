# Get all comic books or a book by title

Lists all comic books in the collection or a specific comic book by title.

## Method

`GET`

## Endpoints
•	**List all comic books**: `{base_url}/comicBooks` <br>
•	**Get a comic book by title**: `{base_url}/comicBooks/{title}` 

## Base URL parameters
•	**Optional**: The title of a specific comic book to list.

## Headers

`Content-Type: application/json`

## Request body

None required

### cURL example
Returns the comic book with the title "batman".

```
curl -X GET http://localhost:3000/comicBooks/batman
```

## Return body
Returns all comic books or the specific comic book requested. The following example shows the result of requesting the comic book with the title "batman":

```json
{
  "title": "batman",
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "Spring_1940",
  "conditionGrade": "7.5",
  "status": "Restored",
  "upcCode": "0087021001",
  "tradePrice": 198000.00,
  "currency": "USD"
}
```

## Post return status

| Status value | Return status | Description |
| ------------ | ------------- | ------------------------------------------------------------ |
| 200          | OK       | Request successful. The server has responded as required |
| 400          | Bad Request   | The server couldn't understand the request |
| 404 | Not Found | Requested resource could not be found |

