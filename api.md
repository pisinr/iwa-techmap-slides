# API

---

## How server communicate the data to the client.

* REST/JSON-API
* GraphQL
* WebSocket

---

## REST/JSON-API

* You know, the usual.
* Response shape is hard coded.
* Problem with Overfetch Underfetch
* Easy to optimize of cases
  * But hard to response to changes

---

## GraphQL

* One side: a Graph Query Langue
* Another: A Server that knows how to responds to the query.

^^^

## GraphQL: Query

* Ask for just what you want.
* Ask for needed graph connections
* Strong Type Schema

```graphql
query {
    activeUsers(first: 10) {
        id
        username
        likedPosts {
            id
            url
            authorUser {
                id
                username
            }
        }
    }
}
```

^^^

## GraphQL: Server

* Apollo server, Absinthe
* Provide "resolver" on how to load a type.
  How to load "activeUsers"
* Provide how to load a connection of an instance
  * Given a User, how to load "likedPosts"
  * Given a Post, how to load its "authorUser"
* GraphQL server will then make the compose.

^^^

## Is it good?

* Require practices:
  * Optimization
  * Handling attacks
  * Authorization

---

## WebSocket??

* THIS IS COMPLETELY DIFFERENT THING
* It's not even related to REST or GraphQL!?!
* But I don't know where to put it.

^^^

* Allow keeping the connection alive
* Allow server to push response to client
* Data is sent in "frame".
* Good for real time application
* Still not easy to scale.
* GraphQL subscription even runs on WebSocket

---

## JWT

* Another thing I don't know where to put.
* It's a explicit cookies.
* It's not tied to a domain.
* It's stateless

[JWT](https://jwt.io/)

^^^

## So what is it?

* JSON object with signed checksum.
* Server can store data there and give it to clients.
* It's signed. They can't modify it.
* You don't need to hit database to trust that data.

^^^

If you have to hit "User" DB on every request, you don't gain much from JWT.