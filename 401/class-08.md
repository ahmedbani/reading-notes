# OO Design

## Don't repeat yourself (DRY)

is a principle of software development that aims to avoid or reduce repition of software patterns, replacing it with abstractions to avoid redundancy 

when **DRY** is applied you will have a non redundant code more readable and easier to modify and update.  
**How to apply DRY?**  
use abstraction for examle:  
if I change a piece of code in one place, it should apply the changes to every instance of that code .

### WET 

stands for **write everything twice** or write every time , WET solutions are common used in multi-tiered architectures

### AHA

stand for **Avoid Hasty Abstractions** , is another principle for abstraction .
optimizing for change first, and avoiding early optimization .  
AHA programming assumes that both WET and DRY solutions inevitably create software that is rigid and difficult to maintain, dont rush into abstraction and reducing redundant code software will be more flexible when you use abstraction whent its needed.

## Rule of three (computer programming)
"three strikes then refactor" it a rule to decide when to refactor your code , it states that when similar code is repeated 2 times there is no need to refactor but on the the third time you refactor.  
The rule implies that the cost of maintenance certainly outweighs the cost of refactoring and potential bad design when there are three copies. 

## YAGNI 

"You Aren't Gonna Need It" is a principle that states that a programmer should not a functionality until its need cause other wise you wont need it .  
XP co-founder Ron Jeffries has written: 
>"Always implement things when you actually need them, never when you just foresee that you need them." 

## Minimum viable product (MVP)

**MVP**: is a version of product with enough functionality and features to be usable to get feedback, its like a beta or an early version.  

### why you should focus on releasing MVP?  

by that you can avoid lengthy and unnecessary work and start working on versions listen to feedback and apply them , challenging and validating assumptions about a product's requirements, and test if this buisness idea would be viable and profitable by testing it like this, it can be used to test the market need for a product or development of an existing product or the need for a service and so on.  
