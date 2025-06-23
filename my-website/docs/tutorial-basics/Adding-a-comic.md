---
sidebar_position: 7
---

# Adding a new comic

This tutorial covers adding a new comic book to the database. You'll learn how to create the JSON data, use cURL commands to make POST requests, and verify the addition. 

## Prerequisites
- You have a REST API endpoint that allows you to add new comic books.
- The endpoint URL is `POST http://localhost:3000/comicBooks`.
- The JSON server or API server is running and accessible.

## Step 1. Prepare the JSON data
1. Create a JSON object representing the new comic book you want to add. For example, let's add a new "Green Lantern" comic book:

```
{
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "July_1940",
  "conditionGrade": "9.0",
  "status": "Restored",
  "upcCode": "0087021005",
  "tradePrice": 250000.00,
  "currency": "USD"
}
```
2. Save this JSON data in a file called `new_comic.json`.

## Step 2. cURL command to add the new book
1. Use the POST method to send the JSON data to the server. To add the new comic book data under the "greenLantern" category, use the following cURL command:

```
curl -X POST "https://api.example.com/comics/greenLantern" \
     -H "Content-Type: application/json" \
     -d @new_comic.json
```

## Step 3: Using with the json-server
Follow these steps:

1. Start the json server
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
4. Create `new_comic.json` file with new comic data. An example below:

```   
{
  "issueNumber": 1,
  "publisher": "DC_Comics",
  "date": "July_1940",
  "conditionGrade": "9.0",
  "status": "Restored",
  "upcCode": "0087021005",
  "tradePrice": 250000.00,
  "currency": "USD"
}
```

5. Use cURL to add the new comic book.

```
curl -X POST "http://localhost:3000/comicBooks/greenLantern" \
     -H "Content-Type: application/json" \
     -d @new_comic.json
```

## Step 4: Verifying the addition
1. To verify that the comic book has been added, you can use a GET request:

```
curl -X GET "http://localhost:3000/comicBooks/greenLantern" -H "accept: application/json"
```

2. This should return the details of the newly added "Green Lantern" comic book.

You have successfully added a new comic book to your collection using cURL. 
