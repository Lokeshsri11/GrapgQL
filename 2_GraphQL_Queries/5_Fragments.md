# Fragments
In GraphQL, a fragment is a reusable piece of a GraphQL query that can be used to retrieve specific fields from one or more types of data

Imagine you have a GraphQL schema with a type called User that has fields like name, email, and age. Now, you want to retrieve the same set of fields for multiple users in your query.

Here's where fragments come in handy:
```graphql
query GetUsers {
  user1: getUser(id: "1") {
    ...userFields
  }
  user2: getUser(id: "2") {
    ...userFields
  }
}

fragment userFields on User {
  name
  email
  age
}
```
In this example, we define a fragment called `userFields` that specifies the fields (`name`, `email`, and `age`) we want to retrieve from the `User` type. We then use the fragment within each user query (`user1` and `user2`) to include those fields.

The response would look something like this:
```json
{
  "data": {
    "user1": {
      "name": "Lokesh",
      "email": "Loki@gmail.com",
      "age": 20
    },
    "user2": {
      "name": "Raghav",
      "email": "Raghav@gmail.com",
      "age": 21
    }
  }
}
```

As you can see, the fragment allows us to reuse the same set of fields (name, email, and age) for multiple users in the query. It helps in reducing duplication and making the query more concise and maintainable.

