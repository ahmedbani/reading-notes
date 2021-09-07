# read 9 
# Functional Programming Concepts 

## What is functional programming?

> **Functions are fundamental to code organization; they exist in all higher order programming languages. Generally, functional programming means using functions to the best effect for creating clean and maintainable software. More specifically, functional programming is a set of approaches to coding, usually described as a programming paradigm.**

## What is a pure function and how do we know if something is a pure function?

> **The first fundamental concept we learn when we want to understand functional programming is pure functionsIt returns the same result if given the same arguments (it is also referred as deterministic) It does not cause any observable side effects


## What are the benefits of a pure function?

* They’re easier to reason about
* They’re easier to combine
* They’re easier to test
* They’re easier to debug
* They’re easier to parallelize

## What is immutability?

*When you need to change data, It will not be Changed !!*

**The best correct solve is `Create new object and pushed new data in it`.**

## what is Referential transparency?

- Basically, if a function consistently yields the same result for the same input, it is referentially transparent. pure functions + immutable data = referential transparency

# Modules and require()

[Node JS Tutorial for Beginners #6 - Modules and require](https://www.youtube.com/watch?v=xHLd36QoS4k)

## What is a module?

>packaging mechanism that enables you to package a Java application or Java API as a separate Java module

## What does the word ‘require’ do?

>**introduced a new module system in which a module-info.**

## How do we bring another module into the file the we are working in?

>`A requires module directive specifies that this module depends on another module — this relationship is called a module dependency. Each module must explicitly state its dependencies`

## What do we have to do to make a module available?

>Concept: Describe our module filename : Concept: Describe our module filepath : Code our module descriptor file: module-info. java : Add code to our module : Compile our module : Run our modul

## Things I want to know more about

