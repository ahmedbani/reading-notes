# CSS
**CSS**:(Cascading Style Sheets) allows you to create great-looking web pages, but how does it work under the hood? This article explains what CSS is, with a simple syntax example, and also covers some key terms about the language.

Why we use **CSS** ?  
- How the html element will look like 
- Coloring the website
- Control the positioning of the elements
- Font size, weight, type
- Add borders
- Responsiveness 
- Animate the website. 

How we write css?
- Inline style:
	`<p> style="color : red"></p>`. 
- Internal style:  
"single html page"
`<head>`. 
`<style>`. 
	`P{
	    color : red
	   }
	</style>`
	`</head>`. 

- External style :
Create new css file and link it into the html
	`<head>`
	`<link type = "text/css" href="name.css">`
`</head>`. 

### CSS selectors:
- Class selectors. 

 You can have a class property in the html element to style each section or part alone, 
You can have the same class name for more than an element to style them the same way
The <div> and the <section> are called block element, it means they are gonna take the whole block.

- ID selectors. 

 Id is unique
An id property inside an html element
Its to style an element alone based on its id
It starts with a # when you style it in css file.  
### CSS syntax:
CSS is a rule-based language — you define rules specifying groups of styles that should be applied to particular elements or groups of elements on your web page.

The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (<h1>).

We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.

Before the colon, we have the property, and after the colon, the value. CSS properties have different allowable values, depending on which property is being specified. In our example, we have the color property, which can take various color values. We also have the font-size property. This property can take various size units as a value.

