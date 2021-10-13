# Linked List

Declare: Is a part of the collection framework present in `java.util` 

    Statment in Java
    LinkedList<String> linkedList  = new LinkedList<String>();

**Get an Example:**

    
    import java.util.*;
    public class Test {
        public static void main(String args[])
        {
            LinkedList<String> ll = new LinkedList<String>();
            ll.add("A");
            ll.add("B");
            ll.addLast("C");
            ll.addFirst("D");
            ll.add(2, "E");
            System.out.println(ll);
            ll.remove("B");
            ll.remove(3);
            ll.removeFirst();
            ll.removeLast();
    
            System.out.println(ll);
        }
    }
    /*OutPut: 
    [D, A, E, B, C]
    [A]*/

>In the last example you are shown how i can used the remove and add item to the linked list.

## When To Use
* It is best to use an ArrayList when:

    * You want to access random items frequently
    * You only need to add or remove elements at the end of the list

* It is best to use a LinkedList when:

    * You only use the list by looping through it instead of accessing random items
    * You frequently need to add and remove items from the beginning, middle or end of the list

**Other Method : `getFirst(ll);` used to return the first value of linked list**

>The starting point of the list is a reference to the first node, which is referred to as the head. Nearly all linked lists must have a head, because this is effectively the only entry point to the list and all of its elements, and without it, you wouldn’t know where to start! The end of the list isn’t a node, but rather a node that points to null, or an empty value.  

## Big O: Analysis of Algorithm Efficiency  
Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:  
1. Running Time
2. Memory Space  

**Big O’s** role is to describe the Worst Case of efficiency an algorithm can have in performing it’s job, and there is 4 Key Areas for analysis:  
1. Input Size
2. Units of Measurement
3. Orders of Growth
4. Best Case, Worst Case, and Average Case  

### Input size  
Input Size refers to the size of the parameter values that are read by the algorithm. This does not simply refer to the number of parameters an algorithm reads, but takes into account the size of each parameter value as well.  
We will use the letter n to refer to the Input Size value.

The higher this number, the more likely there will be an increase to Running Time and Memory Space.  

### Orders of Growth
![Orders of Growth](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/OrdersOfGrowth.png)  

**Constant Complexity:** means that no matter what inputs are thrown at our algorithm, it always uses the same amount of time or space.  

**Logarithmic Complexity:** represents a function that sees a decrease in the rate of complexity growth, the greater our value of n.  

**Linear Complexity:** the size of our inputs ‘n’ will directly determine the amount of Memory Space used and Running Time length. This is a very common efficiency and is usually used to denote functions with loops, or often algorithms that use recursion.  
