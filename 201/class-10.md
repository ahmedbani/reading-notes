# class 10

## Error Handling & Debugging
 JavaScript can be hard to learn and everyone makes mistakes when writing it. When you are writing JavaScript, do not expect to write it perfectly the first time. Programming is like problem solving: you are given a puzzle and not only do you have to solve it, but you also need to create the instructions that allow the computer to solve it. too.
When writing a long script, nobody gets everything right in their first attempt. The error messages that a browser gives look cryptic at first, but they can help you determine what went wrong in your JavaScript and how to fix it.   
**EXECUTION CONTEXTS**  
The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope.  
**The stack**  
the javaScript inetrpreter processes one line of code at a time, when a statement needs data from another function, it stacks the new function on the top of the current task.  
```js
function greetUser () {
return 'He11o ' + getName();
}
function getName() { 
 var name= 'Molly ' ; return name;
}
 var greeting= greetUser(); e al ert(greeting);

```  
**EXECUTION CONTEXT & HOISTING**  

Each time a script enters a new execution context, there are two phases of activity:  
1. PREPARE: 
- The new scope is created
- Variables, functions, and arguments are created
- The value of the this keyword is determined  
2. EXECUTE:  
- Now it can assign values to variables
- Reference functions and run their code 
- Execute statements  

In the interpreter, each execution context has its own vari ables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's vari ables object.  
If a JavaScript statement generates an error, then it throws an exception . At that point, the interpreter stops and looks for exception-handling code.  
**ERROR OBJECTS**  
 Error objects can help you find where your mistakes are and browsers have tools to help you read them.  
- SyntaxError: SYNTAX IS NOT CORRECT 
- ReferenceError: VARIABLE DOES NOT EXIST
- EvalError: INCORRECT USE OF eval() FUNCTION
- URIError: INCORRECT USE OF URI FUNCTIONS
- Type Error: VALUE IS UNEXPECTED DATA TYPE
- RangeError: NUMBER OUTSIDE OF RANGE
- Error: GENERIC ERROR OBJECT
- NaN: NOT A NUMBER  

 HOW TO DEAL WITH ERRORS?
1. DEBUG THE SCRIPT TO FIX ERRORS
2. HANDLE ERRORS GRACEFULLY  


Debugging is about deduction: eliminating potential causes of an error. Try to narrow down where the problem might be, then look for clues.  
you can look at the errors throw the browser.  

• you can log data to the console through console.log(the data). There are more console methods like :  
1. `conso1e.info()` canbeused for general information
2. `console.warn()` can be used for warnings 
3. `console.error()` canbeused to hold errors  

• You can pause the execution of a script on any line using breakpoints. Then you can check the values stored in variables at that point in time.  
If you set multiple breakpoints, you can step through them one-by-one to see where values change and a problem might occur. You can indicate that a breakpoint should be triggered only if a condition that you specify is met. The condition can use existing variables.  
**HANDLING EXCEPTIONS**  
If you know your code might fail, use try, catch, and finally. Each one is given its own code block.  
```js

try {
// Try to execute this code
}catch (exception) {
// If there is an exception, run this code 
}finally {
// This always gets executed
}
```  
- If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code.
- Debugging is the process of finding errors. It involves a process of deduction.
- The console helps narrow down the area in which the error is located, so you can try to find the exact error.
- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.
- If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.