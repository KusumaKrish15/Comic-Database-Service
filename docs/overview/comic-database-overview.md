# Comic Database Service API

This is a mock API to simulate the REST interface of an imaginary service.

The Comic Database Service lets you search for a comic in the database. Use this API service to:
- Get a list of all comic books or a specific comic book by title from the database.
- Add a comic or a comic trade paperback book to the database.
- Update a comic or comic trade paperback book to the database.
- Retrieve the following details for each comic book and comic trade paperback in the database:
    - `issueNumber`: The specific issue number of the book.
    - `publisher`: The company that published the book.
    - `date`: The publication date of the book.
    - `conditionGrade`: The grade indicating the condition of the book.
    - `status`: The status of the comic book (e.g., Restored).
    - `upcCode`: The unique product code for the comic book.
    - `tradePrice`: The trade price of the comic book.
    - `currency`: The currency of the trade price.

## Tutorials

First, do this tutorial to set up your development system for these tutorials. You only have to do this one time per development system.

* [Setting up your development system](../tutorials/dev-env.md)

After your system is ready, these tutorials show you how to perform common tasks.
- [Getting started with the Comic Database Service API](../tutorials/Getting_started.md)
- [Add a new comic to the database](../tutorials/Add_a_new_comic.md)
- [Update an existing comic in the database](../tutorials/Update_a_comic.md)

## API reference docs

The API References show detailed descriptions of the service's resources.

> 📘 **NOTE**: The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service. When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

- [Get a list of comic books](../api/Get-comics.md)
- [Get a list of comic trade paperback books](../api/Get-comics-paperback.md)
- [Add a new comic book](../api/Post-comic.md)
- [Add a new comic trade paperback book](../api/Post-comic-paperback.md)

## API resources

These API resources and endpoints are available:
- [comicBook](../api/comicBook.md)
- [comicTradePaperBack](../api/comicTradePaperBack.md)
<br>
  
<p align="right"> ⏭️ [Setting up your development system](../tutorials/dev-env.md)
