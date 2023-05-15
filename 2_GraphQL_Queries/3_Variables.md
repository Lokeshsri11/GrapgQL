# Variables in GraphQL
Variables in GraphQL allow you to pass dynamic values to a query or a mutation. They make your queries more flexible by allowing you to reuse the same query with different input values.

Imagine you want to ask a server for information about a specific person, but you don't know their name yet. In GraphQL, variables come to the rescue!
Variables allow you to pass in dynamic values to your queries or mutations. It's like filling in a blank space with the actual value when you make the request.
Here's an example to help you understand:

Let's say you have the following query to get details about a person:
```graphql
query GetPerson {
  person(name: "Lokesh") {
    name
    age
    occupation
  }
}
```
In this query, "John" is hardcoded as the name. But what if you want to retrieve information about a different person? That's where variables come in.

You can modify the query to use a variable instead:
```graphql
query GetPerson($name: String!) {
  person(name: $name) {
    name
    age
    occupation
  }
}
```
In this updated query, $name is a variable of type String! (a non-null string). It represents the name of the person you want to retrieve.

When you actually make the request, you provide the value for the variable separately, like this:
```json
{
    "name": "Lokesh"
}
```
In this JSON object, you specify the value for the $name variable. Here, we're using the name "Lokesh".

By using variables, you can easily change the name value without modifying the query itself. It gives you the flexibility to ask for different people's information without rewriting the whole query each time.

Variables in GraphQL also help ensure that the provided values match the expected types, keeping things safe and reliable.

I hope this simplified explanation makes variables in GraphQL easier to understand!