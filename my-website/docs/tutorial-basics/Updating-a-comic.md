---
sidebar_position: 7
---

# Update a comic
This tutorial covers updating an existing comic book. You'll learn how to update the JSON data, use cURL commands to make PUT requests, and verifying the update.

## Prerequisites
- You have a REST API endpoint that allows you to add new comic books.
- The endpoint URL is `PUT http://localhost:3000/comicBooks/{category}/{id}`, where `{category}` is the specific comic book category (e.g., batman) and `{id}` is the unique identifier of the comic book.
- The JSON server or API server is running and accessible.

## Step 1. Prepare the JSON data for update
1. Create a JSON object representing the updated data for the comic book. For example, let's update the Batman comic book's condition and trade price:

```
{
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "Spring_1940",
  "conditionGrade": "8.0",
  "status": "Restored",
  "upcCode": "0087021001",
  "tradePrice": 210000.00,
  "currency": "USD"
}
```

2. Save this JSON data in a file called `update_comic.json`.

## Step 2. cURL command to update the comic book
1. Use the PUT method to send the JSON data to the server. 

```
curl -X PUT "http://localhost:3000/comicBooks/batman/1" \
     -H "Content-Type: application/json" \
     -d @update_comic.json
```

## Step 3: Using with the json-server
Follow these steps:

1. Start the json server.
2. Verify the comic-book-database.json file with the initial data. An excerpt below:

```
{
  "comicBooks": {
    "batman": [
      {
        "issueNumber": 1,
        "publisher": "DC_Comics",
        "date": "Spring_1940",
        "conditionGrade": "7.5",
        "status": "Restored",
        "upcCode": "0087021001",
        "tradePrice": 198000.00,
        "currency": "USD"
      }
    ]
  }
}
```

3. Start json-server using the command: `json-server -w comic-book-database.json`
4. Create `update_comic.json` file with an updated content. An example below:

```   
{
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "Spring_1940",
  "conditionGrade": "8.0",
  "status": "Restored",
  "upcCode": "0087021001",
  "tradePrice": 210000.00,
  "currency": "USD"
}
```

5. Use cURL to update the comic book.

```
curl -X PUT "http://localhost:3000/comicBooks/batman/1" \
     -H "Content-Type: application/json" \
     -d @update_comic.json
```

## Step 4: Verifying the update
1. To verify that the comic book has been added, you can use a GET request:

```
curl -X GET "http://localhost:3000/comicBooks/batman/1" -H "accept: application/json"
```

2. This should return the updated details of the "Batman" comic book.

You have successfully updated an existing comic book using cURL. 
