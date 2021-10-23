# Spring

**Spring FrameWork:** *is an open source application framework that provides infrastructure support for developing Java applications, it's the one of the most popular Java Enterprise Edition (Java EE) frameworks.*

## Serving Web Content with Spring MVC 

• creating a website using Spring:  

### Starting with Spring Initializr
You can use this [pre-initialized project](https://start.spring.io) and click Generate to download a ZIP file.

### Create a Web Controller  
HTTP requests are handled by a controller. to identify the controller by the `@Controller` annotation.  
The `@GetMapping` annotation ensures that HTTP GET requests to `/path` are mapped to the method.

The implementation of the method body relies Thymeleaf to perform server-side rendering of the HTML. Thymeleaf parses the template and evaluates the th:text expression to render the value of the parameter that was set in the controller.

•**Make sure you have Thymeleaf on your classpath**  

### Spring Boot Devtools
Spring Boot offers with a module known as spring-boot-devtools, To speed up this refresh cycle, Spring Boot Devtools:

- Enables hot swapping.

- Switches template engines to disable caching.

- Enables LiveReload to automatically refresh the browser.

- Other reasonable defaults based on development instead of production.  

### Run the Application
The Spring Initializr creates an application class for you.  
```java
package com.example.servingwebcontent;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class ServingWebContentApplication {

    public static void main(String[] args) {
        SpringApplication.run(ServingWebContentApplication.class, args);
    }

}
```

The `main()` method uses Spring Boot’s `SpringApplication.run()` method to launch an application. this web application has no XML lines or file its 100% pure java.  
• You can run the application from the command line with Gradle or Maven.

**Thymeleaf:** is a modern server-side Java template engine for both web and standalone environments.

**Thymeleaf's main goal**  
is to bring elegant natural templates to your development workflow — HTML that can be correctly displayed in browsers and also work as static prototypes, allowing for stronger collaboration in development teams.

### Spring MVC and Thymeleaf: how to access data from templates

in a Spring MVC application, `Controller` classes are responsible for preparing a model map with data and selecting a view to be rendered. This model map allows for abstraction of the view technology and Thymeleaf, it is transformed into a Thymeleaf context object, that makes all the defined variables available to expressions executed in templates. 

### Spring model attributes  
Spring MVC calls the pieces of data to a view "model attributes".in Thymeleaf language is "context variables".  
There are several ways of adding model attributes to a view in Spring MVC: 

- Add attribute to `Model` via its `addAttribute` method.  
- Return `ModelAndView` with model attributes included.
- Expose common attributes via methods annotated with `@ModelAttribute`.

• in all these cases the `message` will be added to the model an it will be in the Thymeleaf views.  
to access theses context variables -> `${attributeName}` which is the messages  
``` html
 <tr th:each="message : ${messages}">
            <td th:text="${message.id}">1</td>
            <td><a href="#" th:text="${message.title}">Title ...</a></td>
            <td th:text="${message.text}">Text ...</td>
        </tr>
```

### Request parameters  
Request parameters are passed from the client to server like:  
`https://example.com/query?q=Thymeleaf+Is+Great!`   
In order to access the q parameter you can use the `param.` prefix:  
`<p th:text="${param.q}">Test</p>`  
Since parameters can be multivalued you may access them using brackets.  
• Another way to access request parameters is by using the special `#request` object that gives you direct access to the `javax.servlet.http.HttpServletRequest` object:

`<p th:text="${#request.getParameter('q')}" th:unless="${#request.getParameter('q') == null}">Test</p>`

### Session attributes  
• When developing web applications, we often need to refer to the same attributes in several views which are the session attributes.  
Similarly to the request parameters, session attributes can be accessed by using the `session.` prefix, 
Or by using `#session`, that gives you direct access to the `javax.servlet.http.HttpSession` object. 

### ServletContext attributes
• when objects are associated with a ServletContext object, they are called context attributes and are available to the whole application, and all the Servlets in the application can access these attributes through the ServletContext object.

The ServletContext attributes are shared between requests and sessions. In order to access ServletContext attributes in Thymeleaf you can use the `#servletContext.` prefix

### Spring beans 
Thymeleaf allows accessing beans registered at the Spring Application Context with the `@beanName` syntax, for example:

`<div th:text="${@urlService.getApplicationUrl()}">...</div>`.  


