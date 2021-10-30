# Spring Authentication

In applications there are some restrictions to have access to and interact with this is what we call application security:  

- Authentication like who are you.  
- Authorization or access control, What are you allowed to do.

### Authentication

the interface for authentication is `AuthenticationManager` and it has one method `authenticate()` and what this method does is to check whether the user is authenticated or not.  

An `AuthenticationProvider` is a bit like an `AuthenticationManager`, but it has an extra method `supports()`to see if it supports an authentication type.  
How this works, is that the providerManager can support multiple different authentication mechanisms by delegating to a chain of AuthenticationProviders, if it doesn't support an authentication instance it will be skipped or the providerManager has a parent which will consult if all the providers returns null, if the parent is not available an exception will be handled.  

### Customizing Authentication Managers  

we use `AuthenticationManagerBuilder` to authentication manager features set up in the application.   
if you want to build the global (parent) `AuthenticationManager`, the `AuthenticationManagerBuilder` will be `@Autowired` into a method in a `@Bean`, if you want to build a local `AuthenticationManager`, use `@Override` of a method in the configurer, and it will be child of the global one.  
>Spring Boot provides a default global AuthenticationManager (with only one user)  

### Authorization or Access Control  

the strategy in Authorization is `AccessDecisionManager` all the implementations delegate to a chain of `AccessDecisionVoter` instances.  

An `AccessDecisionVoter` considers an Authentication (representing a principal) and a secure Object, The `ConfigAttributes` is an interface and it has one method that returns a string where you can configure the level of access and the name of the user roles and determine what can be accessed.  

### Web Security

Spring Security in the web tier is based on Servlet `Filters`.  
The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI, one servlet can handle a single request, but filters form a chain, so they are ordered.

**Why use Servlet Filters?**  
the authentication and authorization should be done before a request hits your @Controllers, you can put filters in front of servlets, which means you could think about writing a SecurityFilter and configure it to filter every incoming HTTP request before it hits your servlet.  

### Creating and Customizing Filter Chains  

add a @Bean of type WebSecurityConfigurerAdapter (or WebSecurityConfigurer) and decorate the class with @Order , This bean causes Spring Security to add a new filter chain  

### Request Matching for Dispatch and Authorization

A security filter chain has a request matcher, and to have more controlof authorization you can set additional matchers in the `HttpSecurity` configurer.  

### Combining Application Security Rules with Actuator Rules

if you add the Actuator to a secure application, you get an additional filter chain that applies only to the actuator endpoints, and to apply application security rules to the actuator endpoints, you can add a filter chain that is ordered earlier than the actuator one and that has a request matcher that includes all actuator endpoints.

### Method Security  

you might want to protect your business logic itself. your @Controllers, @Components, @Services or even @Repositories, this approach is called method security,  
`@EnableGlobalMethodSecurity(securedEnabled = true)`  
If Spring creates a @Bean of this type, the caller will go through security stop before the method is executed and check access is granted or denied 

### Working with Threads  

The basic building block is the SecurityContext, which may contain an Authentication (and when a user is logged in it is an Authentication that is explicitly authenticated). You can always access and manipulate the SecurityContext through static convenience methods in SecurityContextHolder, which, in turn, manipulate a ThreadLocal.  
>**Principal** : used to validate the authentication, so this can be a useful little trick to get a type-safe reference to your user data.  
