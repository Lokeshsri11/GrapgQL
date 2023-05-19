# Operation Name
In GraphQL, an operation name is a way to give a meaningful identifier to a query or a mutation. It's like giving a name to a function or a method in programming, so you can refer to it easily and understand its purpose.

Here's an example to illustrate how an operation name is used:
```graphql
query GetUserInfo {
  user(id: "123") {
    name
    email
    age
  }
}
```
In the above example, `GetUserInfo` is the operation name. It provides a clear and descriptive name for the query, indicating that we want to retrieve user information.

Operation names are also useful when you have multiple queries or mutations in a single GraphQL document. By providing a unique name for each operation, you can refer to them individually when executing the document.

```graphql
query GetUserInfo {
  user(id: "123") {
    name
    email
  }
}

mutation UpdateUser {
  updateUser(id: "123", input: { name: "Loki" }) {
    id
    name
  }
}
```

In this example, we have two operations: `GetUserInfo` for querying user information and `UpdateUser` for updating a user's name. Each operation has a distinct name, making it clear what action it performs.

Using operation names in GraphQL helps improve clarity, understandability, and error handling when working with multiple operations in a single document.
