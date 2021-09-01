# read 5 
#  Things I want to know more about React Docs - thinking in React


How would you break a mock into a component heirarchy?

**we draw boxes around every component so we split it into heirarchy of components like FilterableProductTable and searchbar and so on.**

What is the single responsibility principle and how does it apply to components?

**It is  a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.**


What does it mean to build a ‘static’ version of your application?

**It is data that changes over time and you will want to build components that reuse other components and pass data using props**

Once you have a static application, what do you need to add?

**We need to starting with FilterableProductTable or ProductRow**

What are the three questions you can ask to determine if something is state?


**1. Is it passed in from a parent via props? If so, it probably isn’t state.
2. Does it remain unchanged over time? If so, it probably isn’t state.
3. Can you compute it based on any other state or props in your component? If so, it isn’t state.**


How can you identify where state needs to live?

**The state lives in FilterableProductTable**

