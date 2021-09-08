# read 10
# Understanding the JavaScript Call Stack

## What is a ‘call’?

> The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

## How many ‘calls’ can happen at once?

> one every time !

## What does LIFO mean?

>Last in First out.

## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.


    function firstFunction(){
        throw new Error('Stack Trace Error');
    }

    function secondFunction(){
        firstFunction();
    }

    function thirdFunction(){
        secondFunction();
    }

    thirdFunction();

## What causes a Stack Overflow?

> **A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.**

>Example:

    function callMyself(){
        callMyself();
    }


# JavaScript error messages

## Reference errors

> Called a variable will not defined.

## Syntax error

> Write a variable or reserved word by wrong way (add leter).

## Range error

> **The Range is equal 0**

## tyep error

>In statistical hypothesis testing

## Breakpoint

>can also be achieved by putting a debugger statement in your code in the line you want to break.

## Things I want to know more about

