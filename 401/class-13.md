# Related Resources and Integration Testing  

## Working with Relationships in Spring Data REST  

### One-to-One Relationship

- The Data Model  
define two entity classes having a one to one relationship using `@OneToOne` annotation above the property that is from the other class and can have the optional @RestResource annotation to customize the association resource.  
be careful to have different names for each association resource, or you will encounter a JsonMappingException  
The association name is default to the property name.  

- The Repositories  
to expose these entities as resources you will have to create to repositories extending the CrudRepository interface.  

- Creating the Resources  
- Creating the Associations  
we can establish the relationship by using one of the association resources, by using the HTTP method PUT.  
add an address to the owner of the association, If successful, this returns status 204.  

### One-to-Many Relationship

A one-to-many relationship is defined using the @OneToMany and @ManyToOne annotations and can have the optional @RestResource annotation to customize the association resource.  

- The Data Model  
lets say we have a one to one relationship, to have a one to many we will add another entity class and have a property from the owner of the association with `@ManyToOne` and in the owner you have a property with `@OneToMany`.  

- The Repository  
create a new repository for the new entity that extends the CrudRepository  

- The Association Resources  
create an instance from the new class, In the response body, we can see the association endpoint has been created.to associate send a PUT request to the association resource that contains the URI of the owner resource. verify it by using GET method, The returned JSON object will contain data fromthe new entity.  
To remove an association, we can use the DELETE method on the association resource

### Many-to-Many Relationship  

A many-to-many relationship is defined using @ManyToMany annotation, to which we can add @RestResource.  

- The Data Model  
add the `@ManyToMany` to the properties of the classes

- The Repository  
create repositories extending the crud repository

- The Association Resources

### Testing the Endpoints With TestRestTemplate  

create a test class that injects a TestRestTemplate instance and defines the constants we will use:

- Testing the One-to-One Relationship  
create a `@Test` method that saves the two class objects by making POST requests to the collection resources.  
Then it saves the relationship with a PUT request to the association resource and verifies that it has been established with a GET request to the same resource  

- Testing the One-to-Many Relationship  
create a `@Test` method that saves a owner instance and two other class instances, sends a PUT request to each class object's /owner association resource, and verifies that the relationship has been saved

- Testing the Many-to-Many Relationship  

## Integration Testing in Spring 

there are dependencies that are required for running the integration tests, the latest junit-jupiter-engine, junit-jupiter-api, and Spring test dependencies. 

**how to configure and run the Spring enabled tests**

1. Enable Spring in Tests with JUnit 5  
 by adding the `@ExtendWith` annotation to the test classes and specifying the extension class to load. To run the Spring test, use SpringExtension.class.  
 and also `@ContextConfiguration` annotation to load the context configuration and bootstrap the context that our test will use.  
  also annotate the test with `@WebAppConfiguration`, which will load the web application context.  

2. The WebApplicationContext  
ObjectWebApplicationContext provides a web application configuration. It loads all the application beans and controllers into the context. to be able to wire the web application context right into the test

3. Mocking Web Context Beans  
MockMvc provides support for Spring MVC testing. It encapsulates all web application beans and makes them available for testing.  
 initialize the mockMvc object in the @BeforeEach annotated method so that we don't have to initialize it inside every test.

4. Verify Test Configuration  

### Writing Integration Tests  

1. Verify View Name  
to get the ResultActions. Using this result, we can have assertion expectations about the response, like its content, HTTP status, or header  
2. Verify Response Body  
verify that response HTTP status is Ok (200). This ensures that the request was successfully executed, and verify that response content matches with the argument  
3. Send GET Request With Path Variable  
in this case you will check wheather the status is ok and the content type is json, and the value to be correct  
4. Send GET Request With Query Parameters  
its similar to point 3.  
5. Send POST Request  
MockMvcRequestBuilders.post will send the POST request. We can set path variables and query parameters, whereas form data can be set only via the param() method, similar to query parameters. 