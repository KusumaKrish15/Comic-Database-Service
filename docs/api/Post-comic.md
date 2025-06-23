# Add a new comic
Creates a new comic book entry in the collection.

## Method: 
`POST`

## URL
`{base_url}/comicBooks`

## Base URL parameters
**Optional**: You should include all properties: title, issueNumber, publisher, date, conditionGrade, status, upcCode, tradePrice, and currency.
The service automatically assigns the new comic book a unique ID.

## Headers
`Content-Type: application/json`

## Request body
A JSON object containing the properties of the comic book to be added.

### cURL example
Shows creating a new comic book titled "Batman".

```
curl -X POST \
-H "Content-Type: application/json" \
-d '{ 
  "title": "batman",
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "Spring_1940",
  "conditionGrade": "7.5",
  "status": "Restored",
  "upcCode": "0087021001",
  "tradePrice": 198000.00,
  "currency": "USD"
}' \
http://localhost:3000/comicBooks
```

## Response
Returns the information from the request body plus a unique ID for the comic book.

```
{
  "title": "batman",
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "Spring_1940",
  "conditionGrade": "7.5",
  "status": "Restored",
  "upcCode": "0087021001",
  "tradePrice": 198000.00,
  "currency": "USD",
  "id": 5
}
```

## Return status

| Status value | Return status | Description |
| --- | --- | --- |
| 201 | Created | A new resource was created successfully |


<br>
<br>

**Next** ⏭️ [Add a new comic trade paperback book](../api/Post-comic-paperback.md)
