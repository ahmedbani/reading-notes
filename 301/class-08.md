# read 8
# API Design Best Practices

* ## What does REST stand for?

>Ans: Representational State Transfer.

* ## REST APIs are designed around a ____.

>Ans1: REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.

>Ans2: A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

* ## What is an identifer of a resource? Give an example.

>Ans: http:// is the protocol. It indicates which protocol the browser must use. Usually it is the HTTP protocol or its secured version, HTTPS. The Web requires one of these two, but browsers also know how to handle other protocols such as mailto: (to open a mail client) or ftp: to handle file transfer, so don't be surprised if you see such protocols.

* ## What are the most common HTTP verbs?

>Ans: GET, POST, PUT, PATCH, and DELETE.

* ## What should the URIs be based on?

>Ans: Nouns (the resource) and not verbs (the operations on the resource).

* ## Give an example of a good URI.

>Ans: https://adventure-works.com/orders

* ## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

>Ans: Expose a large number of small resources.

* ## What status code does a successful GET request return?

>Ans: Return a response message with the body containing the value

* ## What status code does an unsuccessful GET request return?

>Ans: If not valid, 400 Bad Request is returned. Order is processed. If the order is successful, a 201 Created is returned for the order

* ## What status code does a successful POST request return?

>Ans: This means the request was successful and the server created a new resource. ... This means the server successfully processed the request, but is not returning any content. Unlike a 204 response, this response requires that the requester reset the document view.


* ## What status code does a successful DELETE request return?

>Ans: Responses. If a DELETE method is successfully applied, there are several response status codes possible: A 202 ( Accepted ) status code if the action will likely succeed but has not yet been enacted. A 204 ( No Content ) status code if the action has been enacted and no further information is to be supplied.



## Things I want to know more about

