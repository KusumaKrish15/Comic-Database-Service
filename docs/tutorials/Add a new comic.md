## Prerequisites
- You have a REST API endpoint that allows you to add new comic books.
- The endpoint URL is https://api.example.com/comics.
- The JSON server or API server is running and accessible.

## Step 1. Prepare the JSON Data
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

2. cURL Command to Add the New Comic Book
Use the POST method to send the JSON data to the server. Assuming the server expects the new comic book data under the "greenLantern" category, you can do this with the following cURL command:

curl -X POST "https://api.example.com/comics/greenLantern" \
     -H "Content-Type: application/json" \
     -d @new_comic.json
Example with json-server
If you are using json-server, follow these steps:

1. Install json-server (if not already installed)
npm install -g json-server
2. Create a db.json File with Initial Data
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
3. Start json-server
json-server --watch db.json
4. Create new_comic.json File with New Comic Data
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
5. Use cURL to Add the New Comic Book
curl -X POST "http://localhost:3000/comicBooks/greenLantern" \
     -H "Content-Type: application/json" \
     -d @new_comic.json
Verifying the Addition
To verify that the comic book has been added, you can use a GET request:

curl -X GET "http://localhost:3000/comicBooks/greenLantern" -H "accept: application/json"
This should return the details of the newly added "Green Lantern" comic book.

Summary
You have successfully added a new comic book to your collection using cURL. This tutorial covers creating the JSON data, using cURL commands to make POST requests, and verifying the addition. If you have any further questions or need more examples, feel free to ask!
