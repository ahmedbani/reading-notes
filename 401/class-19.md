# Spring and Sockets


## **Real time messaging with websockets:**

### What is websockets?
*WebSocket* is a thin, lightweight layer above TCP. This makes it suitable for using “subprotocols” to embed messages. In this guide, we use STOMP messaging with Spring to create an interactive web application. STOMP is a subprotocol operating on top of the lower-level WebSocket.

### How to use websockets with spring boot?
1. Starting with Spring Initializr.
2. Adding Dependencies.
3. Create a Resource Representation Class. *The service will accept messages that contain a name in a STOMP message whose body is a JSON object.*
4. Create a Message-handling Controller.

*In Spring’s approach to working with STOMP messaging, STOMP messages can be routed to @Controller classes. For example, the GreetingController (from src/main/java/com/example/messagingstompwebsocket/GreetingController.java) is mapped to handle messages to the /hello destination, as the following listing shows:*

5. Make the Application Executable.

    @SpringBootApplication is a convenience annotation that adds all of the following:
   + @Configuration: Tags the class as a source of beandefinitions for the application context.

   + @EnableAutoConfiguration: Tells Spring Boot to start addingbeans based on classpath settings, other beans, and variousproperty settings. For example, if spring-webmvc is on theclasspath, this annotation flags the application as a webapplication and activates key behaviors, such as setting up aDispatcherServlet.

   + @ComponentScan: Tells Spring to look for other components,configurations, and services in the com/example package,letting it find the controllers.


**resources:** 

*[https://spring.io/guides/gs/messaging-stomp-websocket/](https://spring.io/guides/gs/messaging-stomp-websocket/)*

