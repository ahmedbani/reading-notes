# Read: 03 - Maps, primitives, File I/O

## Pirmitives Vs Objects

Primitive is a basic data Type like:
* boolean
* byte
* short, long
* int
* float, double
* char 

object is a basic data type like:

* Boolean
* Integer
* Byte
* Short, Long
* Char
* Double
* Float

>and the defaults is **Null**.

## File

### File path have three parts:

- Folder Path
- File Name
- Extension

### File systems are composed of three main parts:

- Header: metadata about the contents of the file (file name, size, type)
- Data: contents of the file as written by the creator or editor
- End of file (EOF): special character that indicates the end of the file

>**Exception :** An exception is an event, which occurs during the execution of a program that disrupts the normal flow of the program's instructions.

**The Catch or Specify Requirement :**  

- A try statement that catches the exception. The try must provide a handler for the exception
- A method that specifies that it can throw the exception. The method must provide a throws clause that lists the exception

### The Three Kinds of Exceptions
1. The first kind of exception is the checked exception.
2. The second kind of exception is the error.
3. The third kind of exception is the runtime exception.

**How to Throw Exceptions**  
the Java platform provides numerous exception classes. All the classes are descendants of the Throwable class, and all allow programs to differentiate among the various types of exceptions that can occur during the execution of a program.  
You can also create your own exception classes to represent problems that can occur within the classes you write.  
All methods use the throw statement to throw an exception. The throw statement requires a single argument: a throwable object. Throwable objects are instances of any subclass of the Throwable class. Here's an example of a throw statement.

`throw someThrowableObject;`

>**Assertion :** An assertion is a sanity-check that you can turn on or turn off when you are done with your testing of the program.

### Scanning

Objects of type `Scanner` are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.  
a scanner uses white space to separate tokens. (White space characters include blanks, tabs, and line terminators. For the full list, refer to the documentation for `Character.isWhitespace`.)