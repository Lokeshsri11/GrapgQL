# Multiple Mutation
In GraphQL, you can simplify and consolidate multiple mutations into a single query using multiple "mutation" fields. This approach is often referred to as "batching" or "chaining" mutations. It allows you to send multiple mutation requests to the server in a single round trip, improving efficiency and reducing network overhead.

Let's say you have a GraphQL schema that supports mutations for creating and updating user information. Here's an example of how you can use multiple mutation fields to perform batch mutations:

```graphql
mutation {
  createUser(input: {name: "Lokesh", email: "Lokesh@example.com"}) {
    id
    name
    email
  }
  updateUser(id: "123", input: {name: "Lokesh", age: 20}) {
    id
    name
    age
  }
  deleteUser(id: "456") {
    success
  }
}
```
In the above example, we have three mutation fields: `createUser`, `updateUser`, and `deleteUser`. Each mutation field takes parameters specific to its operation, such as `input` for creating/updating user data and id for deleting a user.

By combining these mutation fields within a single `mutation` block, you can execute them all together in a single GraphQL request. In the response, you'll receive the corresponding results for each mutation field.

The server will process each mutation in the order they appear in the request and return a response with the data you requested. This approach allows you to perform multiple mutations efficiently without making separate requests for each operation.

Keep in mind that the ability to perform batch mutations using multiple mutation fields depends on how the GraphQL server is implemented. Not all GraphQL servers support this feature out of the box, so it's essential to check the documentation or the capabilities of the server you are using.

By utilizing multiple mutation fields, you can simplify and optimize your GraphQL queries, making your code more concise and reducing unnecessary network traffic.