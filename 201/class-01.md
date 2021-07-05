## HTML

* HTML describes the structuce of pages  
The HTML code is made up of characters that live inside angled brackets — these are called HTML elements. Elements are usually made up of two tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags.  
* these are the main html tags 
![htmlTags](https://stuyhsdesign.files.wordpress.com/2015/09/basic-structure.png)  
  
* `<head>`  
This contains information about the page
* `<title>`  
The contents of the `<title>` element are shown on the tab of the page  
* `<body>`  
Everything inside this element is shown inside the main browser window.  
* ATTRIBUTES  
Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.
`<p lang="en-us">Paragraph in English</p>`  
**EXTRA MARKUP**
![htmlEvo](https://image.slidesharecdn.com/perspectivesontheevolutionofhtml-131028135529-phpapp02/95/perspectives-on-the-evolution-of-html-3-638.jpg?cb=1382968603) 

* DOCTYPES tell browsers which version of HTML you are using.
* You can add comments to your code between the `<!-- and -->` markers.
* The id and class attributes allow you to identify particular elements.
* The `<div>` and `<span>` elements allow you to group block-level and inline elements together.
* `<iframes>` cut windows into your web pages through which other pages can be displayed.
* The `<meta>` tag allows you to supply all kinds of information about your web page.
* Escape characters are used to include special characters in your pages such as <, >, and ©.  

**HTML5 LAYOUT**  

* The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure.
* The new elements provide clearer code (compared with using multiple `<div>` elements).
* Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements.
* To make HTML5 elements work in Internet Explorer 8 (and older versions of IE), extra JavaScript is needed, which is available free from Google.  

**PROCESS AND DESIGN**  

* It's important to understand who your target audience is, why they would come to your site, what information they want to find and when they are likely to return.
* Site maps allow you to plan the structure of a site.
* Wireframes allow you to organize the information that
will need to go on each page.
* Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them.
* You can differentiate between pieces of information using size, color, and style.
* You can use grouping and similarity to help simplify the information you present.

## JAVASCRIPT  

What is a script and how do I create one?
* A script is a series of instructions that the computer can follow in order to achieve a goal.
* Each time the script runs, it might only use a subset of all the instructions.
* Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task prggrammatically.
* To approach writing a script, break down your goal into a series of tasks and then work out each step needed to complete that task (a flowchart can help).  

How do computers fit in the worldaround them ?  
* computers create models of the world using data
* the models use objects torepresent physical things. objects can have:  
properties that tell us about the object, methods that perform tasks using the properties of that object, events which are triggered when a user interacts with the computer.
* Programmers can write code to say whenthis event occurs. 
* web browsers use HTML markup to create model of the page. 
* to make the web pages interactive, you write code that uses the browser's model of the web page.

How do I write a script for a web page?  
* It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files (like HTML pages and CSS style sheets), but they have the . j s extension.
* The HTML `<script>` element is used in HTML pages to tell the browser to load the JavaScript file (rather like the `<link>` element can be used to load a CSS file).
* If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.