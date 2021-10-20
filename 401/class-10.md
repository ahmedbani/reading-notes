# Stack and Queue

## What's Stack?

>**It follows a particular order for adding or removing elements. Linear data structures organize their components in a straight line, so if we we add or remove an element, they will grow or shrink respectively.**

* push 
* pop
* top

## What's Queue?

>**A Queue is also a linear structure that follows a First In First Out (FIFO) order, but they differ in how elements are removed.**

* end
* enqueue
* dequeue
* front

## How to implement a Stack in Java

    Stack<Integer> myStack = new Stack<>();
    myStack.push(5);
    myStack.push(6);
    myStack.push(7);

## How to implement a Queue in Java

    Queue<String> str_queue = new LinkedList<> ();
    str_queue.add(“one”);
    str_queue.add(“two”);
    str_queue.add(“three”);

Side                            | Queue                         | Stack
------------------------------- | ----------------------------- | -----------------------------
Pros                            | It is easy to implement and logical for beginners | Queues are flexible.
Pros                            | It allows you to control how memory is allocated | They can handle multiple data types.
Pros                            | Easier to use than queues     | Data queues are fast and optimized
Cons                            | Neither flexible nor scalable | Inserting/ removing elements from the middle is complex.
Cons                            | Random access to elements in a stack is nearly impossible | Queues are not readily searchable

