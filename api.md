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
* Allow keeping the connection alive
* Allow server to push response to client
* Good for real time application
* Still not easy to scale.
* GraphQL subscription even runs on WebSocket
* But I don't know where to put it.
