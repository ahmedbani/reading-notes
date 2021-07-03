# Functions
Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.  

![function](https://miro.medium.com/max/4000/1*fqcYje1plRJWcIggILyuow.png)
* ### Why we use functions ?
1. It helps us to solve problems effectively in a simpler way.
2. Reusability. 
3. It improves modularity.
4. It reduces complex problems into simple pieces.
5. It improves the productivity of the developer.
6. It helps us to debug the code quickly.  

### There are two ways for creating a function:
1. Function declaration:
- The name of the function.
- A list of parameters to the function, enclosed in parentheses and separated by commas.
- The JavaScript statements that define the function, enclosed in curly brackets, {...}.  
function name(){
  code...  
  return ;  
}
2. Function expression:  
While the function declaration above is syntactically a statement, functions can also be created by a function expression.  
Such a function can be anonymous, However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function.  
var name = function(){
  code...  
  return ;  
}

* to invoke/call the function you just type its name.  
functioName();