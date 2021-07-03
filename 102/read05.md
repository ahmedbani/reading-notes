## Logicaloperators
Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table. 

| operator      | usage        | description |
| :---          |    :----:    | ---:        |
| logical and (&&) | x && y    |returns true if both of the variables are true otherwise its false |
| logical or (`||`) | x `||` y | returns false if both of the variables are false |
| not (!) | ! x | returns the inverse of the boolean value |
here is the truth table for the operators :
![table](https://3.bp.blogspot.com/-mnDeONCDxuo/Th63hE_gYsI/AAAAAAAAAEc/nk7-dEtDO-o/s1600/and+or+not+truth+table.gif)
## Loops
Loops offer a quick and easy way to do something repeatedly, There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times.  

-  **for loop**:
for ([initialExpression]; [conditionExpression]; [incrementExpression]){
  statement}. 
  
1. The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
2. The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)
3. The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.
4. If present, the update expression incrementExpression is executed.
5. Control returns to Step 2.
- **while loop**: 

while (condition){
  statement}. 

If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.