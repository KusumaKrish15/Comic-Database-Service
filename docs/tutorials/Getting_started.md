# Getting started: a tutorial
<mark>Adapted from To-do service API overview. </mark>

<br>This tutorial shows you how to download the API files and try one of the available services. If you already [set up your development environment](/docs/tutorials/dev-env.md), the process should take about 15 minutes.

## Step 1: Confirm if you have the API files
The files are located in the [Comic-Database-Service repo](https://github.com/KusumaKrish15/Comic-Database-Service) on GitHub. The directory contains the following files:

- `comic-database-service.json`: a JSON file containing example comic books.
- `start-server.sh`: a shell script that starts JSON Server. Use this for Linux or macOS.
- `start-server.bat`: a batch file that starts JSON Server. Use this for Windows.

## Step 2: Start JSON Server with the `comic-book-database` service
1. Open a terminal window and `cd` to the location of the json-server app.
2. Make sure the API files are in the same directory.
3. Start the service by typing `json-server -w comic-book-database.json`. You should see some text to show the service is running:

    ```
     macBook:api <username>$ json-server -w comic-book-database.json

     \{^_^}/ hi!

     Loading comic-book-database.json
     Done

     Resources
     http://localhost:3000/comicBooks
     http://localhost:3000/comicTradePaperBacks

     Home
     http://localhost:3000

     Type s + enter at any time to create a snapshot of the database
     Watching...
    ```

## Step 3: List the comic books
You can use cURL or Postman to list all the comic books.

### If you’re using cURL
1. Open a terminal window.
2. Run this command:
```
curl http://localhost:3000/comicBooks
```
### If you’re using Postman
1 In Postman’s main panel select GET and add the following content to the URL text box: http://localhost:3000/comicBooks/.

## Step 4: Check the response
The response pane should show all the comic books. An example below. 
 ```
   {
     "batman": [
    {
      "issueNumber": 1,
      "publisher": "DC_Comics",
      "date": "Spring_1940",
      "conditionGrade": "7.5",
      "status": "Restored",
      "upcCode": "0087021001",
      "tradePrice": 198000,
      "currency": "USD"
    }

