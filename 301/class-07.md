# read 7
# REST

**`Roy Thomas Fielding` :** **is an American computer scientist, one of the principal authors of the HTTP specification and the originator of the Representational State Transfer (REST) architectural style. He is an authority on computer network architecture and co-founded the Apache HTTP Server project**

## Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

we have a `clash names` of may location for an example we have an Amman founded in Gaza and Jordan. And i need on of them te returned not both or trying to get on of this tow locations.

## HTTP

>**The Hypertext Transfer Protocol (HTTP) is an application-level protocol for distributed, collaborative, hypermedia information systems.**

# HTTP Methods

* **GET**
    * `GET is used to request data from a specified resource.` 
    * `GET is one of the most common HTTP methods.`
    * `Some other notes on GET requests:`
        * *GET requests can be cached*
        * *GET requests remain in the browser history*
        * *GET requests can be bookmarked*
        * *GET requests should never be used when dealing with sensitive data*
        * *GET requests have length restrictions*
        * *GET requests are only used to request data (not modify)*

* **POST**
    * `POST is used to send data to a server to create/update a resource.`
    * `POST is one of the most common HTTP methods.`
    * `Some other notes on POST requests:`
        * *POST requests are never cached*
        * *POST requests do not remain in the browser history*
        * *POST requests cannot be bookmarked*
        * *POST requests have no restrictions on data length*

* **PUT**
    * `PUT is used to send data to a server to create/update a resource.`
     >**The difference between POST and PUT is that PUT requests are idempotent. That is, calling the same PUT request multiple times will always produce the same result. In contrast, calling a POST request repeatedly have side effects of creating the same resource multiple times.**

* **PATCH**
    * The HTTP PATCH request method applies partial modifications to a resource.
    * Syntax : `PATCH /file.txt HTTP/1.1`


