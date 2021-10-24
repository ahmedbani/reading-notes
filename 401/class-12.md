# Spring RESTful Routing & Static Files

## Spring RequestMapping  
**the annotation is used to map web requests to Spring Controller methods.**  

### @RequestMapping Basics

- @RequestMapping — by Path  

```java
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@ResponseBody
public String getFoosBySimplePath() {
    return "Get some Foos";
}
```  

- @RequestMapping — the HTTP Method  
•The HTTP method parameter has no default. So, if we don't specify a value, it's going to map to any HTTP request.

### RequestMapping and HTTP Headers

- @RequestMapping With the headers Attribute  
when request mapping you can even specify the header for the request in the annotation attributes, and also multiple headers not only one.  
`@RequestMapping(value = "/ex/foos", headers = { "key1=val1", "key2=val2" }, method = GET)`  
• in the curl syntax to seperate between the header key and a value usually we use a `:` but in spring the `=` is used.  

- @RequestMapping Consumes and Produces  
We can map a request based on its Accept header via the @RequestMapping headers attribute  
`@RequestMapping(value = "/ex/foos", method = GET, headers = "Accept=application/json")`  

```java
@RequestMapping(
  value = "/ex/foos", 
  method = RequestMethod.GET, 
  produces = "application/json"
)
```

•if you used the old type of mapping with the headers attribute it will be converted to the new procedures way  
procedures supports multiple values  

### RequestMapping With Path Variables
mapping URI can be bound to variables via the @PathVariable annotation.

- Single @PathVariable 
If the name of the method parameter matches the name of the path variable exactly, then this can be simplified by using `@PathVariable `with no value and if it doesnt you have to use a value.  

-  Multiple @PathVariable  

```java
@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```

- @PathVariable With Regex  

### RequestMapping With Request Parameters  

```java
@RequestMapping(value = "/ex/bars", method = GET)
@ResponseBody
public String getBarBySimplePathWithRequestParam(
  @RequestParam("id") long id) {
    return "Get a specific Bar with id=" + id;
}
```

extracting the value of the id parameter using the @RequestParam(“id”) annotation in the controller method signature.

To send a request with the id parameter, we'll use the parameter support in curl  

### RequestMapping Corner Cases

### New Request Mapping Shortcuts
- @GetMapping
- @PostMapping
- @PutMapping
- @DeleteMapping
- @PatchMapping

## Accessing Data with JPA  

### Define a Simple Entity
create a class and annotate it with `@Entity` , indicating that it is a JPA entity, you store objects, each annotated as a JPA entity.

### Create Simple Queries 
Spring Data JPA focuses on using JPA to store data in a relational database. Its most compelling feature is the ability to create repository implementations automatically, at runtime, from a repository interface.  

### Create an Application Class  
Spring Initializr creates a simple class for the application.  
Now you need to modify the simple class that the Initializr created for you. To get output to the console  

## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data

JpaRepository – which extends PagingAndSortingRepository and the CrudRepository.  
- CrudRepository provides CRUD functions
- PagingAndSortingRepository provides methods to do pagination and sort records
- JpaRepository provides JPA related methods such as flushing the persistence context and delete records in a batch
• the JpaRepository contains the full API of CrudRepository and PagingAndSortingRepository because the inheritance.

### CrudRepository  

CRUD functionality:  

- save(…) – save an Iterable of entities. so you can pass multiple objects to save them in a batch
- findOne(…) – get a single entity based on passed primary key value
- findAll() – get an Iterable of all available entities in database
- count() – return the count of total entities in a table
- delete(…) – delete an entity based on the passed object
- exists(…) – verify if an entity exists based on the passed primary key value

### PagingAndSortingRepository 

When using Pageable, we create a Pageable object with certain properties and we've to specify at least:

1. Page size
2. Current page number
3. Sorting

### JpaRepository  

JPA methods: 

- findAll() – get a List of all available entities in database
- findAll(…) – get a List of all available entities and sort them using the provided condition
- save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
- flush() – flush all pending task to the database
- saveAndFlush(…) – save the entity and flush changes immediately
- deleteInBatch(…) – delete an Iterable of entities. Here, we can pass multiple objects to delete them in a batch
