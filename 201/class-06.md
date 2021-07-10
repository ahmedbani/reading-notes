# class 6

## The problem domain

what is the hardest thing in programming ?  
There are many common answers to this question:  

- Learning a new technology
- Naming things
- Testing your code
- Debugging
- Fixing bugs
- Making software maintainable  

The list goes on and on.  

### Understanding The Problem Domain Is The Hardest Part Of Programming  
**Why problem domains are hard**   

```Have you ever tried to put together a jigsaw puzzle that didn’t have any picture on it?  How about one like this one, that has a very similar pattern repeated on it and is double-sided?

hard puzzle problem domain

The reason why puzzles like this one are so hard, is because you can’t really see what you are trying to build very clearly.  Normally when you put together a jigsaw puzzle you follow steps that might look something like this:


1. Figure out what the major components of the picture are
2. Sort the pieces by color or component
3. Put together all the border pieces
4. Put together each component of the picture from the piles you created
This all breaks down when you don’t have a picture with clear components that you can identify.

The same thing happens when writing code.  Writing code is a lot like putting together a jigsaw puzzle.  We put together code with the purpose of building components that we have taken out of the “bigger picture” of the problem domain.
```

**Programming is easy if you understand the problem domain**.  

### What can you do about it?
If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:  

1. Make the problem domain easier: You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.  

2. Get better at understanding the problem domain:
As developers, we tend to think that sitting down and talking to customers or business people who know about the problem domain is a waste of time. It is easy to fall into the trap of thinking you understand enough of the problem to get started coding it.
  
## object literals 
What is an object?  
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world.  
IN AN OBJECT:
- VARIABLES BECOME KNOWN AS PROPERTIES.  
- FUNCTIONS BECOME KNOWN AS METHODS.  
creating an object: literal notation  
EX:  
```js
var hotel ={
    name= 'Quay';
    rooms= 40;
    booked= 25;
    checkAvailabilty : function(){
        return this.rooms - this.booked
    }
};
```
- the object is the curly braces and their content
- name,rooms,booked : are the properties of the object. 
- the checkAvailabilty: is the method.  

you can access an object like :
```js
var hotel= hotel.name;
var freeRooms = hotel.checkAvailabilty();
```

## Document object model (DOM)  
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

THE DOM TREE IS A MODEL OF A WEB PAGE
As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory. It consists of four main types of nodes. 
1. THE DOCUMENT NODE
2. ELEMENT NODES
3. ATTRIBUTE NODES
4. TEXT NODES
Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in the browser.  

Accessing and updating the DOM tree involves two steps:
1. Locate the node that represents the element you want to work with.  
2. Use its text content, child elements, and attributes.  

**accessing elements**  
DOM queries may return one element, or they may return a Nodelist, which is a collection of nodes.  
```js
METHODS THAT RETURN A SINGLE ELEMENT NODE 
getElementByld('id')
querySelector('css selector')
METHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST):
getElementByClassName('class')
getElementsByTagName('tagName')
querySelectorAll ('css selector')
```
LOOPING THROUGH A NODELIST
```js
var hotltems =document.querySelectorAll('li.hot'); II Store Nodelist in array
if (hotltems.length > O) { 
for (var i=O; i<hotltems.length; i++) { 
hotltems[i].className = 'cool';
}
}
```
TRAVERSING THE DOM  
When you have an element node, you can select another element in relation to it using these five properties. This is known as traversing the DOM.
1. parentNode
2. previousSibling
3. nextSibling
4. firstChild
5. lastChild
  
- The browser represents the page using a DOM tree. 
- DOM trees have four types of nodes: document nodes,element nodes, attribute nodes, and text nodes. 
- You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax. 
- Whenever a DOM query can return more than one node, it will always return a Nadeli st.
- From an element node, you can access and update its content using properties such as textContent and innerHTML or using DOM manipulation techniques.
- An element node can contain multiple text nodes and child elements that are siblings of each other.
- In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).
- Browsers offer tools for viewing the DOM tree.