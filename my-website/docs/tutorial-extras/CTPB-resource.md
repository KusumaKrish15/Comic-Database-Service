---
sidebar_position: 2
---

# `comicTradePaperBack` resource

**Base endpoint**:

```shell

{server_url}/comicTradePaperBacks

```

Contains information about the comic trade paperbacks in the collection. A comicTradePaperBack resource describes the details of individual trade paperbacks including the issue number, publisher, and other relevant details.

## Resource properties

Sample `comicTradePaperBack` resource

```js

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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The title of the comic trade paperback (e.g., "conanTheBarbarian") |
| `issueNumber` | number | The issue number of the comic trade paperback |
| `publisher` | string | The publisher of the comic trade paperback |
| `date` | string | The publication date of the comic trade paperback |
| `conditionGrade` | string | The condition grade of the comic trade paperback |
| `status` | string | The restoration status of the comic book |
| `upcCode` | string | The UPC code of the comic trade paperback |
| `tradePrice` | number | The trade price of the comic trade paperback |
| `currency` | string | The currency used for the trade price |

This resource can be used to manage the collection of comic trade paperbacks, including adding, updating, and retrieving detailed information about each trade paperback in the collection.

