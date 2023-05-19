# What are Subscription
In GraphQL, subscriptions are like having a live stream of updates from the server. They enable clients to subscribe to specific events or data changes and receive real-time updates as soon as those events occur or the data changes.

Let's say you have a chat application built with GraphQL. With subscriptions, you can provide real-time updates to users whenever a new message is sent in a chat room. Here's an example of how subscriptions work:

```graphql
subscription NewMessage {
  messageAdded(chatRoomId: "123") {
    id
    content
    sender
    timestamp
  }
}
```
In the above example, we define a subscription named `NewMessage`. It specifies that we want to subscribe to new messages in a particular chat room with the ID `"123"`. The fields within the `messageAdded` field indicate the data we want to receive for each new message, such as the message ID, content, sender, and timestamp.

Once the client subscribes to this subscription, it establishes a long-lived connection with the server. Whenever a new message is added in the specified chat room, the server pushes the updated message data to all subscribed clients in real-time. Clients can then update their user interface or take any necessary actions based on the received updates.