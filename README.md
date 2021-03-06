# introToReact
Introduction to the React Library
React is a declarative and component-based JavaScript library.

Declarative means that React updates the application interface when data changes. As an example of this declarative functionality, it is utilized when a user logs into their account and their name displays elsewhere on the screen.

Component-based design is the concept of writing small bits of functionality that are reusable throughout an application. For example, a log-in form could be a component that is displayed in multiple places or situations. Component-based design improves the development and maintenance of large codebases. You will learn more about it later this week.

Before you start using React, it is important to understand the role of frameworks and libraries in web development.
What Is A Framework?
A framework is a collection of tools and features built into a language that attempts to save a developer time by automating the mundane tasks they would normally have to complete manually. Angular (Links to an external site.) is a front-end framework that includes built-in functionality and a computer-line interface tool. Angular is opinionated, meaning that it enforces the developer to follow a specific folder structure and development practices.

For example, suppose you are developing a user input form. If you are using a framework like Angular, you will have to use specific, built-in form functionality to create it. A library, on the other hand, will allow you to create the form with more flexibility.

What Is A Library?
A library is an unopinionated collection of prewritten code. Unopinionated means that it offers flexibility and freedom when developing an application. React is a JavaScript library that has no one specific folder structure that you must follow and no built-in functionality for things like routing, forms, or network calls. Instead, the developer must decide how they will structure their project and what packages they will use.

When To Use A Framework Vs. A Library
Frameworks and libraries have advantages and disadvantages. Both options are widely used in the software development industry, and it is good to be familiar with them. You should choose what you use based on the needs of your project and your personal preferences.

Advantages	Disadvantages	Examples
Framework	You can develop an application quickly without making decisions upfront.	You have less flexibility in how your application operates and what tools you can use.	Angular, Next.js, Redwood.js, Vue
Library	You have complete control over the codebase and the flexibility to use several packages and tools within your application.	You have to create the application manually and make several decisions, which will take longer.	React
In this course, you will learn how to use the React library and how to make decisions about the development of your application. After you learn how to leverage the library, if you want to add the framework functionality, you can use frameworks that are based on React (e.g., Next.js (Links to an external site.), Gatsby (Links to an external site.), and Redwood.js (Links to an external site.)).

# What is JSX?
JSX  (Links to an external site.)is a JavaScript syntax extension that allows HTML-like code to be written in JavaScript. With JSX, you can put HTML-like syntax inside of JavaScript code to render an HTML element and give it functionality.

Unlike Angular and Vue, which use HTML templates, React uses JSX to combine the UI code and logic in one place.

Introduction To JSX Syntax
Review the example of JSX below:

const title = 'Hello World';

const element = <h1>{title}</h1>;
Notice how the <h1> elements and reference to the title variable are assigned to the element variable. In this example of JSX, the HTML elements are assigned to a JavaScript variable.

If the element variable was rendered by React, the web page would display the text ???Hello World??? in h1 (header) tags.
  
# ReactDOM 
ReactDOM is a shadow DOM that synchronizes with the browser DOM. ReactDOM ensures that the entire page does not have to re-render when an individual component is updated.

In order to run the code shown in this video, please use the starter files within the ???Introduction to JSX??? folder, which you can download from the Introduction and Instructions page.

Additionally, you will need to have node installed  (Links to an external site.)so you can run the following command to install http-server:

npm install -g http-server

After this installs, you may need to restart your terminal in order to run the http-server command from the directory that houses the starter files.

Note: If you are using Windows and you get the following message when running the http-server command (execution of scripts is disabled on this system), please reference this link (Links to an external site.) for a resolution. More specifically, you may need to run Set-ExecutionPolicy RemoteSigned from an administrator terminal to successfully run the http-server command.

# State
State
When data on the web changes, such as when a user selects a button, React updates the React DOM. The automatic management of data on a web page through React is called state.

Suppose that you stored a list of users in a JavaScript object, and the users are displayed as a table on a web page. In this example, the user data is the state.

User ID

Username

1

peter.parker

2

bruce.wayne

3

tchalla

4

diana.prince

If you created this object with React, the user data table would be a component. This userComponent would manage its own state, hence updating the list of users when changes are made. React is declarative, which means that when the state (or data) is changed, React updates the interface accordingly. 

User ID

Username

1

peter.parker

2

bruce.wayne

3

tchalla

4

diana.prince

5

dr.strange

State Example
Imagine a component that acts as a counter. The counter starts at zero, and the user selects a button to increment the counter by one.

1.PNG

Since the counter is a component, which can be reused, there can be multiple instances of the counter on one web page. Using what you know about state and components, what would happen if there were two counters on the page and the user selected one of the buttons to increment the counter?

If you predicted that only the counter instance that the user selected would increment, you are correct. The component???s state is internal, and multiple instances of the component do not share the same state. 

2.PNG


To enforce the same state between multiple components or  instances of components, there are two common patterns in React: lifting the state to a common parent component or a centralized state store such as Redux that can be made available to any component. You will learn more about this in Week 16. 

# Destructuring 
 Destructuring allows you to unpack values from arrays or properties from objects and assign them to different variables.

Assigning Properties Without Destructuring
Review the example that assigns an object???s properties without destructuring below.

Imagine you have an object called product containing three properties: name, cost, and inStock.

let product = {name: 'pear', cost: 2, inStock: 7};
Now suppose you create two new variables, one for the product???s name property and the other for the product???s inStock property.

Without destructuring, you would handle it like this:

let name = product.name;
let inStock = product.inStock;
Assigning Properties With Destructuring
With destructuring, you can assign the properties with just one line of code.

Start by creating a new variable with let, var, or const. Instead of adding a single variable name, you can add multiple variable names inside curly brackets.

let { name, inStock } = product;
This tells JavaScript to create a variable called name and assign it to the property inside of product called name. It also tells JavaScript to create a variable called inStock and assign it to the property inside of product called inStock.

If you print those variables to the console, you will see the data.

console.log(name);    // 'pear'
console.log(inStock); // 7
It???s important to know that the name inside the curly brackets must match the property name inside the object you are looking at. So, for example, if you use the same code above but add another variable called ordered, it will look like this:

let { name, inStock, ordered } = product;
The variable ordered would be undefined because there is no property called ordered inside the product object.

Destructuring allows you to save time by writing less code. While you only saw how to use destructuring with an object in this example, you can also use it with arrays and function parameters.

Review the Mozilla Developer Network (MDN) documentation here (Links to an external site.) to see all the different ways you can use destructuring and their corresponding examples.
