Get All Comic Books or a Book by Title
Lists all comic books in the collection or a specific comic book by title.
Method: GET
Endpoints
•	List all comic books: {base_url}/comicBooks
•	Get a comic book by title: {base_url}/comicBooks/{title}
Base URL Parameters
•	Optional: The title of a specific comic book to list.
Headers
Content-Type: application/json
Request Body
None required.
cURL Example
Returns the comic book with the title "batman".
curl -X GET http://localhost:3000/comicBooks/batman
Postman Example
Request builder method and endpoint:
•	Select GET and enter http://localhost:3000/comicBooks/batman.
Request builder body:
None required.
Return Body
Returns all comic books or the specific comic book requested. The following example shows the result of requesting the comic book with the title "batman":
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
Postman Return Status
Status Value	Return Status Description
200	OK - Request successful. The server has responded as required.
404	Not Found - Requested resource could not be found.
This documentation provides details on how to fetch all comic books or a specific comic book by its title, using both cURL and Postman examples.

