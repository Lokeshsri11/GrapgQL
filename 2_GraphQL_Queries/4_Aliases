# Aliases 
Aliases in GraphQL are a way to rename fields when they are requested in a query.

Imagine you have a GraphQL schema that includes a field called fullName, which combines a person's first name and last name. Now, you want to request the full name of two different people in a single query.
```graphql
query GetPeople {
  person1: person(id: "1") {
    fullName
  }
  person2: person(id: "2") {
    fullName
  }
}
```
In this example, we use aliases (person1 and person2) to differentiate between the two requests for the fullName field. By assigning each request a unique alias, we can easily identify and work with the specific data in the response.

The response would look something like this:
```json
{
  "data": {
    "person1": {
      "fullName": "Lokesh"
    },
    "person2": {
      "fullName": "Raghav"
    }
  }
}
```
As you can see, the response contains the aliases (`person1` and `person2`) as the keys, allowing you to access the corresponding full names (`Lokesh` and `Raghav`).

Using aliases not only helps in cases where you request the same field multiple times but also when the field name itself is not suitable for your specific use case. Aliases provide a way to make your query more readable and work with the response more conveniently.