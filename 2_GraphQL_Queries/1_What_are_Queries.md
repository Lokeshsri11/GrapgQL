# What is Queries
In GraphQL, a query is like a request you make to the server to get the data you want. It's a way of asking the server, "Hey, give me this specific information!"

Imagine you're building an app for a library, and you want to display a list of books. With GraphQL, you can send a query to the server like this:

```graphql
query {
  books {
    title
    author
    publicationDate
  }
}
```
In this query, you're asking the server for information about books. You specify the fields you're interested in: `title`, `author`, and `publicationDate`. It's like telling the server, "Please give me the title, author, and publication date of each book."

The server will then process the query and send back a response with the requested data. For example, you might receive a response like this:

```json
{
  "data": {
    "books": [
      {
        "title": "Loki the Iron Man",
        "author": "Lokesh Srivastava",
        "publicationDate": "2002"
      }
      ...
    ]
  }
}
```
The response contains an array of books, and each book has the fields you requested: `title`, `author`, and `publicationDate`. You can then use this data to display the book information in your app.

So, in simple terms, a query in GraphQL is a way of asking the server for specific data. You specify the fields you want, and the server responds with the requested data. It's like ordering exactly what you need from a menu and getting exactly that.



