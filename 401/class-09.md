# WRRC and Java

## The HTTP Request Lifecycle

### Step 1: Local Processing: 

1. The browser extracts the "scheme"/protocol, host, and optional port number, resource path, and query strings that are specified in the form  
`<protocol>://<host><:optional port>/<path/to/resource><?query>`. 

example:  
`|http|://|www.funter.com||:3010||/homepage||?query=param&query2=param2|`.

2. Now the browser has the hostname for the request, it needs to resolve an IP address  
**IP address:**  Internet Protocol Address is a numeric identifier for a computer, server, or other resource connected to a TCP/IP (Transmission Control Protocol) network.  
The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.

### Step 2: Resolve an IP

resolving an IP from a "DNS server", This is a server that serves a collection of hostnames and their correlated IPs. 

1. If the cache lookup fails (we will assume it does), your browser fires off a DNS request using UDP. The DNS request contains the preconfigured IP for your DNS server and your return IP in its header. The hostname for which you are trying to resolve an IP is in the request’s "Question" section.  
 **UDP** is a lightweight protocol that optimizes for speed, with the tradeoff being that it offers no guarantees in terms of delivery or order.  
 
 2. the request will now have to travel many network devices to reach its target DNS server. Whenever the packet hits a piece of networking equipment, the device uses a routing table to determine which other device it is connected to that is most likely situated along the shortest path to the destination.  

 3. Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname. If it finds one, it sends a response. If, on the other hand, the DNS server you have targeted cannot locate the given hostname, it passes the request along to another DNS server it is configured to defer to. this will keep hapening until the address is found  

 ### Step 3: Establish a TCP Connection  

 since the request is sent over TCP the client must open a connection, TCP connections are opened using what’s known as a three-way handshake.

 1. The client initiates the active open by sending a `SYN`(Synchronize) "control" packet to the server. the sequence number is set for the first packet randomly for security purposes `x`

 2. The server responds with a `SYN-ACK`(Synchronize Acknowledgment) and contains an acknowledgement number which is always `x+1`

 3. he client sends an `ACK` message back to the server with a `x+1`, which should match the `SYN-ACK`

### Step 4: Send an HTTP Request  

now that the client has an IP address and a TCP connection, it can finally send an HTTP request.  

1. The request is made up of a "request line", request header, and a body. 
   - **request line**: a line that indicates the HTTP method, the resource being requested, and the protocol version.
   - **header**: is made up of pairs in the form name:value `<CR><LF>`. Two consecutive `<CR><LF>` pairs indicate the end of the header section. 
   - **body**: The body content of an HTTP request is completely optional, but often contains something like form data or JSON. 

2. Once the HTTP request is sent, it follows a similar routing procedure

3. Once the server receives the request, processes it, and finds the resource being requested, it generates an HTTP response. containing a "status line", response header fields, and an optional body.
   - **status line**: contains an HTTP status code indicating the success, failure, or error-state of the request along with a "reason message" that provides detail.

4. Once the response is generated, the server responds to the request. At the TCP layer.

### Step 5: Tearing Down and Cleaning Up  

The client sends a `FIN` packet at the TCP level, the server responds with an `ACK`, and then generally sends a `FIN` of its own, which the client responds to with its own `ACK` signal. The client then waits for a brief timeout, during which it cannot accept new connections, to prevent delayed packets from previous connections arriving during subsequent activities on the port.  

## Java HTTP Request example

[HTTP Request example](https://www.baeldung.com/java-http-request)
