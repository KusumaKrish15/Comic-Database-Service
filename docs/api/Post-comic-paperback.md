## Add a new comic trade paperback book
Creates a new comic trade paperback book entry in the collection.

## Method: 
`POST`

## URL
`{base_url}/comicTradePaperBacks`

## Base URL parameters
**Optional**: You should include all properties: title, issueNumber, publisher, date, conditionGrade, status, upcCode, tradePrice, and currency.
The service automatically assigns new comic trade paperback book a unique ID.

## Headers
`Content-Type: application/json`

## Request body
A JSON object containing the properties of the comic trade paperback book to be added.

### cURL example
Shows creating a new comic trade paperback book titled "Conan The Barbarian".

```
curl -X POST \
-H "Content-Type: application/json" \
-d '{ 
  "title": "conanTheBarbarian",
  "issueNumber": 1,
  "publisher": "Marvel_Comics",
  "date": "October_1970",
  "conditionGrade": "9.6",
  "status": "Restored",
  "upcCode": "4591364011",
  "tradePrice": 3500.00,
  "currency": "USD"
}' \
http://localhost:3000/comicTradePaperBacks
```

## Response
Returns the information from the request body plus a unique ID for the comic trade paperback book.

```
{
  "title": "conanTheBarbarian",
  "issueNumber": 1,
  "publisher": "Marvel_Comics",
  "date": "October_1970",
  "conditionGrade": "9.6",
  "status": "Restored",
  "upcCode": "4591364011",
  "tradePrice": 3500.00,
  "currency": "USD",
  "id": 5
}
```

## Return status

| Status value | Return status | Description |
| --- | --- | --- |
| 201 | Created | A new resource was created successfully |
