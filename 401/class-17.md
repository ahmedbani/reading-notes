
# Spring Boot and OAuth2:
The samples are all single-page apps using Spring Boot and Spring Security on the back end. They also all use plain jQuery on the front end. But, the changes needed to convert to a different JavaScript framework or to use server-side rendering would be minimal.

All samples are implemented using the native OAuth 2.0 support in Spring Boot.

There are several samples building on each other, adding new features at each step:

+ simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

+ click: adds an explicit link that the user has to click to login.

+ logout: adds a logout link as well for authenticated users.

+ two-providers: adds a second login provider so the user can choose on the home page which one to use.

+ custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

### **Single Sign On With GitHub**
1. Creating a New Project.
2. Add a Home Page: In your new project, create index.html in the src/main/resources/static folder.
3. Securing the Application with GitHub and Spring Security.

4. Add a New GitHub App.
5. Configure.
6. Boot Up the Application.



**resources:** 

*https://spring.io/guides/tutorials/spring-boot-oauth2/*