# What are Mutations 
In GraphQL, a mutation is a type of query used to make changes to data on the server.

Imagine you have a web application where users can create and update their profiles. You also have a GraphQL API that serves as the backend for your application. In this scenario, you would use mutations to make changes to the user profiles stored on the server.
Let's say you want to create a new user profile. In GraphQL, you would use a mutation to achieve this. You would define a mutation called "createUserProfile" and specify the necessary fields to create the user profile, such as the user's name, email, and password.
Here's an example of how the mutation might look in GraphQL syntax:
```graphql
mutation {
  createUserProfile(name: "John Doe", email: "john@example.com", password: "password123") {
    id
    name
    email
  }
}
```
In this example, the mutation is named "createUserProfile", and it takes three arguments: name, email, and password. These arguments specify the data needed to create a new user profile. The fields inside the curly braces after the mutation specify the data that should be returned after the mutation is performed, such as the newly created user's ID, name, and email.

Once you send this mutation to the GraphQL server, it will create a new user profile with the provided data and return the specified fields in the response.

Similarly, you can use mutations to update or delete user profiles. For updating, you would define a mutation like "updateUserProfile" and provide the necessary arguments for identifying the profile to update, as well as the fields to be modified. For deleting, you would define a mutation like "deleteUserProfile" and specify the identifier of the profile to be deleted.

Mutations in GraphQL provide a standardized and structured way to perform changes to data on the server, allowing you to create, update, or delete data easily and efficiently.