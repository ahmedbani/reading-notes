# Read: 02 - Arrays, Loops, Imports

## **Packages and Import**

* Package = directory. Java classes can be grouped together in packages
* A package name is the same as the directory (folder) name which contains the

### Package declaration

>Following the optional package declaration, you can have import statements

>Default package. Altho all Java classes are in a directory, it's possible to omit the package declaration. For small programs it's common to omit it, in which case Java creates what it calls a default package. 

**The statement order is as follows. Comments can go anywhere.**

* Package statment (optional).
* Imports (optional).
* Class or interface definitions.


## **Import**

* import `javax.swing.*;` when write * all classes that located in swing available to use in another program.
* import `javax.swing.JOptionPane;` just JOptionPane method available in my program.
* `javax.swing.JOptionPane.showMessageDialog(null, "Hi");` write packages name and the method in my code.

### Common imports


* import `java.awt.*;`	Common GUI elements.
* import `java.awt.event.*;`	The most common GUI event listeners.
* import `javax.swing.*;`	More common GUI elements. Note "javax".
* import `java.util.*;`	Data structures (Collections), time, Scanner, etc classes.
* import `java.io.*;`	Input-output classes.
* import `java.text.*;`	Some formatting classes.
* `import java.util.regex.*;`	Regular expression classes.

# Array

**Using array to stored data in the one variable like `int []arr= {'1','2','3'};` of string or numbered and can fixed and compared to returned the result like which value of these array is long length or odd even capital letter or small letter.**

# Loops

## Type
* While loop => Have a condition, if condition is true login in the while if not don't join the loops. 
* for loop using almost to search in the array value or to entered value many time. 
* Do-while => using to do something before see the condition is true or false.