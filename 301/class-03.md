# read 3
# Passing Functions as Props

## React Docs - lists and keys

*When working on React apps, you will encounter use cases where you have to deal with arrays. These cases could involve data from an external API, responses from your backend services, or, most commonly, rendering a list of data items in your component.*

>`map()` function lets you manipulate the items in an array by iterating and accessing individual items. In this guide, you will learn how to use the `map()` function and exporting. 

**If I want to loop through an array and display each value in JSX, how do I do that in React?** 
`array.map(function(currentValue, index, arr), thisValue)` and all items need a key `unique` to can know's what the item will be changed (`add`, `delete` and others), by key i can returned the value what i actually needed.

## The Spread Operator

**The `spread operator` is a new addition to the set of `operators` in JavaScript `ES6`. It takes in an iterable (e.g an array) and expands it into individual elements. `The spread operator` is commonly used to make shallow copies of JS objects. Using this `operator` makes the code concise and enhances its readability.**

>**If you want to merge between 2 arrays we are used Spread bt three dots(`***`)**

**spread operator is useful for many different routine tasks in JavaScript, including the following:**
>* Copy an array.
>* Using math functions like pow().
>* Add item to list like
>* Add state in React.

>Example

    const arr1 = ["Ali" , "Khaled" , "Aown"];
    const arr2 = ["Saja" , "Hadeel" , "Aya"];
    const arr3 = [...arr1 , ...arr2];
    //The value of arr3 = ["Ali" , "Khaled" , "Aown" , "Saja" , "Hadeel" , "Aya"];


>If i need to added new name I'll be using push like:
    
    arr3.push("Abed AlRahman");

>To mearge Objects !

    const person = { name: 'Ali', gender: 'Male' };
    const tools = { computer: 'HP', editor: 'Akef' };
    const summary = {...person, ...tools};
    /*
    Summary Object {
    "computer": "HP",
    "editor": "Akef",
    "gender": "Male",
    "name": "Ali",
    }
    */

## How to Pass Functions Between Components

In the video, what is the first step that the developer does to pass fucntions between components?

`Using map`

In your own words, what does the increment function do?

`Go to next Nodes.`

How can you pass a method from a parent component into a child component?

`import Child from './Child'`

How does the child component invoke a method that was passed to it from a parent component?



## Things I want to know more about

