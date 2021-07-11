# class 7
## Domain modeling
Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.  

### Define a constructor and initialize properties  
To define the same properties between many objects, you'll want to use a constructor function.  

```js
let functionName = function(x, y) {
  this.x = x;
  this.y = y;
}
// creating new objects
let instance1 = new functionName(7, false);
let instance2 = new functionName(4, true);

console.log(instance1);
console.log(instance2);
```  
As you can see, the constructor function is defined using a function expression. When the function is called, the data inside these parameters are stored inside the  this.x  and this.y properties respectively. Storing data within properties ensures any newly created object can access that data later.  
After the constructor function definition, two objects are instantiated with the new keyword and their properties are initialized by calling the constructor function.  
This is object-oriented programming in JavaScript at its most fundamental level.

1. The new keyword instantiates (i.e. creates) an object.
2. The constructor function initializes properties inside that object using the this variable.
3. The object is stored in a variable for later use.  

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.  

## Tables
There are several types of information that need to be displayed in a grid or table. When representing information in a table, you need to think in terms of a grid made up of rows and columns.  
**What's a Table?**  

A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.  

Table structure:  
- The `<table>` element is used to create a table. The contents of the table are written out row by row.
- You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.)
It is followed by one or more `<td>` elements (one for each cell in that row).
At the end of the row you use a closing `</tr>` tag.
- Each cell of a table is represented using a `<td>` element. (The td stands for table data.)
At the end of each cell you use a closing `</td>` tag.
- The `<th>` element is used just like the `<td>` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.)  

**Spanning columns & rows**  

- Sometimes you may need the entries in a table to stretch across more than one column. The colspan attribute can be used on a `<th>` or `<td>` element and indicates how many columns that cell should run across.  
- You may also need entries in a table to stretch down across more than one row. The rowspan attribute can be used on a `<th>` or `<td>` element to indicate how many rows a cell should span down the table.

**long Tables**  

There are three elements that help distinguish between the main content of the table and the first and last rows (which can contain different content).
- The headings of the table should sit inside the `<thead>` element.
- The body should sit inside the `<tbody>` element.
- The footer belongs inside the `<tfoot>` element.  

## Objects
creating an object using the new keyword from the constructor as before,
- the new keyword and the object constructor create a blank object.  
- you can update the properties using the dot notation. 
- sometimes you want several objects to represent similar things using the object constructor.
- add and remove properties 

**this**  
The keyword this is commonly used inside functions and objects. Where the function is declared alters what this means. It always refers to one object, usually the object in which the function operates.  

### arrays
arrays are actually a special type of objects, they hold a related set of key/value pairs, but the key for each value is its index number. 
you can combine arrays and objects , arrays can store a series of objects and objects can also hold arrays.  
WHAT ARE BUILT-IN OBJECTS?  
Browsers come with a set of built-in objects that represent things like the browser window and the current web page shown in that window. These built-in objects act like a toolkit for creating interactive web pages.  
There are three groups of built in objects :
1. BROWSER OBJECT MODEL:
The Browser Object Model contains objects that represent the current browser window or tab. It contains objects that model things like browser history and the device's screen.
2. DOCUMENT OBJECT MODEL:  
The Document Object Model uses objects to create a representation of the current page. It creates a new object for each element (and each individual section of text) within the page.
3. GLOBAL JAVASCRIPT OBJECTS:  
The global JavaScript objects represent things that the JavaScript language needs to create a model of. For example, there is an object that deals only with dates and times.  

- Functions allow you to group a set of related statements together that represent a single task.
- Functions can take parameters (informatiorJ required to do their job) and may return a value.
- An object is a series of variables and functions that represent something from the world around you.
- In an object, variables are known as properties of the object; functions are known as methods of the object.
- Web browsers implement objects that represent both the browser window and the document loaded into the browser window.
- JavaScript also has several built-in objects such as String, Number, Math, and Date. Their properties and methods offer functionality that help you write scripts.
- Arrays and objects can be used to create complex data sets (and both can contain the other).
