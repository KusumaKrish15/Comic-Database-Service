---
layout: page
---

# `comicBook` resource

**Base endpoint**:

```shell

{server_url}/comicBooks
```

Contains information about the comic books in the collection. A comicBook resource describes the details of individual comic books including the issue number, publisher, and other relevant details.

## Resource properties

Sample `comicBook` resource

```js

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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The title of the comic book (e.g., "batman") |
| `issueNumber` | number | The issue number of the comic book |
| `publisher` | string | The publisher of the comic book |
| `date` | string | The publication date of the comic book |
| `conditionGrade` | string | The condition grade of the comic book |
| `status` | string | The restoration status of the comic book |
| `upcCode` | string | The UPC code of the comic book |
| `tradePrice` | number | The trade price of the comic book |
| `currency` | string | The currency used for the trade price |

This resource can be used to manage the collection of comic books, including adding, updating, and retrieving detailed information about each comic book in the collection.


